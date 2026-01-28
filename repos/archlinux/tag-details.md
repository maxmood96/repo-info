<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260125.0.484595`](#archlinuxbase-202601250484595)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260125.0.484595`](#archlinuxbase-devel-202601250484595)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260125.0.484595`](#archlinuxmultilib-devel-202601250484595)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:4585b6322b40a28877dbe2363c7281dd046d9289300a36f58edc207ed1c8db90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:09e04a8a3e454c0c3349a57cd55723300d675aaa3c9316583f4e092290a9e241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565265df54812b4519894e6d690dd2b19d5d1fefc81e8bb325e4ccc2fb729c60`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:14:25 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:14:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb0318c5d907dd630183122cc0e398efa682d9e87262c08e1a42453f89881cb`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:978f9926de3a1e20127fdb92661d4e1963e30aa0b573899b0fe90f179a01e346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7462992050a70ad73f1d556e805d8785a19ffdd471d169d8897483e4c9ae3fd`

```dockerfile
```

-	Layers:
	-	`sha256:c2609cd1cc40277c4e3ccd82558b96c15ea9128a314d16a3b7042079b560ee50`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d81a3b55b35bade08946f84782dd563d97c014bcfbea47f897fc1eb7badd30`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260125.0.484595`

```console
$ docker pull archlinux@sha256:4585b6322b40a28877dbe2363c7281dd046d9289300a36f58edc207ed1c8db90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260125.0.484595` - linux; amd64

```console
$ docker pull archlinux@sha256:09e04a8a3e454c0c3349a57cd55723300d675aaa3c9316583f4e092290a9e241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565265df54812b4519894e6d690dd2b19d5d1fefc81e8bb325e4ccc2fb729c60`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:14:25 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:14:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb0318c5d907dd630183122cc0e398efa682d9e87262c08e1a42453f89881cb`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260125.0.484595` - unknown; unknown

```console
$ docker pull archlinux@sha256:978f9926de3a1e20127fdb92661d4e1963e30aa0b573899b0fe90f179a01e346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7462992050a70ad73f1d556e805d8785a19ffdd471d169d8897483e4c9ae3fd`

```dockerfile
```

-	Layers:
	-	`sha256:c2609cd1cc40277c4e3ccd82558b96c15ea9128a314d16a3b7042079b560ee50`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d81a3b55b35bade08946f84782dd563d97c014bcfbea47f897fc1eb7badd30`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c26263d698029443e20a4dcfa26d4c7180216f28fa5dbe6a6c12f8f031dc757b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:354f88d30991e6d9a7dcd831fda1983701fe7c4b40cfd8b2b8b29ff4b41177a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293785552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7612e886c56dc6d1a291b346986b51af2362f38280bf81ff22a9f0d2d34f9b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:13:46 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:13:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:13:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1e89069645e551320191d6ed4f9c08c6914dfd1f3290113122c929bd19065ebc`  
		Last Modified: Mon, 26 Jan 2026 19:37:49 GMT  
		Size: 293.8 MB (293776194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316601f3a3fb10987a7d2a44b0e4251175abf717727a7391499227120e07029f`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3cdc30e26f2f1c634cedcab1c3431efbc51d32a40019eb40794e736c483a65f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098dd36798168957b53dd47921b550a4bf4402311225af1d477d0e8ec4678d89`

```dockerfile
```

-	Layers:
	-	`sha256:c96eb7a7d902d72e3ab09d6292f560b31f626eee765fd62443d43963667be31f`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05314a8379a20655073273bc14a6baf271a4585b4d8ea3c952bdf5ea5526565`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260125.0.484595`

```console
$ docker pull archlinux@sha256:c26263d698029443e20a4dcfa26d4c7180216f28fa5dbe6a6c12f8f031dc757b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260125.0.484595` - linux; amd64

```console
$ docker pull archlinux@sha256:354f88d30991e6d9a7dcd831fda1983701fe7c4b40cfd8b2b8b29ff4b41177a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293785552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7612e886c56dc6d1a291b346986b51af2362f38280bf81ff22a9f0d2d34f9b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:13:46 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:13:46 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:13:52 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:13:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1e89069645e551320191d6ed4f9c08c6914dfd1f3290113122c929bd19065ebc`  
		Last Modified: Mon, 26 Jan 2026 19:37:49 GMT  
		Size: 293.8 MB (293776194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316601f3a3fb10987a7d2a44b0e4251175abf717727a7391499227120e07029f`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260125.0.484595` - unknown; unknown

```console
$ docker pull archlinux@sha256:3cdc30e26f2f1c634cedcab1c3431efbc51d32a40019eb40794e736c483a65f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098dd36798168957b53dd47921b550a4bf4402311225af1d477d0e8ec4678d89`

```dockerfile
```

-	Layers:
	-	`sha256:c96eb7a7d902d72e3ab09d6292f560b31f626eee765fd62443d43963667be31f`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b05314a8379a20655073273bc14a6baf271a4585b4d8ea3c952bdf5ea5526565`  
		Last Modified: Wed, 28 Jan 2026 02:14:35 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:4585b6322b40a28877dbe2363c7281dd046d9289300a36f58edc207ed1c8db90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:09e04a8a3e454c0c3349a57cd55723300d675aaa3c9316583f4e092290a9e241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565265df54812b4519894e6d690dd2b19d5d1fefc81e8bb325e4ccc2fb729c60`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:14:25 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:14:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb0318c5d907dd630183122cc0e398efa682d9e87262c08e1a42453f89881cb`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:978f9926de3a1e20127fdb92661d4e1963e30aa0b573899b0fe90f179a01e346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7462992050a70ad73f1d556e805d8785a19ffdd471d169d8897483e4c9ae3fd`

```dockerfile
```

-	Layers:
	-	`sha256:c2609cd1cc40277c4e3ccd82558b96c15ea9128a314d16a3b7042079b560ee50`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d81a3b55b35bade08946f84782dd563d97c014bcfbea47f897fc1eb7badd30`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:62b48a4626012151d9ee4af09327960544705347c1a5d7fc1b201e6cb6c68a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0755415f74a28c1929b1943844e3ee61fc56b7c184adb0520c3fcc296aa5524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345103912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a82e0671c48eb44cbf77019aa289814255fe288e4cf72e2d90232cf075bf89f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:15:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:15:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b082aaf37d1f8448ecdf12a68276aa8babba8acde9f2d22a3396b4db41c0684d`  
		Last Modified: Mon, 26 Jan 2026 19:37:38 GMT  
		Size: 345.1 MB (345093462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b9c8e8e1cf6559d71b9af774ae973e20cff63e99786d53a47af30139ee2b9`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a23a2753526a42201223973ccc77d6c5c1717d0df974080445005859a1b508bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2780033282d205047f48551a33524b2ecb8776b9b25acd6206a42b2e920d3cf`

```dockerfile
```

-	Layers:
	-	`sha256:43f3a03a18066722189daa2d4482e24262a4c8fa5406bd0454c0aabf9b7201b6`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 12.4 MB (12431019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44cb6afc2af36a9e94721f186ccc689077d74a4dc38a8306a62d73c53826f80`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260125.0.484595`

```console
$ docker pull archlinux@sha256:62b48a4626012151d9ee4af09327960544705347c1a5d7fc1b201e6cb6c68a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260125.0.484595` - linux; amd64

```console
$ docker pull archlinux@sha256:0755415f74a28c1929b1943844e3ee61fc56b7c184adb0520c3fcc296aa5524a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345103912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a82e0671c48eb44cbf77019aa289814255fe288e4cf72e2d90232cf075bf89f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:15:07 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:15:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:15:15 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:15:15 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b082aaf37d1f8448ecdf12a68276aa8babba8acde9f2d22a3396b4db41c0684d`  
		Last Modified: Mon, 26 Jan 2026 19:37:38 GMT  
		Size: 345.1 MB (345093462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486b9c8e8e1cf6559d71b9af774ae973e20cff63e99786d53a47af30139ee2b9`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260125.0.484595` - unknown; unknown

```console
$ docker pull archlinux@sha256:a23a2753526a42201223973ccc77d6c5c1717d0df974080445005859a1b508bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2780033282d205047f48551a33524b2ecb8776b9b25acd6206a42b2e920d3cf`

```dockerfile
```

-	Layers:
	-	`sha256:43f3a03a18066722189daa2d4482e24262a4c8fa5406bd0454c0aabf9b7201b6`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 12.4 MB (12431019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d44cb6afc2af36a9e94721f186ccc689077d74a4dc38a8306a62d73c53826f80`  
		Last Modified: Wed, 28 Jan 2026 02:16:06 GMT  
		Size: 11.8 KB (11765 bytes)  
		MIME: application/vnd.in-toto+json
