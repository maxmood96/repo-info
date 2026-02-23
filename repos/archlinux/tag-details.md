<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260222.0.493200`](#archlinuxbase-202602220493200)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260222.0.493200`](#archlinuxbase-devel-202602220493200)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260222.0.493200`](#archlinuxmultilib-devel-202602220493200)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:e25a13ea0e2a36df12f3593fe4bc1063605cfd2ab46c704f72c9e1c3514138ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:58a1cde0acb1a9fa847c5d829e0349ab76d6fb0893c47f3dad176d2cdf301ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128266383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453453af7a6f321d70c1d0855ce385fb1bbbc622b8213d7981bf205409e4f9de`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.version=20260215.0.490969
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.created=2026-02-15T00:06:54+00:00
# Tue, 17 Feb 2026 18:11:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Feb 2026 18:11:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260215.0.490969' /etc/os-release # buildkit
# Tue, 17 Feb 2026 18:11:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 18:11:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b2d9d946693ed5d2ad46777157e06c2ee1aa6270da5007dee549f429dc470ae1`  
		Last Modified: Tue, 17 Feb 2026 18:11:55 GMT  
		Size: 128.3 MB (128257808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad61ad26ec7862a5bde2fb078d78122d2fd61ea72bcff6fae75d4af471275894`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 8.6 KB (8575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:f3b95755139ca0c40f929333ad9e1d059ae51e97a10de774b712e5efb9848cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8471516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326176095077c0180d2d9fd7b86ae55d9c967fc6fb79db5f33e555cf1e698f78`

```dockerfile
```

-	Layers:
	-	`sha256:89840e3003f3914213acec748e5b71a6b0cb1686004af093d93b35dede08ecd5`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 8.5 MB (8459587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd221151afb6b3bf1abbccb5fc84852dc2f5d714e7bdfbddb3feb52aca5a061e`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260222.0.493200`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:839e930e2fa6d6f2e0b2005402c42c42b4e4be030337e0a311b17678b517f657
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8555624e8fd75d0a2e8f2f9a71f2c61b41501e41c5b07eb9cb0a3d1d7b630600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245813711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e946df517cb7ba7b9b11d514fc11b9bc55690008beb58122fca9645755b5c92`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.version=20260215.0.490969
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.created=2026-02-15T00:06:54+00:00
# Tue, 17 Feb 2026 18:12:46 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Feb 2026 18:12:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260215.0.490969' /etc/os-release # buildkit
# Tue, 17 Feb 2026 18:12:52 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 18:12:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d56ae5d19c1d2f04ea452d8de4fea13755b24651da53787d2422b538a07bb424`  
		Last Modified: Tue, 17 Feb 2026 18:13:38 GMT  
		Size: 245.8 MB (245804589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba4a8dca53d5f3f5abcab43ef7f312f7fba6c98c2708a39fc0e7d5d18986e9`  
		Last Modified: Tue, 17 Feb 2026 18:13:34 GMT  
		Size: 9.1 KB (9122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:6c220e5d999ed75e22dbedf1a3e40b399fd67b6449af7b7c0d5aeb79e8f5cb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12233626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e8461ab9fac244de925df5a0292fee96e0e5ecab8aa3514547366f7398600`

```dockerfile
```

-	Layers:
	-	`sha256:25ae73fffaac92346a92a6aaeb0b895e9104cb2a93cb6b547bfb6638fa7b0b44`  
		Last Modified: Tue, 17 Feb 2026 18:13:34 GMT  
		Size: 12.2 MB (12221916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31952edc35976610789df4f03c0745e06ff562c48ad555d009adc47327e08a5`  
		Last Modified: Tue, 17 Feb 2026 18:13:34 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260222.0.493200`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:e25a13ea0e2a36df12f3593fe4bc1063605cfd2ab46c704f72c9e1c3514138ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:58a1cde0acb1a9fa847c5d829e0349ab76d6fb0893c47f3dad176d2cdf301ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128266383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453453af7a6f321d70c1d0855ce385fb1bbbc622b8213d7981bf205409e4f9de`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.version=20260215.0.490969
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 17 Feb 2026 18:11:26 GMT
LABEL org.opencontainers.image.created=2026-02-15T00:06:54+00:00
# Tue, 17 Feb 2026 18:11:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Feb 2026 18:11:29 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260215.0.490969' /etc/os-release # buildkit
# Tue, 17 Feb 2026 18:11:29 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 18:11:29 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b2d9d946693ed5d2ad46777157e06c2ee1aa6270da5007dee549f429dc470ae1`  
		Last Modified: Tue, 17 Feb 2026 18:11:55 GMT  
		Size: 128.3 MB (128257808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad61ad26ec7862a5bde2fb078d78122d2fd61ea72bcff6fae75d4af471275894`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 8.6 KB (8575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:f3b95755139ca0c40f929333ad9e1d059ae51e97a10de774b712e5efb9848cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8471516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326176095077c0180d2d9fd7b86ae55d9c967fc6fb79db5f33e555cf1e698f78`

```dockerfile
```

-	Layers:
	-	`sha256:89840e3003f3914213acec748e5b71a6b0cb1686004af093d93b35dede08ecd5`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 8.5 MB (8459587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd221151afb6b3bf1abbccb5fc84852dc2f5d714e7bdfbddb3feb52aca5a061e`  
		Last Modified: Tue, 17 Feb 2026 18:11:52 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:f7c8aff548bd590bcf6c4b53e0d6dee711e6da52f4ee9e75959e195251e98637
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0a97b836b7baa8a78ac87d4c636f002fad5caf20c89f782c94e23aa742053948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267974118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08bd07a0428d372cd6129c0e386cc9389b24d011a12f0b1579d02ded0752ee4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.version=20260215.0.490969
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 17 Feb 2026 18:12:27 GMT
LABEL org.opencontainers.image.created=2026-02-15T00:06:54+00:00
# Tue, 17 Feb 2026 18:12:27 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Feb 2026 18:12:33 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260215.0.490969' /etc/os-release # buildkit
# Tue, 17 Feb 2026 18:12:33 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 18:12:33 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f5acad426fd0c8126c49ed2eee9bd51ed358460059421e9c596fad49547ffde9`  
		Last Modified: Tue, 17 Feb 2026 18:13:22 GMT  
		Size: 268.0 MB (267963820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e2adf10a195d94a1ae1215fbd8f09cc1bd0eb475a4c040015d8c0f969202a3`  
		Last Modified: Tue, 17 Feb 2026 18:13:16 GMT  
		Size: 10.3 KB (10298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bb73fb599efcf64181205e95c034e3afdb43175d4b133c66dc5e55247e696693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12503554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11ed0a1b2e5736033f663cba6f81d6494d8b92c4ff43ae72e737e7ffa52b132`

```dockerfile
```

-	Layers:
	-	`sha256:b48e8385a988ff8b589c4afac6ee025d1c7d36404cc90b62f8b08f382f765620`  
		Last Modified: Tue, 17 Feb 2026 18:13:17 GMT  
		Size: 12.5 MB (12491786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e684cb327c93a3da56d43647df9a4e2e1981bd6008fdcc6f1a229560184ecd0`  
		Last Modified: Tue, 17 Feb 2026 18:13:16 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260222.0.493200`

**does not exist** (yet?)
