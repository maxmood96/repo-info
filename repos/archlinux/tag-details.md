<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260111.0.480139`](#archlinuxbase-202601110480139)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260111.0.480139`](#archlinuxbase-devel-202601110480139)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260111.0.480139`](#archlinuxmultilib-devel-202601110480139)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:417aa2d3e8e4cc8377360a94bf48ae1ed38e593cbecfcb34feb16d57e3efa1b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:f63269aa09e82c18fe3066ba08d4e3e3ca0563aea84fbb85b7f65b317482c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176196185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ead43a9bf672282b8fd0b2a2c07466c68b91f3127f069671fc7e17ad9ff4a2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:41:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:41:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1783afd91fdd549adee0628532122581a17d849598d0cdbd9b23ae3b1cb1916e`  
		Last Modified: Mon, 12 Jan 2026 19:42:51 GMT  
		Size: 176.2 MB (176187405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d004c9cbdd7a9fb79180b6da2bccf91ade2e8cfb91669a192ac3d2825d13d`  
		Last Modified: Mon, 12 Jan 2026 19:42:43 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:fae8a207785da31c23883139edd4bfa54edcaa3f6305d94b77d17f204facc0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3f9c7390f6917ebf1a7679af233d24433cef1f6714c8ea7f4ee7adff54d70`

```dockerfile
```

-	Layers:
	-	`sha256:27231ef966bb178feb0db4f8b55bf7a45a91eb790a729d88034788c579cfa664`  
		Last Modified: Mon, 12 Jan 2026 20:48:18 GMT  
		Size: 8.4 MB (8398809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195204be3a072f4cbe86788d1502198815347f1ffe91d60e9a29134a8778ffa6`  
		Last Modified: Mon, 12 Jan 2026 20:48:19 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260111.0.480139`

```console
$ docker pull archlinux@sha256:417aa2d3e8e4cc8377360a94bf48ae1ed38e593cbecfcb34feb16d57e3efa1b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260111.0.480139` - linux; amd64

```console
$ docker pull archlinux@sha256:f63269aa09e82c18fe3066ba08d4e3e3ca0563aea84fbb85b7f65b317482c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176196185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ead43a9bf672282b8fd0b2a2c07466c68b91f3127f069671fc7e17ad9ff4a2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:41:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:41:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1783afd91fdd549adee0628532122581a17d849598d0cdbd9b23ae3b1cb1916e`  
		Last Modified: Mon, 12 Jan 2026 19:42:51 GMT  
		Size: 176.2 MB (176187405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d004c9cbdd7a9fb79180b6da2bccf91ade2e8cfb91669a192ac3d2825d13d`  
		Last Modified: Mon, 12 Jan 2026 19:42:43 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260111.0.480139` - unknown; unknown

```console
$ docker pull archlinux@sha256:fae8a207785da31c23883139edd4bfa54edcaa3f6305d94b77d17f204facc0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3f9c7390f6917ebf1a7679af233d24433cef1f6714c8ea7f4ee7adff54d70`

```dockerfile
```

-	Layers:
	-	`sha256:27231ef966bb178feb0db4f8b55bf7a45a91eb790a729d88034788c579cfa664`  
		Last Modified: Mon, 12 Jan 2026 20:48:18 GMT  
		Size: 8.4 MB (8398809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195204be3a072f4cbe86788d1502198815347f1ffe91d60e9a29134a8778ffa6`  
		Last Modified: Mon, 12 Jan 2026 20:48:19 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:84c36fa73fc692775e6b99de0d6a10967005b459ef170fc4faea426673b5e7b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:bb59138e0f1735a5c4449c39cc0d72ea7592beb3fdc46b8166538e5b326ef4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293731041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1512daf7f17af1c7641bacad417e4cc12edcc901c32891b39d8e0f5dc524bb4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:43:02 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:43:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:43:09 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:43:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cc32ee06ac77e6731f18c764c2e72a887ff547d69de10ec09dda33ed3f0eefc6`  
		Last Modified: Mon, 12 Jan 2026 19:43:58 GMT  
		Size: 293.7 MB (293721693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e569b708c9698e5117c1d999863a141d95f2b0b0538f21711097755c00ec120`  
		Last Modified: Mon, 12 Jan 2026 19:43:52 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:57f28034d876181e06208e27d98e61b1cb5378c2b876757d88a5ff5af98ff8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89818d2877e388bfe99270ac7912ba87ff3cc1e86b5ff6fdb4b536e795d620fd`

```dockerfile
```

-	Layers:
	-	`sha256:9316ce4f66cb865108f677a609fffd32e148844e06bf6db744466aea30322db5`  
		Last Modified: Mon, 12 Jan 2026 19:43:53 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090dcb99cca41d0874b08a89776bf6cf00ede46ddbeb24da8ee5536acb48df8b`  
		Last Modified: Mon, 12 Jan 2026 20:48:25 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260111.0.480139`

```console
$ docker pull archlinux@sha256:84c36fa73fc692775e6b99de0d6a10967005b459ef170fc4faea426673b5e7b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260111.0.480139` - linux; amd64

```console
$ docker pull archlinux@sha256:bb59138e0f1735a5c4449c39cc0d72ea7592beb3fdc46b8166538e5b326ef4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293731041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1512daf7f17af1c7641bacad417e4cc12edcc901c32891b39d8e0f5dc524bb4`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:43:02 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:43:02 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:43:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:43:09 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:43:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cc32ee06ac77e6731f18c764c2e72a887ff547d69de10ec09dda33ed3f0eefc6`  
		Last Modified: Mon, 12 Jan 2026 19:43:58 GMT  
		Size: 293.7 MB (293721693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e569b708c9698e5117c1d999863a141d95f2b0b0538f21711097755c00ec120`  
		Last Modified: Mon, 12 Jan 2026 19:43:52 GMT  
		Size: 9.3 KB (9348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260111.0.480139` - unknown; unknown

```console
$ docker pull archlinux@sha256:57f28034d876181e06208e27d98e61b1cb5378c2b876757d88a5ff5af98ff8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89818d2877e388bfe99270ac7912ba87ff3cc1e86b5ff6fdb4b536e795d620fd`

```dockerfile
```

-	Layers:
	-	`sha256:9316ce4f66cb865108f677a609fffd32e148844e06bf6db744466aea30322db5`  
		Last Modified: Mon, 12 Jan 2026 19:43:53 GMT  
		Size: 12.2 MB (12161144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:090dcb99cca41d0874b08a89776bf6cf00ede46ddbeb24da8ee5536acb48df8b`  
		Last Modified: Mon, 12 Jan 2026 20:48:25 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:417aa2d3e8e4cc8377360a94bf48ae1ed38e593cbecfcb34feb16d57e3efa1b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:f63269aa09e82c18fe3066ba08d4e3e3ca0563aea84fbb85b7f65b317482c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176196185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ead43a9bf672282b8fd0b2a2c07466c68b91f3127f069671fc7e17ad9ff4a2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:41:46 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:41:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:41:50 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:41:50 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1783afd91fdd549adee0628532122581a17d849598d0cdbd9b23ae3b1cb1916e`  
		Last Modified: Mon, 12 Jan 2026 19:42:51 GMT  
		Size: 176.2 MB (176187405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786d004c9cbdd7a9fb79180b6da2bccf91ade2e8cfb91669a192ac3d2825d13d`  
		Last Modified: Mon, 12 Jan 2026 19:42:43 GMT  
		Size: 8.8 KB (8780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:fae8a207785da31c23883139edd4bfa54edcaa3f6305d94b77d17f204facc0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea3f9c7390f6917ebf1a7679af233d24433cef1f6714c8ea7f4ee7adff54d70`

```dockerfile
```

-	Layers:
	-	`sha256:27231ef966bb178feb0db4f8b55bf7a45a91eb790a729d88034788c579cfa664`  
		Last Modified: Mon, 12 Jan 2026 20:48:18 GMT  
		Size: 8.4 MB (8398809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195204be3a072f4cbe86788d1502198815347f1ffe91d60e9a29134a8778ffa6`  
		Last Modified: Mon, 12 Jan 2026 20:48:19 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9323d3b3c7820c46482b0bb6e923de50c6c57559c6b24da2fba20080e38ec756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:86480447275383bee14322c6cd282de8077c14ba012d9cebc3a036f380c4835f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (345049834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ddc12e4505f7caae20b2c36fe036f533d21a79bb0a56dabcb3cd3795003cdf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:43:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:43:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:43:20 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:43:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:493685d34efc1b3b976004964157c27a3d5de3f6b952a5fd469441213132444e`  
		Last Modified: Mon, 12 Jan 2026 19:45:46 GMT  
		Size: 345.0 MB (345039388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec5dba24b86b8db48c9e22afb803190afd87c8c62598a7d8666417400dfaa5`  
		Last Modified: Mon, 12 Jan 2026 19:44:22 GMT  
		Size: 10.4 KB (10446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0231aba07e41078e2bf076ffae7128bd2e0fe6c743cb106f51ae54dcc84c7a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12441705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7ca0862b02cf40fb5dace81e3b0b79702f7d0dcef76168c30ee13929f4a71d`

```dockerfile
```

-	Layers:
	-	`sha256:dd9b612d05efa0c7fc376d50fc4d9cdd1eb36d9581c83b433f619bd38068b400`  
		Last Modified: Mon, 12 Jan 2026 20:48:31 GMT  
		Size: 12.4 MB (12429937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32410d291a859c1a18167d95dc899ab3e1f80aa649da27a260b3e839db719f39`  
		Last Modified: Mon, 12 Jan 2026 20:48:32 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260111.0.480139`

```console
$ docker pull archlinux@sha256:9323d3b3c7820c46482b0bb6e923de50c6c57559c6b24da2fba20080e38ec756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260111.0.480139` - linux; amd64

```console
$ docker pull archlinux@sha256:86480447275383bee14322c6cd282de8077c14ba012d9cebc3a036f380c4835f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (345049834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ddc12e4505f7caae20b2c36fe036f533d21a79bb0a56dabcb3cd3795003cdf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:43:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:43:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:43:20 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:43:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:493685d34efc1b3b976004964157c27a3d5de3f6b952a5fd469441213132444e`  
		Last Modified: Mon, 12 Jan 2026 19:45:46 GMT  
		Size: 345.0 MB (345039388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec5dba24b86b8db48c9e22afb803190afd87c8c62598a7d8666417400dfaa5`  
		Last Modified: Mon, 12 Jan 2026 19:44:22 GMT  
		Size: 10.4 KB (10446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260111.0.480139` - unknown; unknown

```console
$ docker pull archlinux@sha256:0231aba07e41078e2bf076ffae7128bd2e0fe6c743cb106f51ae54dcc84c7a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12441705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7ca0862b02cf40fb5dace81e3b0b79702f7d0dcef76168c30ee13929f4a71d`

```dockerfile
```

-	Layers:
	-	`sha256:dd9b612d05efa0c7fc376d50fc4d9cdd1eb36d9581c83b433f619bd38068b400`  
		Last Modified: Mon, 12 Jan 2026 20:48:31 GMT  
		Size: 12.4 MB (12429937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32410d291a859c1a18167d95dc899ab3e1f80aa649da27a260b3e839db719f39`  
		Last Modified: Mon, 12 Jan 2026 20:48:32 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
