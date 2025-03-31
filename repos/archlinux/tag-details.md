<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250330.0.328921`](#archlinuxbase-202503300328921)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250330.0.328921`](#archlinuxbase-devel-202503300328921)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250330.0.328921`](#archlinuxmultilib-devel-202503300328921)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:b831611bfe7692138a4020e8ec98758584ba2d7a169532384df15c6c7d79a17b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:fb9b13c74cc68f6f81f6b6e68c3972839669df11245d184b1ce501d16dd29930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159344799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad26a34398795b32f3c0f16443adb4c104daa54a716275785c59e097ce82151`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cfd45e302a03f3117f34ed7aac1950ec5b3aa9da2ba8554dac2271904f4f25c1`  
		Last Modified: Mon, 31 Mar 2025 16:34:36 GMT  
		Size: 159.3 MB (159336453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796f1e3132fbf65c54538393ba07f586a79f2a9da37edd20a024acae632f62f1`  
		Last Modified: Mon, 31 Mar 2025 16:34:31 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:b8435c55d9c3c0f54aa11835fc68391fa5468c8c40c4e270b4b86a2847bb13aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8173667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32caad8aa0d5ce818a53574eaf1163c73bdfa8c3f0f51287e45ffbf4835650df`

```dockerfile
```

-	Layers:
	-	`sha256:07c95dc86680272fd5f8ed29fae4205a521e5a01cfa67b74076a1dc030309094`  
		Last Modified: Mon, 31 Mar 2025 16:34:32 GMT  
		Size: 8.2 MB (8161695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d66108bb31eee67d0f6b3a8a74b71a0cb0469d273353bd668cee7d7b6d94d88`  
		Last Modified: Mon, 31 Mar 2025 16:34:31 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250330.0.328921`

```console
$ docker pull archlinux@sha256:b831611bfe7692138a4020e8ec98758584ba2d7a169532384df15c6c7d79a17b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250330.0.328921` - linux; amd64

```console
$ docker pull archlinux@sha256:fb9b13c74cc68f6f81f6b6e68c3972839669df11245d184b1ce501d16dd29930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159344799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad26a34398795b32f3c0f16443adb4c104daa54a716275785c59e097ce82151`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cfd45e302a03f3117f34ed7aac1950ec5b3aa9da2ba8554dac2271904f4f25c1`  
		Last Modified: Mon, 31 Mar 2025 16:34:36 GMT  
		Size: 159.3 MB (159336453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796f1e3132fbf65c54538393ba07f586a79f2a9da37edd20a024acae632f62f1`  
		Last Modified: Mon, 31 Mar 2025 16:34:31 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250330.0.328921` - unknown; unknown

```console
$ docker pull archlinux@sha256:b8435c55d9c3c0f54aa11835fc68391fa5468c8c40c4e270b4b86a2847bb13aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8173667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32caad8aa0d5ce818a53574eaf1163c73bdfa8c3f0f51287e45ffbf4835650df`

```dockerfile
```

-	Layers:
	-	`sha256:07c95dc86680272fd5f8ed29fae4205a521e5a01cfa67b74076a1dc030309094`  
		Last Modified: Mon, 31 Mar 2025 16:34:32 GMT  
		Size: 8.2 MB (8161695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d66108bb31eee67d0f6b3a8a74b71a0cb0469d273353bd668cee7d7b6d94d88`  
		Last Modified: Mon, 31 Mar 2025 16:34:31 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:11438acf52972a505eda9c9b588c1ee04f27186277aec15ef7f283ef6222c311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4d1b7a09932104456e96c77bb56c58616622f2503708d5a4d73e42a5850f1655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280831909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24c16ed9b3ebf03730a7f060c7cc0216fd1875ce3dec10621831f7f27a4393a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cb85c779ffeab5ed3bbaebb5b6d366ab27015ebf1161cba4c455902e74762905`  
		Last Modified: Mon, 31 Mar 2025 16:34:50 GMT  
		Size: 280.8 MB (280822858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361baea604e9e076887982734dd8196267555b7698a6d432c416b1a67cda5f20`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 9.1 KB (9051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4d4fbcbbdb2b6cacf0ac781b444d01d1d291c10422e704bd2e249c307e3bf727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11993871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed5f53b5f5e8ecd52564ff8581f1e6f8fe9ff50a2f9446fd15cf710b69da997`

```dockerfile
```

-	Layers:
	-	`sha256:8269457670b8542712582dde59edd256e5ee494e1a7d40dee68da80cb29bb00c`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 12.0 MB (11982117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4cd0ea4e5d469967ac6a07ba682820003b266837de94206a0f27024e9087a4`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250330.0.328921`

```console
$ docker pull archlinux@sha256:11438acf52972a505eda9c9b588c1ee04f27186277aec15ef7f283ef6222c311
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250330.0.328921` - linux; amd64

```console
$ docker pull archlinux@sha256:4d1b7a09932104456e96c77bb56c58616622f2503708d5a4d73e42a5850f1655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280831909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24c16ed9b3ebf03730a7f060c7cc0216fd1875ce3dec10621831f7f27a4393a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cb85c779ffeab5ed3bbaebb5b6d366ab27015ebf1161cba4c455902e74762905`  
		Last Modified: Mon, 31 Mar 2025 16:34:50 GMT  
		Size: 280.8 MB (280822858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361baea604e9e076887982734dd8196267555b7698a6d432c416b1a67cda5f20`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 9.1 KB (9051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250330.0.328921` - unknown; unknown

```console
$ docker pull archlinux@sha256:4d4fbcbbdb2b6cacf0ac781b444d01d1d291c10422e704bd2e249c307e3bf727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11993871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed5f53b5f5e8ecd52564ff8581f1e6f8fe9ff50a2f9446fd15cf710b69da997`

```dockerfile
```

-	Layers:
	-	`sha256:8269457670b8542712582dde59edd256e5ee494e1a7d40dee68da80cb29bb00c`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 12.0 MB (11982117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f4cd0ea4e5d469967ac6a07ba682820003b266837de94206a0f27024e9087a4`  
		Last Modified: Mon, 31 Mar 2025 16:34:46 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:b831611bfe7692138a4020e8ec98758584ba2d7a169532384df15c6c7d79a17b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:fb9b13c74cc68f6f81f6b6e68c3972839669df11245d184b1ce501d16dd29930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159344799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad26a34398795b32f3c0f16443adb4c104daa54a716275785c59e097ce82151`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cfd45e302a03f3117f34ed7aac1950ec5b3aa9da2ba8554dac2271904f4f25c1`  
		Last Modified: Mon, 31 Mar 2025 16:34:36 GMT  
		Size: 159.3 MB (159336453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796f1e3132fbf65c54538393ba07f586a79f2a9da37edd20a024acae632f62f1`  
		Last Modified: Mon, 31 Mar 2025 16:34:31 GMT  
		Size: 8.3 KB (8346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:b8435c55d9c3c0f54aa11835fc68391fa5468c8c40c4e270b4b86a2847bb13aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8173667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32caad8aa0d5ce818a53574eaf1163c73bdfa8c3f0f51287e45ffbf4835650df`

```dockerfile
```

-	Layers:
	-	`sha256:07c95dc86680272fd5f8ed29fae4205a521e5a01cfa67b74076a1dc030309094`  
		Last Modified: Mon, 31 Mar 2025 16:34:32 GMT  
		Size: 8.2 MB (8161695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d66108bb31eee67d0f6b3a8a74b71a0cb0469d273353bd668cee7d7b6d94d88`  
		Last Modified: Mon, 31 Mar 2025 16:34:31 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:c173b8e612164227dc475cad83e9e126938925e6e4ce89ec9ccc2a8a117c8288
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:9d637ee873ac25906ef22dfb5bf3832adbeec8998c786b8fc18227b593547aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330834610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32bf15ddf39ce2ecb3d3e153874f44851505506cf57506316ec19ba7eb24c7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad34537c3749262aa4117f2f3c7acbd59db0eced0a6efee1cdba55032a967b0e`  
		Last Modified: Mon, 31 Mar 2025 16:35:15 GMT  
		Size: 330.8 MB (330824353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cdf2da152fe4648b2bfb5f57eb0fdce85b8fabb9b153f5a67f3fe5b292366f`  
		Last Modified: Mon, 31 Mar 2025 16:35:07 GMT  
		Size: 10.3 KB (10257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:87ebf1488c6902a4bbfe2567053ac58f7d7437a1d085b4a819e1402abfd0e6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12262463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f1bd9df030ad99b19aec22187fb2c00b76fd4a60916de6485392d5172038e2`

```dockerfile
```

-	Layers:
	-	`sha256:c1bd5878d4df9fe2426591610e1e64791efc50249a36114b2b85e054e45f0dcd`  
		Last Modified: Mon, 31 Mar 2025 16:35:08 GMT  
		Size: 12.3 MB (12250652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a891cbe827c9043a292ac6b68b0833c420170a44e75ab68364d2668954fa20c3`  
		Last Modified: Mon, 31 Mar 2025 16:35:07 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250330.0.328921`

```console
$ docker pull archlinux@sha256:c173b8e612164227dc475cad83e9e126938925e6e4ce89ec9ccc2a8a117c8288
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250330.0.328921` - linux; amd64

```console
$ docker pull archlinux@sha256:9d637ee873ac25906ef22dfb5bf3832adbeec8998c786b8fc18227b593547aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330834610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32bf15ddf39ce2ecb3d3e153874f44851505506cf57506316ec19ba7eb24c7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.version=20250330.0.328921
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 30 Mar 2025 00:07:39 GMT
LABEL org.opencontainers.image.created=2025-03-30T00:07:39+00:00
# Sun, 30 Mar 2025 00:07:39 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250330.0.328921' /etc/os-release # buildkit
# Sun, 30 Mar 2025 00:07:39 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 00:07:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ad34537c3749262aa4117f2f3c7acbd59db0eced0a6efee1cdba55032a967b0e`  
		Last Modified: Mon, 31 Mar 2025 16:35:15 GMT  
		Size: 330.8 MB (330824353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cdf2da152fe4648b2bfb5f57eb0fdce85b8fabb9b153f5a67f3fe5b292366f`  
		Last Modified: Mon, 31 Mar 2025 16:35:07 GMT  
		Size: 10.3 KB (10257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250330.0.328921` - unknown; unknown

```console
$ docker pull archlinux@sha256:87ebf1488c6902a4bbfe2567053ac58f7d7437a1d085b4a819e1402abfd0e6c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12262463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f1bd9df030ad99b19aec22187fb2c00b76fd4a60916de6485392d5172038e2`

```dockerfile
```

-	Layers:
	-	`sha256:c1bd5878d4df9fe2426591610e1e64791efc50249a36114b2b85e054e45f0dcd`  
		Last Modified: Mon, 31 Mar 2025 16:35:08 GMT  
		Size: 12.3 MB (12250652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a891cbe827c9043a292ac6b68b0833c420170a44e75ab68364d2668954fa20c3`  
		Last Modified: Mon, 31 Mar 2025 16:35:07 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
