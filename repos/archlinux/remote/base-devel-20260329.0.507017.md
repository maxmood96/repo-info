## `archlinux:base-devel-20260329.0.507017`

```console
$ docker pull archlinux@sha256:0cce2e42862208217cb44f67feb93630e45300619d293601202d34bb6cf77d98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260329.0.507017` - linux; amd64

```console
$ docker pull archlinux@sha256:123b63f10fdac8af4bbcf2bf0565082b9e19eaef311da03a523a4995e07393e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246377153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f075a6a53dd9b45825d6ad9f8769bde141a07cdb520ef9205a20e1e7701bb5a8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.version=20260329.0.507017
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 30 Mar 2026 17:34:16 GMT
LABEL org.opencontainers.image.created=2026-03-29T00:10:46+00:00
# Mon, 30 Mar 2026 17:34:16 GMT
COPY /rootfs/ / # buildkit
# Mon, 30 Mar 2026 17:34:21 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260329.0.507017' /etc/os-release # buildkit
# Mon, 30 Mar 2026 17:34:21 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:34:21 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2241eba7336df872244d714d678a5ab3d7540c9727f8a0eeac67f4dc21f34347`  
		Last Modified: Mon, 30 Mar 2026 17:35:04 GMT  
		Size: 246.4 MB (246368027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb0ad76c12cff38bd7ccff8402fce8e797f088166f4a457357abec93cb0b079`  
		Last Modified: Mon, 30 Mar 2026 17:34:59 GMT  
		Size: 9.1 KB (9126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260329.0.507017` - unknown; unknown

```console
$ docker pull archlinux@sha256:ffc17fca7797f937b5429bf427a22af764033b39344a6bd41079e10ba16332be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11943958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4102788cdc55328c1906bb18d99d3a59c0870d737727c096132c585c45c6c3fb`

```dockerfile
```

-	Layers:
	-	`sha256:abaf8ecd218dac943b2bc32c0122201ad967e957f088ea8653b1d0da9b60fe62`  
		Last Modified: Mon, 30 Mar 2026 17:34:59 GMT  
		Size: 11.9 MB (11932247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec6888e600025dca5ff64693b1cea8f79213a10a2458b0a854b2ab0815dad9b`  
		Last Modified: Mon, 30 Mar 2026 17:34:59 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
