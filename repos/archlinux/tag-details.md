<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260329.0.507017`](#archlinuxbase-202603290507017)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260329.0.507017`](#archlinuxbase-devel-202603290507017)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260329.0.507017`](#archlinuxmultilib-devel-202603290507017)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:237637c52069930ed7fc76c76f04b6b6b9cf82c5222ae002b7932df983cb69c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:f0f37234a62d4e948cdd6beee7057651393129f240172f52043fd33850cad7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128730662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6a8dcab3e30e6f226e4655831eaa6a15b7e6940f247a10e24f5d8240b69d4f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.version=20260329.0.507017
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.created=2026-03-29T00:10:46+00:00
# Mon, 30 Mar 2026 17:33:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 30 Mar 2026 17:33:03 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260329.0.507017' /etc/os-release # buildkit
# Mon, 30 Mar 2026 17:33:03 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:33:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:976a2c87c6cdf25305f991155660a6ffc3f6fdbd7f2663b31c47787e697fac81`  
		Last Modified: Mon, 30 Mar 2026 17:33:27 GMT  
		Size: 128.7 MB (128722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb366f7addb676024810e17876aaac00317b42e2b465e2266e92744fcbbd566`  
		Last Modified: Mon, 30 Mar 2026 17:33:24 GMT  
		Size: 8.6 KB (8598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:7b72b0b30b022c84693ba99bb4f9fe61e9cbef059b9ad9ffa86f078d483934f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8159328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a4c7f34d503a61c54d123884e376f53c1292fd8c64a836b3e9955539c98d76`

```dockerfile
```

-	Layers:
	-	`sha256:fcf157e6cb88191f05a038d7ad1fee7a645401eb74f68af6758cb94abef5f049`  
		Last Modified: Mon, 30 Mar 2026 17:33:24 GMT  
		Size: 8.1 MB (8147399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d390d05224faa3d7977494c904579b255840907f092d77922675463b1897d327`  
		Last Modified: Mon, 30 Mar 2026 17:33:23 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260329.0.507017`

```console
$ docker pull archlinux@sha256:237637c52069930ed7fc76c76f04b6b6b9cf82c5222ae002b7932df983cb69c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260329.0.507017` - linux; amd64

```console
$ docker pull archlinux@sha256:f0f37234a62d4e948cdd6beee7057651393129f240172f52043fd33850cad7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128730662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6a8dcab3e30e6f226e4655831eaa6a15b7e6940f247a10e24f5d8240b69d4f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.version=20260329.0.507017
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.created=2026-03-29T00:10:46+00:00
# Mon, 30 Mar 2026 17:33:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 30 Mar 2026 17:33:03 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260329.0.507017' /etc/os-release # buildkit
# Mon, 30 Mar 2026 17:33:03 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:33:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:976a2c87c6cdf25305f991155660a6ffc3f6fdbd7f2663b31c47787e697fac81`  
		Last Modified: Mon, 30 Mar 2026 17:33:27 GMT  
		Size: 128.7 MB (128722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb366f7addb676024810e17876aaac00317b42e2b465e2266e92744fcbbd566`  
		Last Modified: Mon, 30 Mar 2026 17:33:24 GMT  
		Size: 8.6 KB (8598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260329.0.507017` - unknown; unknown

```console
$ docker pull archlinux@sha256:7b72b0b30b022c84693ba99bb4f9fe61e9cbef059b9ad9ffa86f078d483934f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8159328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a4c7f34d503a61c54d123884e376f53c1292fd8c64a836b3e9955539c98d76`

```dockerfile
```

-	Layers:
	-	`sha256:fcf157e6cb88191f05a038d7ad1fee7a645401eb74f68af6758cb94abef5f049`  
		Last Modified: Mon, 30 Mar 2026 17:33:24 GMT  
		Size: 8.1 MB (8147399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d390d05224faa3d7977494c904579b255840907f092d77922675463b1897d327`  
		Last Modified: Mon, 30 Mar 2026 17:33:23 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0cce2e42862208217cb44f67feb93630e45300619d293601202d34bb6cf77d98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

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

### `archlinux:base-devel` - unknown; unknown

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

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:237637c52069930ed7fc76c76f04b6b6b9cf82c5222ae002b7932df983cb69c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:f0f37234a62d4e948cdd6beee7057651393129f240172f52043fd33850cad7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128730662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6a8dcab3e30e6f226e4655831eaa6a15b7e6940f247a10e24f5d8240b69d4f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.version=20260329.0.507017
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 30 Mar 2026 17:33:01 GMT
LABEL org.opencontainers.image.created=2026-03-29T00:10:46+00:00
# Mon, 30 Mar 2026 17:33:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 30 Mar 2026 17:33:03 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260329.0.507017' /etc/os-release # buildkit
# Mon, 30 Mar 2026 17:33:03 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:33:03 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:976a2c87c6cdf25305f991155660a6ffc3f6fdbd7f2663b31c47787e697fac81`  
		Last Modified: Mon, 30 Mar 2026 17:33:27 GMT  
		Size: 128.7 MB (128722064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb366f7addb676024810e17876aaac00317b42e2b465e2266e92744fcbbd566`  
		Last Modified: Mon, 30 Mar 2026 17:33:24 GMT  
		Size: 8.6 KB (8598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:7b72b0b30b022c84693ba99bb4f9fe61e9cbef059b9ad9ffa86f078d483934f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8159328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a4c7f34d503a61c54d123884e376f53c1292fd8c64a836b3e9955539c98d76`

```dockerfile
```

-	Layers:
	-	`sha256:fcf157e6cb88191f05a038d7ad1fee7a645401eb74f68af6758cb94abef5f049`  
		Last Modified: Mon, 30 Mar 2026 17:33:24 GMT  
		Size: 8.1 MB (8147399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d390d05224faa3d7977494c904579b255840907f092d77922675463b1897d327`  
		Last Modified: Mon, 30 Mar 2026 17:33:23 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:d229b760db22a5348a778b6dc42749c160a9426990e413fd06484190c62f9a80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d9ed19bf543b46660be4cff8a23d54630fb5364ced64d1280c09eb9b05c5e9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268537672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8519ab0f23f7b3d466900bf4ffe097133f554841c91109dc57b66da0ddd395a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.version=20260329.0.507017
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.created=2026-03-29T00:10:46+00:00
# Mon, 30 Mar 2026 17:34:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 30 Mar 2026 17:34:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260329.0.507017' /etc/os-release # buildkit
# Mon, 30 Mar 2026 17:34:36 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:34:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a62fe7f33cbacca24085d9fba3b0371e6b6882ffb175eb3502dfa667f0865470`  
		Last Modified: Mon, 30 Mar 2026 17:35:28 GMT  
		Size: 268.5 MB (268527366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e6257934d9bebcd34e3ec6d04ea47b265b0d56e4172c1a49860b032064dc39`  
		Last Modified: Mon, 30 Mar 2026 17:35:22 GMT  
		Size: 10.3 KB (10306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:fdfb90122b0fc5c31dfd5871611d56a7f7dc3df54604a6f84a010ec5c56e4685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12213885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14fed52ee64392889cb4754c99c201948df326c85e307ace9460c661fbd2166`

```dockerfile
```

-	Layers:
	-	`sha256:041dcfa146c290350c97f715917c794b2671bc7eb52e02b14b5fd14b66a26e68`  
		Last Modified: Mon, 30 Mar 2026 17:35:23 GMT  
		Size: 12.2 MB (12202117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2489eaf24b91abbfffb910e9b3930bd47efb2990e48286979fcc5b62d721ae`  
		Last Modified: Mon, 30 Mar 2026 17:35:22 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260329.0.507017`

```console
$ docker pull archlinux@sha256:d229b760db22a5348a778b6dc42749c160a9426990e413fd06484190c62f9a80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260329.0.507017` - linux; amd64

```console
$ docker pull archlinux@sha256:d9ed19bf543b46660be4cff8a23d54630fb5364ced64d1280c09eb9b05c5e9ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268537672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8519ab0f23f7b3d466900bf4ffe097133f554841c91109dc57b66da0ddd395a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.version=20260329.0.507017
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 30 Mar 2026 17:34:30 GMT
LABEL org.opencontainers.image.created=2026-03-29T00:10:46+00:00
# Mon, 30 Mar 2026 17:34:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 30 Mar 2026 17:34:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260329.0.507017' /etc/os-release # buildkit
# Mon, 30 Mar 2026 17:34:36 GMT
ENV LANG=C.UTF-8
# Mon, 30 Mar 2026 17:34:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a62fe7f33cbacca24085d9fba3b0371e6b6882ffb175eb3502dfa667f0865470`  
		Last Modified: Mon, 30 Mar 2026 17:35:28 GMT  
		Size: 268.5 MB (268527366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e6257934d9bebcd34e3ec6d04ea47b265b0d56e4172c1a49860b032064dc39`  
		Last Modified: Mon, 30 Mar 2026 17:35:22 GMT  
		Size: 10.3 KB (10306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260329.0.507017` - unknown; unknown

```console
$ docker pull archlinux@sha256:fdfb90122b0fc5c31dfd5871611d56a7f7dc3df54604a6f84a010ec5c56e4685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12213885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14fed52ee64392889cb4754c99c201948df326c85e307ace9460c661fbd2166`

```dockerfile
```

-	Layers:
	-	`sha256:041dcfa146c290350c97f715917c794b2671bc7eb52e02b14b5fd14b66a26e68`  
		Last Modified: Mon, 30 Mar 2026 17:35:23 GMT  
		Size: 12.2 MB (12202117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2489eaf24b91abbfffb910e9b3930bd47efb2990e48286979fcc5b62d721ae`  
		Last Modified: Mon, 30 Mar 2026 17:35:22 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
