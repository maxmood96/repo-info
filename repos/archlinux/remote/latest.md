## `archlinux:latest`

```console
$ docker pull archlinux@sha256:644b416048d39616bbaca93ce768ba492655c83fba80ceca65a4f59dcabdcac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:901ce548a325fe7cec8895e5837343af9c8ec89edb420d3a96b2cc6f5e86c771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.7 MB (176684514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bd5aa142840790b05c0cd1cfd1a2f45f027f26a821c992efb9e83f04956c10`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.version=20260208.0.488728
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Feb 2026 19:34:50 GMT
LABEL org.opencontainers.image.created=2026-02-08T00:07:04+00:00
# Mon, 09 Feb 2026 19:34:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260208.0.488728' /etc/os-release # buildkit
# Mon, 09 Feb 2026 19:34:54 GMT
ENV LANG=C.UTF-8
# Mon, 09 Feb 2026 19:34:54 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2efc828fc4c1e8872ffc2e6302cc5e768e96b0c007f65ca96fda719e3926c471`  
		Last Modified: Mon, 09 Feb 2026 19:35:24 GMT  
		Size: 176.7 MB (176675766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92388da7a721ababcdfa711244fe175254c409e8ec45b989a260e040ac66de2`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:f116c06fbb3b80b9a67e514e433887fd39d59a47bd78f76c1a98b0eaef5f4914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8416418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7480c9ee28ee5c453d165ffaadfebba1c72a33a47d386656cd15589377306a61`

```dockerfile
```

-	Layers:
	-	`sha256:999756a439ced73a1fc9afa4c48923466350a0ffd2850efa2aa8ffb00eb067c8`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 8.4 MB (8404489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b77473698ebeedd394103e94dde7256d5b49922a8e6bd9e398969798f7b1b505`  
		Last Modified: Mon, 09 Feb 2026 19:35:20 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
