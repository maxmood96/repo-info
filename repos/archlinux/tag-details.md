<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20251214.0.467559`](#archlinuxbase-202512140467559)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20251214.0.467559`](#archlinuxbase-devel-202512140467559)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20251214.0.467559`](#archlinuxmultilib-devel-202512140467559)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:69a7520c58d27f1b2ee52dd61f6496e632582616b89c7952865f56b44617772b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:f6d2fbe8e7c8763f89d8fc37006df2a12747d6a85e554c703eafe3f5a7e175d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174525090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eac4baa2770ac68b66b93da02fbc9ee0dc9789221199fc131855ec51b198d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:27:34 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:37 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:27:37 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:37 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f01404d5588892b3d97f4e80816575127ee71f0db9920a3765dc85e0df6538e3`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 174.5 MB (174516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037507b733bf8957243f82eb85384dca6103f75f860e6970d02932b12ebcf981`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 8.7 KB (8676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:80fc79d4c4cc9b3c54691d7a75f17a01c1576813c96c7235f52e946a964ebaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5d453a40bffa2a8a017e7549dfd395c98dd9175e3fba11b8fad39d8016fd1`

```dockerfile
```

-	Layers:
	-	`sha256:0912bca3e78d9bc46e93737696b4a453be2f839e857ecb3d98e6026495827b96`  
		Last Modified: Thu, 18 Dec 2025 02:48:16 GMT  
		Size: 8.4 MB (8368818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260e755189df09fbee502bb31d2a6f7a6549e7ab8750c1c0542988126e6d20b0`  
		Last Modified: Thu, 18 Dec 2025 02:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251214.0.467559`

```console
$ docker pull archlinux@sha256:69a7520c58d27f1b2ee52dd61f6496e632582616b89c7952865f56b44617772b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:f6d2fbe8e7c8763f89d8fc37006df2a12747d6a85e554c703eafe3f5a7e175d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174525090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eac4baa2770ac68b66b93da02fbc9ee0dc9789221199fc131855ec51b198d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:27:34 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:37 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:27:37 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:37 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f01404d5588892b3d97f4e80816575127ee71f0db9920a3765dc85e0df6538e3`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 174.5 MB (174516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037507b733bf8957243f82eb85384dca6103f75f860e6970d02932b12ebcf981`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 8.7 KB (8676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:80fc79d4c4cc9b3c54691d7a75f17a01c1576813c96c7235f52e946a964ebaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5d453a40bffa2a8a017e7549dfd395c98dd9175e3fba11b8fad39d8016fd1`

```dockerfile
```

-	Layers:
	-	`sha256:0912bca3e78d9bc46e93737696b4a453be2f839e857ecb3d98e6026495827b96`  
		Last Modified: Thu, 18 Dec 2025 02:48:16 GMT  
		Size: 8.4 MB (8368818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260e755189df09fbee502bb31d2a6f7a6549e7ab8750c1c0542988126e6d20b0`  
		Last Modified: Thu, 18 Dec 2025 02:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:9414f5b766a34ebd769608b9ec80e1b4bfd7ea5e86dd49cae06ae308ad6c4221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:e70875c9b4d9255ca79874fb4ea44a635786e6029f130ee4aa1ba4fe583eab5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4633b6c477df051bc51c08ae1f6409f12ebe939c41d02f71d544b3fa14b197b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:28:57 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:29:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:29:04 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:28f03c6e8bb3a7030933065fad15d28b50b0bfc498ea6d4cedd92904feb81e22`  
		Last Modified: Mon, 15 Dec 2025 18:33:53 GMT  
		Size: 292.1 MB (292061547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec6827e8076675e684a976065d24343ac4e4526b572e6fc2fac4f4f4bc9e13f`  
		Last Modified: Thu, 18 Dec 2025 00:29:57 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d2d7cd076c4272924466ed1ea4ed4313bb018e888c6fa6392bca372a5ed90d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12142872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92432e93531d948c726d191ad80db451daba2730389a263533b13a0c978e2016`

```dockerfile
```

-	Layers:
	-	`sha256:270abacd820fb98a36d2ac78e0a917a713abf3c021771795b148c556408dffb7`  
		Last Modified: Thu, 18 Dec 2025 02:48:22 GMT  
		Size: 12.1 MB (12131161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ccbcee7b05649d682c72ab32235add143982b403be4f0be2a265ebdf79c014`  
		Last Modified: Thu, 18 Dec 2025 02:48:23 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251214.0.467559`

```console
$ docker pull archlinux@sha256:9414f5b766a34ebd769608b9ec80e1b4bfd7ea5e86dd49cae06ae308ad6c4221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:e70875c9b4d9255ca79874fb4ea44a635786e6029f130ee4aa1ba4fe583eab5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292070731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4633b6c477df051bc51c08ae1f6409f12ebe939c41d02f71d544b3fa14b197b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:28:57 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:28:57 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:29:04 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:29:04 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:04 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:28f03c6e8bb3a7030933065fad15d28b50b0bfc498ea6d4cedd92904feb81e22`  
		Last Modified: Mon, 15 Dec 2025 18:33:53 GMT  
		Size: 292.1 MB (292061547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec6827e8076675e684a976065d24343ac4e4526b572e6fc2fac4f4f4bc9e13f`  
		Last Modified: Thu, 18 Dec 2025 00:29:57 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:d2d7cd076c4272924466ed1ea4ed4313bb018e888c6fa6392bca372a5ed90d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12142872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92432e93531d948c726d191ad80db451daba2730389a263533b13a0c978e2016`

```dockerfile
```

-	Layers:
	-	`sha256:270abacd820fb98a36d2ac78e0a917a713abf3c021771795b148c556408dffb7`  
		Last Modified: Thu, 18 Dec 2025 02:48:22 GMT  
		Size: 12.1 MB (12131161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ccbcee7b05649d682c72ab32235add143982b403be4f0be2a265ebdf79c014`  
		Last Modified: Thu, 18 Dec 2025 02:48:23 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:69a7520c58d27f1b2ee52dd61f6496e632582616b89c7952865f56b44617772b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:f6d2fbe8e7c8763f89d8fc37006df2a12747d6a85e554c703eafe3f5a7e175d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174525090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77eac4baa2770ac68b66b93da02fbc9ee0dc9789221199fc131855ec51b198d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:27:34 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:27:34 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:37 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:27:37 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:27:37 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f01404d5588892b3d97f4e80816575127ee71f0db9920a3765dc85e0df6538e3`  
		Last Modified: Mon, 15 Dec 2025 20:48:23 GMT  
		Size: 174.5 MB (174516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037507b733bf8957243f82eb85384dca6103f75f860e6970d02932b12ebcf981`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 8.7 KB (8676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:80fc79d4c4cc9b3c54691d7a75f17a01c1576813c96c7235f52e946a964ebaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8380747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d5d453a40bffa2a8a017e7549dfd395c98dd9175e3fba11b8fad39d8016fd1`

```dockerfile
```

-	Layers:
	-	`sha256:0912bca3e78d9bc46e93737696b4a453be2f839e857ecb3d98e6026495827b96`  
		Last Modified: Thu, 18 Dec 2025 02:48:16 GMT  
		Size: 8.4 MB (8368818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260e755189df09fbee502bb31d2a6f7a6549e7ab8750c1c0542988126e6d20b0`  
		Last Modified: Thu, 18 Dec 2025 02:48:17 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:6455ac31ed0d5f0fbd0f534ef3be9b18de5bda5d1c89e0482bc701d14d4e2bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:17a0d8bc467497f4245007c0969e42c1c4e679c75932aa60ade0c88b166216c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343393677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd00528193253ec8633b53549063fe9fd16cb792aaf0baf86e5d4a09a1db93b6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7b1e20b4fe65799151a60bf5d121f5f6f83fcd2aca9d80b1b2515a189308c3fd`  
		Last Modified: Mon, 15 Dec 2025 18:34:37 GMT  
		Size: 343.4 MB (343383370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a33c1bca70186f8c39bbc030c8d90520413062e000fe4f7bf591df1c2b5abd`  
		Last Modified: Thu, 18 Dec 2025 00:30:08 GMT  
		Size: 10.3 KB (10307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9c65c7622ac836cbe353b8a53e983ba743dc9b03e45a7c33a51e8a9cd41250d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ad4c303e019fc1250c5e620187a06087f0d6daa420d34789ed3110b4bcfe1`

```dockerfile
```

-	Layers:
	-	`sha256:6d9bab6330d8043df3604ceeb286b5a8f752c4f6d2831434175f45a330c42a4a`  
		Last Modified: Thu, 18 Dec 2025 02:48:31 GMT  
		Size: 12.4 MB (12399954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddaa5f6bf808068817ad2f978a0b0fc14400c0b2a367c5f05b32fdb966a238ee`  
		Last Modified: Thu, 18 Dec 2025 02:48:32 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251214.0.467559`

```console
$ docker pull archlinux@sha256:6455ac31ed0d5f0fbd0f534ef3be9b18de5bda5d1c89e0482bc701d14d4e2bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251214.0.467559` - linux; amd64

```console
$ docker pull archlinux@sha256:17a0d8bc467497f4245007c0969e42c1c4e679c75932aa60ade0c88b166216c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343393677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd00528193253ec8633b53549063fe9fd16cb792aaf0baf86e5d4a09a1db93b6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7b1e20b4fe65799151a60bf5d121f5f6f83fcd2aca9d80b1b2515a189308c3fd`  
		Last Modified: Mon, 15 Dec 2025 18:34:37 GMT  
		Size: 343.4 MB (343383370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a33c1bca70186f8c39bbc030c8d90520413062e000fe4f7bf591df1c2b5abd`  
		Last Modified: Thu, 18 Dec 2025 00:30:08 GMT  
		Size: 10.3 KB (10307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251214.0.467559` - unknown; unknown

```console
$ docker pull archlinux@sha256:9c65c7622ac836cbe353b8a53e983ba743dc9b03e45a7c33a51e8a9cd41250d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ad4c303e019fc1250c5e620187a06087f0d6daa420d34789ed3110b4bcfe1`

```dockerfile
```

-	Layers:
	-	`sha256:6d9bab6330d8043df3604ceeb286b5a8f752c4f6d2831434175f45a330c42a4a`  
		Last Modified: Thu, 18 Dec 2025 02:48:31 GMT  
		Size: 12.4 MB (12399954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddaa5f6bf808068817ad2f978a0b0fc14400c0b2a367c5f05b32fdb966a238ee`  
		Last Modified: Thu, 18 Dec 2025 02:48:32 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
