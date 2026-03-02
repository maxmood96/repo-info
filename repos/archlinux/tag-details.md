<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260301.0.494762`](#archlinuxbase-202603010494762)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260301.0.494762`](#archlinuxbase-devel-202603010494762)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260301.0.494762`](#archlinuxmultilib-devel-202603010494762)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:6417af93a50740f2c88503b098e780c9edf5ee00aa156021c28bcfffe226f57d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:32ef0b1658af994e1a9be54043970c161c5b8ff2be057687bdb73a7e00fa9f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128328916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f1bdc4343b235a9f79259a7cfe88dd5013999144cbb2d88f329dc548b5b653`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:12:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:12:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:30309458937ad265aaf28267249ee4c81fb36b01436042e1db699fbd376aae51`  
		Last Modified: Mon, 02 Mar 2026 19:12:36 GMT  
		Size: 128.3 MB (128320326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec592b6ce77ee4468ee080ecd79e1bc2f27389cb69b2c80752a7fd8080fc86`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 8.6 KB (8590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:186b9184d0d19d1a05967aa36da7d77d883c0b953fddfec571e2e7332b636d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8488859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d84ac9548c5ce774ad930f5e4c4d83b81f524654787834005b985690e0a997`

```dockerfile
```

-	Layers:
	-	`sha256:09304ff833801dc2643fd2617438e4e3143ae559b89f4e018972ce135a0fc764`  
		Last Modified: Mon, 02 Mar 2026 19:12:31 GMT  
		Size: 8.5 MB (8476930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdcaf245f3775c930a42adf12c7f7dcb9b7384e41bcb134483417d3fcebd1d9`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20260301.0.494762`

```console
$ docker pull archlinux@sha256:6417af93a50740f2c88503b098e780c9edf5ee00aa156021c28bcfffe226f57d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20260301.0.494762` - linux; amd64

```console
$ docker pull archlinux@sha256:32ef0b1658af994e1a9be54043970c161c5b8ff2be057687bdb73a7e00fa9f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128328916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f1bdc4343b235a9f79259a7cfe88dd5013999144cbb2d88f329dc548b5b653`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:12:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:12:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:30309458937ad265aaf28267249ee4c81fb36b01436042e1db699fbd376aae51`  
		Last Modified: Mon, 02 Mar 2026 19:12:36 GMT  
		Size: 128.3 MB (128320326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec592b6ce77ee4468ee080ecd79e1bc2f27389cb69b2c80752a7fd8080fc86`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 8.6 KB (8590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20260301.0.494762` - unknown; unknown

```console
$ docker pull archlinux@sha256:186b9184d0d19d1a05967aa36da7d77d883c0b953fddfec571e2e7332b636d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8488859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d84ac9548c5ce774ad930f5e4c4d83b81f524654787834005b985690e0a997`

```dockerfile
```

-	Layers:
	-	`sha256:09304ff833801dc2643fd2617438e4e3143ae559b89f4e018972ce135a0fc764`  
		Last Modified: Mon, 02 Mar 2026 19:12:31 GMT  
		Size: 8.5 MB (8476930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdcaf245f3775c930a42adf12c7f7dcb9b7384e41bcb134483417d3fcebd1d9`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:a4e49d3505c6bad5909d292ef31ae7599aa58c1468c5d407883507d7d77ce3b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:799c4c5935baaf7b4ca1ec216e55146dac5720c1de2e07608516c80f0c9206a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245924827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f0b7e135cf3b829df5466b5a0bd5ad6259b5b28a83776bbec12213a5863df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:13:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:13:19 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:13:19 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:13:19 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6d6e1ae42c059c45ffaf68544ea82d0b0ce2d8144da1734b551558eea33f3f4b`  
		Last Modified: Mon, 02 Mar 2026 19:14:02 GMT  
		Size: 245.9 MB (245915716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb94e2ef0f05673e841bb09b9c44d613bb9129d050bb58a399b988ec8e27ae1`  
		Last Modified: Mon, 02 Mar 2026 19:13:55 GMT  
		Size: 9.1 KB (9111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:17f7060aecc3e49017def05fc8406cd2a6db9d626ce614f19e3169eddc86919e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12250998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2fb327b75f9b5671e075f3b04ea3eee5c782ef68293bf26313bbff29bccb9a`

```dockerfile
```

-	Layers:
	-	`sha256:26eeb41ae39a9d0e42562a20eada6d5cf78ca5779955058c90d4a17a1da7823f`  
		Last Modified: Mon, 02 Mar 2026 19:13:56 GMT  
		Size: 12.2 MB (12239289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539c61b08285f85d9262884cc0464f287219f12f07bd7c9bf62687c3dc4b49f9`  
		Last Modified: Mon, 02 Mar 2026 19:13:55 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260301.0.494762`

```console
$ docker pull archlinux@sha256:a4e49d3505c6bad5909d292ef31ae7599aa58c1468c5d407883507d7d77ce3b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260301.0.494762` - linux; amd64

```console
$ docker pull archlinux@sha256:799c4c5935baaf7b4ca1ec216e55146dac5720c1de2e07608516c80f0c9206a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245924827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f0b7e135cf3b829df5466b5a0bd5ad6259b5b28a83776bbec12213a5863df`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:13:13 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:13:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:13:19 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:13:19 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:13:19 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6d6e1ae42c059c45ffaf68544ea82d0b0ce2d8144da1734b551558eea33f3f4b`  
		Last Modified: Mon, 02 Mar 2026 19:14:02 GMT  
		Size: 245.9 MB (245915716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb94e2ef0f05673e841bb09b9c44d613bb9129d050bb58a399b988ec8e27ae1`  
		Last Modified: Mon, 02 Mar 2026 19:13:55 GMT  
		Size: 9.1 KB (9111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260301.0.494762` - unknown; unknown

```console
$ docker pull archlinux@sha256:17f7060aecc3e49017def05fc8406cd2a6db9d626ce614f19e3169eddc86919e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12250998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2fb327b75f9b5671e075f3b04ea3eee5c782ef68293bf26313bbff29bccb9a`

```dockerfile
```

-	Layers:
	-	`sha256:26eeb41ae39a9d0e42562a20eada6d5cf78ca5779955058c90d4a17a1da7823f`  
		Last Modified: Mon, 02 Mar 2026 19:13:56 GMT  
		Size: 12.2 MB (12239289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539c61b08285f85d9262884cc0464f287219f12f07bd7c9bf62687c3dc4b49f9`  
		Last Modified: Mon, 02 Mar 2026 19:13:55 GMT  
		Size: 11.7 KB (11709 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:6417af93a50740f2c88503b098e780c9edf5ee00aa156021c28bcfffe226f57d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:32ef0b1658af994e1a9be54043970c161c5b8ff2be057687bdb73a7e00fa9f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128328916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f1bdc4343b235a9f79259a7cfe88dd5013999144cbb2d88f329dc548b5b653`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:12:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:12:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:30309458937ad265aaf28267249ee4c81fb36b01436042e1db699fbd376aae51`  
		Last Modified: Mon, 02 Mar 2026 19:12:36 GMT  
		Size: 128.3 MB (128320326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec592b6ce77ee4468ee080ecd79e1bc2f27389cb69b2c80752a7fd8080fc86`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 8.6 KB (8590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:186b9184d0d19d1a05967aa36da7d77d883c0b953fddfec571e2e7332b636d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8488859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d84ac9548c5ce774ad930f5e4c4d83b81f524654787834005b985690e0a997`

```dockerfile
```

-	Layers:
	-	`sha256:09304ff833801dc2643fd2617438e4e3143ae559b89f4e018972ce135a0fc764`  
		Last Modified: Mon, 02 Mar 2026 19:12:31 GMT  
		Size: 8.5 MB (8476930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdcaf245f3775c930a42adf12c7f7dcb9b7384e41bcb134483417d3fcebd1d9`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:20ac0dba3c5282241f7703467533357379f56160d8d3e682c09115675c8e0493
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c84b6ac73dc84aaf21d13e6081b2bd84fffb7d926b9682ab1d101d3afe0a4df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268087964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf7fcd005a84c65d46fd0648d9705ae334ab7abebfae39785ad51a30ee5b7e1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:13:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:13:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:13:12 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:13:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8c764f1514a66c73f29af53aaf52d5a38e20996ec1ad72fa0c732d08486ac2fb`  
		Last Modified: Mon, 02 Mar 2026 19:13:59 GMT  
		Size: 268.1 MB (268077638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b339c3bbac1bb41286ebb0486af34c2333afecbebc5998d81f90cdf7bb5846`  
		Last Modified: Mon, 02 Mar 2026 19:13:53 GMT  
		Size: 10.3 KB (10326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d1cfb9d9984c251cb56556fa82a087255821a7c5ebf24eb14ef74de3ea912ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12520926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d109be139ec9b0f8830309ffc5781c6d9416ebc602a02e41cc91cade6752699e`

```dockerfile
```

-	Layers:
	-	`sha256:b3105912f0b710d34ede0d4f3b7ecd0d8058497e528861e68e0f9fc43b35fb84`  
		Last Modified: Mon, 02 Mar 2026 19:13:54 GMT  
		Size: 12.5 MB (12509159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1751276bc1904666d9615e22dc7e3a792fe85be43d05a3cd3eeec837c816152`  
		Last Modified: Mon, 02 Mar 2026 19:13:53 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260301.0.494762`

```console
$ docker pull archlinux@sha256:20ac0dba3c5282241f7703467533357379f56160d8d3e682c09115675c8e0493
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260301.0.494762` - linux; amd64

```console
$ docker pull archlinux@sha256:c84b6ac73dc84aaf21d13e6081b2bd84fffb7d926b9682ab1d101d3afe0a4df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268087964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf7fcd005a84c65d46fd0648d9705ae334ab7abebfae39785ad51a30ee5b7e1`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:13:06 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:13:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:13:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:13:12 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:13:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8c764f1514a66c73f29af53aaf52d5a38e20996ec1ad72fa0c732d08486ac2fb`  
		Last Modified: Mon, 02 Mar 2026 19:13:59 GMT  
		Size: 268.1 MB (268077638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b339c3bbac1bb41286ebb0486af34c2333afecbebc5998d81f90cdf7bb5846`  
		Last Modified: Mon, 02 Mar 2026 19:13:53 GMT  
		Size: 10.3 KB (10326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260301.0.494762` - unknown; unknown

```console
$ docker pull archlinux@sha256:3d1cfb9d9984c251cb56556fa82a087255821a7c5ebf24eb14ef74de3ea912ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12520926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d109be139ec9b0f8830309ffc5781c6d9416ebc602a02e41cc91cade6752699e`

```dockerfile
```

-	Layers:
	-	`sha256:b3105912f0b710d34ede0d4f3b7ecd0d8058497e528861e68e0f9fc43b35fb84`  
		Last Modified: Mon, 02 Mar 2026 19:13:54 GMT  
		Size: 12.5 MB (12509159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1751276bc1904666d9615e22dc7e3a792fe85be43d05a3cd3eeec837c816152`  
		Last Modified: Mon, 02 Mar 2026 19:13:53 GMT  
		Size: 11.8 KB (11767 bytes)  
		MIME: application/vnd.in-toto+json
