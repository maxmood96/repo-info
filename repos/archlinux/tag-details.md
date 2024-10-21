<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241020.0.271562`](#archlinuxbase-202410200271562)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241020.0.271562`](#archlinuxbase-devel-202410200271562)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241020.0.271562`](#archlinuxmultilib-devel-202410200271562)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:36e14d971d587c5cc7e2c832bd8789b27cabfd75e0be8e4f79bc162468c5043b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:5c3fb7b417945a3d6ff506f5d8764385956d629ad37b480ed3416240ae54b2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151205810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e84141a99956b46bb2f3a1adeeffaaebbb5a2e1d2779b501c87453abd62a63`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.version=20241013.0.269705
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.created=2024-10-13T00:07:34+00:00
# Sun, 13 Oct 2024 00:07:34 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241013.0.269705' /etc/os-release # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
ENV LANG=C.UTF-8
# Sun, 13 Oct 2024 00:07:34 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9de125b2003639366eb85bf6b0a340229a9b2be0a2efda65f3abd97be902d88`  
		Last Modified: Mon, 14 Oct 2024 16:57:58 GMT  
		Size: 151.2 MB (151197584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0a06a02c96571f8b86f75e0eed3087a35d16edbeb7d30381616407009b1fc`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:4c02f4ffb27e355e1d8f773fb2b46d0e8973f71ac155aea3074b2b9f160ca9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c96c8fb166dba210683a94477cf8b404d8efa1d8ded09034e8b307d8299d21f`

```dockerfile
```

-	Layers:
	-	`sha256:f15845601f16bf05c20abd228626ea0e99da93c5db5602b10cfaf28f5a58219c`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 8.1 MB (8102276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629057bec6b0b13bb93048c0cdeba5f187d5a2f660360f65b542e6eda13fa75f`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241020.0.271562`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:291198370afb8645d8341adfc354a407c0f981fd66a3bd89a267080db05314c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:cf078f3ed4c05215655cf546ec9baf1a722c956dc615a83afb9504ba5f2de2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272207868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fef481d84240d74d79f1bf7ff90814f04d3e3014a28672e8236941292a858f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.version=20241013.0.269705
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.created=2024-10-13T00:07:34+00:00
# Sun, 13 Oct 2024 00:07:34 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241013.0.269705' /etc/os-release # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
ENV LANG=C.UTF-8
# Sun, 13 Oct 2024 00:07:34 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e76fd01d88ac44554cbddc68bc825ded8ae4866aeb8709765151c2b9cdfc95d4`  
		Last Modified: Mon, 14 Oct 2024 16:58:37 GMT  
		Size: 272.2 MB (272198866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea70b41381990070a0d797c943fd2e654e382d1223d9fb0a7ba106397286a3b`  
		Last Modified: Mon, 14 Oct 2024 16:58:33 GMT  
		Size: 9.0 KB (9002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ab2c1268d29e0112e8915372c25861e5a230ff20078666b0f152ed03611f67fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e29df3c2a92e91668ba098d2fab29e941a330b354ab048a70b2c41f1c888ff`

```dockerfile
```

-	Layers:
	-	`sha256:1b2b3499eb47cff39b43b50198c0873f43e8566eaa3599661471616ac845991c`  
		Last Modified: Mon, 14 Oct 2024 16:58:33 GMT  
		Size: 11.9 MB (11900567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6efa016cc5092fcd316db4ebb0bbdb0b5b3bd0404d7f0fa71f8fb109cf0e228f`  
		Last Modified: Mon, 14 Oct 2024 16:58:33 GMT  
		Size: 11.5 KB (11541 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241020.0.271562`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:36e14d971d587c5cc7e2c832bd8789b27cabfd75e0be8e4f79bc162468c5043b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:5c3fb7b417945a3d6ff506f5d8764385956d629ad37b480ed3416240ae54b2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151205810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e84141a99956b46bb2f3a1adeeffaaebbb5a2e1d2779b501c87453abd62a63`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.version=20241013.0.269705
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.created=2024-10-13T00:07:34+00:00
# Sun, 13 Oct 2024 00:07:34 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241013.0.269705' /etc/os-release # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
ENV LANG=C.UTF-8
# Sun, 13 Oct 2024 00:07:34 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9de125b2003639366eb85bf6b0a340229a9b2be0a2efda65f3abd97be902d88`  
		Last Modified: Mon, 14 Oct 2024 16:57:58 GMT  
		Size: 151.2 MB (151197584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f0a06a02c96571f8b86f75e0eed3087a35d16edbeb7d30381616407009b1fc`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:4c02f4ffb27e355e1d8f773fb2b46d0e8973f71ac155aea3074b2b9f160ca9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c96c8fb166dba210683a94477cf8b404d8efa1d8ded09034e8b307d8299d21f`

```dockerfile
```

-	Layers:
	-	`sha256:f15845601f16bf05c20abd228626ea0e99da93c5db5602b10cfaf28f5a58219c`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 8.1 MB (8102276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629057bec6b0b13bb93048c0cdeba5f187d5a2f660360f65b542e6eda13fa75f`  
		Last Modified: Mon, 14 Oct 2024 16:57:56 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:bc7b145c837776bc29c499b8fd55b9e229c73f1a118701ff33a4a1f74105f839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:fa32ba9229770ff04b16774dec4d48906430c77116c36416b9056a39df728e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322061544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54daaf80f03e696bc16603bfa8cf8b50974634cc454461ff7d1c73a1eec227a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.version=20241013.0.269705
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 13 Oct 2024 00:07:34 GMT
LABEL org.opencontainers.image.created=2024-10-13T00:07:34+00:00
# Sun, 13 Oct 2024 00:07:34 GMT
COPY /rootfs/ / # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241013.0.269705' /etc/os-release # buildkit
# Sun, 13 Oct 2024 00:07:34 GMT
ENV LANG=C.UTF-8
# Sun, 13 Oct 2024 00:07:34 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e8bac2ec1e9ac3fc4345cd625a0d59da834a50b49e726689c348241a2c6f19a6`  
		Last Modified: Mon, 14 Oct 2024 16:58:57 GMT  
		Size: 322.1 MB (322051434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4da072a877bc0e32c51ab1f51eacc501c455982eefa3f37dd4626e7026f20bb`  
		Last Modified: Mon, 14 Oct 2024 16:58:49 GMT  
		Size: 10.1 KB (10110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:1d4f238f382dfce03e6d8922fd1db3798938b6b03a9ca5c27b85c85e25095a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3e1afcd0d17101f0e6764407b345358d84cbdc49a02ee0475bc7e09a675d35`

```dockerfile
```

-	Layers:
	-	`sha256:b8d0e62991372c675f0518d6f49053ee8298e00ccf68d7103f4d82c932e70a19`  
		Last Modified: Mon, 14 Oct 2024 16:58:49 GMT  
		Size: 12.2 MB (12167879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e3ef50435a2011438c3c14cbb0220f599fbe105ed679c71cb3cf695fecde173`  
		Last Modified: Mon, 14 Oct 2024 16:58:49 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241020.0.271562`

**does not exist** (yet?)
