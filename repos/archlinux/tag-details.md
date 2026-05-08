<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260503.0.523481`](#archlinuxbase-202605030523481)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260503.0.523481`](#archlinuxbase-devel-202605030523481)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260503.0.523481`](#archlinuxmultilib-devel-202605030523481)

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

## `archlinux:base-20260503.0.523481`

```console
$ docker pull archlinux@sha256:36301eef718527e362e568206b7606a3246c1fc089b24fce20c47cf68065f229
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260503.0.523481` - linux; amd64

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

### `archlinux:base-20260503.0.523481` - unknown; unknown

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

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:fdff15f24df062598faebf380430955a9bd2109736e179ebb354f1208f725774
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

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

### `archlinux:base-devel` - unknown; unknown

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

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:36301eef718527e362e568206b7606a3246c1fc089b24fce20c47cf68065f229
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

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

### `archlinux:latest` - unknown; unknown

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

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:98169d312640757c3f9fbc5f91c48b6ef5963da789fbe88b0889418f6f233e4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ad87a9b436197a5e25abf2f5b202bf63be776183bad12616f6ec80199cf482d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275758734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af28ca4534de49ae005e159344b62cae7f473dc060869f033eb0ce3149ee2d08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.version=20260503.0.523481
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.created=2026-05-03T00:09:00+00:00
# Fri, 08 May 2026 00:02:33 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 00:02:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260503.0.523481' /etc/os-release &&     true # buildkit
# Fri, 08 May 2026 00:02:39 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:02:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8951f99ef7054daea6754cde72fc40693309fac635c287747b166ae7aab04943`  
		Last Modified: Fri, 08 May 2026 00:03:26 GMT  
		Size: 275.7 MB (275748374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0633fd9a26c06df0d03ae07ceac7e3df2ab689769502a4a7a7beb94739aa02`  
		Last Modified: Fri, 08 May 2026 00:03:20 GMT  
		Size: 10.4 KB (10360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:62a319e8fe7f939908a6c93dd5988079c2d93eb8a6ad28aade2b00173321bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12318897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa2f71c15a41baca3a95cde3c2b3eeb310dfa5262767ac620d9fbe879ab129f`

```dockerfile
```

-	Layers:
	-	`sha256:28257b1970bb43035f51c37a1292e0d13ab330a8d7b9f0642ee6b771dc79e027`  
		Last Modified: Fri, 08 May 2026 00:03:21 GMT  
		Size: 12.3 MB (12307047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6414041c06bcecfe359359ec3bb5ef24defb75ec47d81a8c9a0e7b2a98409316`  
		Last Modified: Fri, 08 May 2026 00:03:20 GMT  
		Size: 11.8 KB (11850 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260503.0.523481`

```console
$ docker pull archlinux@sha256:98169d312640757c3f9fbc5f91c48b6ef5963da789fbe88b0889418f6f233e4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260503.0.523481` - linux; amd64

```console
$ docker pull archlinux@sha256:ad87a9b436197a5e25abf2f5b202bf63be776183bad12616f6ec80199cf482d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275758734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af28ca4534de49ae005e159344b62cae7f473dc060869f033eb0ce3149ee2d08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.version=20260503.0.523481
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Fri, 08 May 2026 00:02:33 GMT
LABEL org.opencontainers.image.created=2026-05-03T00:09:00+00:00
# Fri, 08 May 2026 00:02:33 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 00:02:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260503.0.523481' /etc/os-release &&     true # buildkit
# Fri, 08 May 2026 00:02:39 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 00:02:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8951f99ef7054daea6754cde72fc40693309fac635c287747b166ae7aab04943`  
		Last Modified: Fri, 08 May 2026 00:03:26 GMT  
		Size: 275.7 MB (275748374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0633fd9a26c06df0d03ae07ceac7e3df2ab689769502a4a7a7beb94739aa02`  
		Last Modified: Fri, 08 May 2026 00:03:20 GMT  
		Size: 10.4 KB (10360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260503.0.523481` - unknown; unknown

```console
$ docker pull archlinux@sha256:62a319e8fe7f939908a6c93dd5988079c2d93eb8a6ad28aade2b00173321bb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12318897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aa2f71c15a41baca3a95cde3c2b3eeb310dfa5262767ac620d9fbe879ab129f`

```dockerfile
```

-	Layers:
	-	`sha256:28257b1970bb43035f51c37a1292e0d13ab330a8d7b9f0642ee6b771dc79e027`  
		Last Modified: Fri, 08 May 2026 00:03:21 GMT  
		Size: 12.3 MB (12307047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6414041c06bcecfe359359ec3bb5ef24defb75ec47d81a8c9a0e7b2a98409316`  
		Last Modified: Fri, 08 May 2026 00:03:20 GMT  
		Size: 11.8 KB (11850 bytes)  
		MIME: application/vnd.in-toto+json
