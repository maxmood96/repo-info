## `archlinux:base`

```console
$ docker pull archlinux@sha256:36301eef718527e362e568206b7606a3246c1fc089b24fce20c47cf68065f229
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:84041fa7d2356dc834e1db51a966d5227767c91f3426e49a5d0767630f504930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130847260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db57fd93d724000a32c8d78d3c1c74a2cdfc476a0c6f9d4fde00a9e70f796c0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.version=20260503.0.523481
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Fri, 08 May 2026 00:02:16 GMT
LABEL org.opencontainers.image.created=2026-05-03T00:09:00+00:00
# Fri, 08 May 2026 00:02:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 00:02:19 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260503.0.523481' /etc/os-release &&     true # buildkit
# Fri, 08 May 2026 00:02:19 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:02:19 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ff6163e82a1a48b5420062702259bf8c58422d48e2873d208e9be1eb3df2d300`  
		Last Modified: Fri, 08 May 2026 00:02:45 GMT  
		Size: 130.8 MB (130838583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8250652c20a77b66f9d8922e6ef2a8706826032ea3530f5ee920cb22ceecd229`  
		Last Modified: Fri, 08 May 2026 00:02:42 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:c5656e85c0b4b4a1c141445da78520ba9555998e49fd62ccf8a6983f0e0e884f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aeefecfa83c156cf53d06bc97b176e5e8074f7f6aec07b60f51a83747421c31`

```dockerfile
```

-	Layers:
	-	`sha256:8c375492f00184ad10837c7e731dec0139e2c66e02c3b9e3480e08511b865ddd`  
		Last Modified: Fri, 08 May 2026 00:02:43 GMT  
		Size: 8.2 MB (8182970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7543b6c75a9b2afd3a607df0500c36f090a1d22bd388584fb041b26ea7a1abc`  
		Last Modified: Fri, 08 May 2026 00:02:42 GMT  
		Size: 12.0 KB (12006 bytes)  
		MIME: application/vnd.in-toto+json
