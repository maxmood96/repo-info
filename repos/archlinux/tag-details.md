<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250105.0.295102`](#archlinuxbase-202501050295102)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250105.0.295102`](#archlinuxbase-devel-202501050295102)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250105.0.295102`](#archlinuxmultilib-devel-202501050295102)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:1fd38e3e4e6e59b35b4cfc63d1416a1eebff7b9e1c0d206d484b537d70e9ee5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:29c0e36e00e6d5a8dc31fc1f1c48293744bf726501bee400bd658238c6a97f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153107934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8877e73a3e461959c9e6020f6c846e5bab90e4b625fc71b34c9ca6576b8c0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:734567a21ac630b02c05a26a3b8bdedcba14ff5644a33b2bb998c65564bf7647`  
		Last Modified: Tue, 07 Jan 2025 01:29:16 GMT  
		Size: 153.1 MB (153099589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b4a585c6e7b1cbb51e0f620a4017295359daaf4fe97d4d44fb7ec8da52a7c8`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 8.3 KB (8345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:7ec2730ae5461957405e83f061ca4793237b70cd0c720f21be76163af2548eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813ceff32a2a96f0cc161f89953211c3223ab12b3c1729078d6cb9893462d640`

```dockerfile
```

-	Layers:
	-	`sha256:5c26359a0123605ae2cb5ff69fd83a6d95655582632f99e6932e8fc6f1945ed6`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 8.1 MB (8088854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e0d5afc84f8673d3d15a3dd69c666c05f2b9879d80fe1fb68f2ad994737a5e`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250105.0.295102`

```console
$ docker pull archlinux@sha256:1fd38e3e4e6e59b35b4cfc63d1416a1eebff7b9e1c0d206d484b537d70e9ee5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20250105.0.295102` - linux; amd64

```console
$ docker pull archlinux@sha256:29c0e36e00e6d5a8dc31fc1f1c48293744bf726501bee400bd658238c6a97f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153107934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8877e73a3e461959c9e6020f6c846e5bab90e4b625fc71b34c9ca6576b8c0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:734567a21ac630b02c05a26a3b8bdedcba14ff5644a33b2bb998c65564bf7647`  
		Last Modified: Tue, 07 Jan 2025 01:29:16 GMT  
		Size: 153.1 MB (153099589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b4a585c6e7b1cbb51e0f620a4017295359daaf4fe97d4d44fb7ec8da52a7c8`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 8.3 KB (8345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20250105.0.295102` - unknown; unknown

```console
$ docker pull archlinux@sha256:7ec2730ae5461957405e83f061ca4793237b70cd0c720f21be76163af2548eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813ceff32a2a96f0cc161f89953211c3223ab12b3c1729078d6cb9893462d640`

```dockerfile
```

-	Layers:
	-	`sha256:5c26359a0123605ae2cb5ff69fd83a6d95655582632f99e6932e8fc6f1945ed6`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 8.1 MB (8088854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e0d5afc84f8673d3d15a3dd69c666c05f2b9879d80fe1fb68f2ad994737a5e`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:cae67dddfec15706ad031d501b6f28ac520afa5d1a4b79a0452437a70c03bcec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0df0b4c65928d063ffeb869e57ad18737f7b223f89c961fbfc74dac9b0743a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274213256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbf5e2f858ee9ce1a04c4c56ac6697e5672c99fd8092d11f46433fae7b35a5f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:680acf88979475a77fdde57deae10e0d8eb993a7fa27c17ea6fd78b65cfe855e`  
		Size: 274.2 MB (274204153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7a3326e5f0b82194d6c5f286b561d32260e2d6675ebd0fb5c7d7c42e55ed4f`  
		Last Modified: Tue, 07 Jan 2025 03:15:10 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3ea2eb37a50ba91294ef69e7ed8e7b0f1cbe23b7af2e7f0ec3e7fcc64a95dbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e69d50fa3d486d27b2118414fae3730fc5688bd8b09e21cdbeb5e89fe07463b`

```dockerfile
```

-	Layers:
	-	`sha256:534ebc1d7851581a1cdc5aaa785d5adfd2f51e95fad1bacc0705757ea847ac84`  
		Last Modified: Tue, 07 Jan 2025 03:15:11 GMT  
		Size: 11.9 MB (11896302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d82f1a29378e6673334d17169a0e4fcc7309e99d7e95073967a9e5a45661a2f1`  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250105.0.295102`

```console
$ docker pull archlinux@sha256:cae67dddfec15706ad031d501b6f28ac520afa5d1a4b79a0452437a70c03bcec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250105.0.295102` - linux; amd64

```console
$ docker pull archlinux@sha256:0df0b4c65928d063ffeb869e57ad18737f7b223f89c961fbfc74dac9b0743a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274213256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbf5e2f858ee9ce1a04c4c56ac6697e5672c99fd8092d11f46433fae7b35a5f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:680acf88979475a77fdde57deae10e0d8eb993a7fa27c17ea6fd78b65cfe855e`  
		Size: 274.2 MB (274204153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7a3326e5f0b82194d6c5f286b561d32260e2d6675ebd0fb5c7d7c42e55ed4f`  
		Last Modified: Tue, 07 Jan 2025 03:15:10 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250105.0.295102` - unknown; unknown

```console
$ docker pull archlinux@sha256:3ea2eb37a50ba91294ef69e7ed8e7b0f1cbe23b7af2e7f0ec3e7fcc64a95dbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11908056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e69d50fa3d486d27b2118414fae3730fc5688bd8b09e21cdbeb5e89fe07463b`

```dockerfile
```

-	Layers:
	-	`sha256:534ebc1d7851581a1cdc5aaa785d5adfd2f51e95fad1bacc0705757ea847ac84`  
		Last Modified: Tue, 07 Jan 2025 03:15:11 GMT  
		Size: 11.9 MB (11896302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d82f1a29378e6673334d17169a0e4fcc7309e99d7e95073967a9e5a45661a2f1`  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:1fd38e3e4e6e59b35b4cfc63d1416a1eebff7b9e1c0d206d484b537d70e9ee5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:29c0e36e00e6d5a8dc31fc1f1c48293744bf726501bee400bd658238c6a97f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153107934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec8877e73a3e461959c9e6020f6c846e5bab90e4b625fc71b34c9ca6576b8c0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:734567a21ac630b02c05a26a3b8bdedcba14ff5644a33b2bb998c65564bf7647`  
		Last Modified: Tue, 07 Jan 2025 01:29:16 GMT  
		Size: 153.1 MB (153099589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b4a585c6e7b1cbb51e0f620a4017295359daaf4fe97d4d44fb7ec8da52a7c8`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 8.3 KB (8345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:7ec2730ae5461957405e83f061ca4793237b70cd0c720f21be76163af2548eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8100826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813ceff32a2a96f0cc161f89953211c3223ab12b3c1729078d6cb9893462d640`

```dockerfile
```

-	Layers:
	-	`sha256:5c26359a0123605ae2cb5ff69fd83a6d95655582632f99e6932e8fc6f1945ed6`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 8.1 MB (8088854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e0d5afc84f8673d3d15a3dd69c666c05f2b9879d80fe1fb68f2ad994737a5e`  
		Last Modified: Tue, 07 Jan 2025 03:14:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:381838703ee564e8e7a29cca049c72b304bc6ff83c3a5f12d1c783f7c50566de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:511ccee2464ee5da2cdb1b99a24c9538a5c32d13289d7b59893d104af0995148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324062556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e2370fef6a51b2636be8f4a3fc6661118df4b39f4c54365a1ddecfb49321ce`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35f18d87fe1c34fb6189104a5557fc7dd308f8df7e0bb81cf374e2a2d3b7c8a2`  
		Last Modified: Tue, 07 Jan 2025 01:30:06 GMT  
		Size: 324.1 MB (324052296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4777a9c61f77fa4ba01d232c41a281a4f2669416dcf2a966ee788a7d60bf0307`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:7f9ecef7e3853105e82c3de3d19ef23318211a3656ba9bdd4cbf3a8a50b26ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208881dde28c504e4b93a5345dd6718dfbbe15eeff035120208988ed52cb1fa6`

```dockerfile
```

-	Layers:
	-	`sha256:957597259501490e469c8418ee89c128a9621ed33c5fa52137a2321b4a9c442a`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 12.2 MB (12164822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d12b515b47b52b249bb9e07785903d76faa1762d42281a49d36b1ce792e9870`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250105.0.295102`

```console
$ docker pull archlinux@sha256:381838703ee564e8e7a29cca049c72b304bc6ff83c3a5f12d1c783f7c50566de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250105.0.295102` - linux; amd64

```console
$ docker pull archlinux@sha256:511ccee2464ee5da2cdb1b99a24c9538a5c32d13289d7b59893d104af0995148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324062556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e2370fef6a51b2636be8f4a3fc6661118df4b39f4c54365a1ddecfb49321ce`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.version=20250105.0.295102
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 05 Jan 2025 00:08:06 GMT
LABEL org.opencontainers.image.created=2025-01-05T00:08:06+00:00
# Sun, 05 Jan 2025 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250105.0.295102' /etc/os-release # buildkit
# Sun, 05 Jan 2025 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 05 Jan 2025 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35f18d87fe1c34fb6189104a5557fc7dd308f8df7e0bb81cf374e2a2d3b7c8a2`  
		Last Modified: Tue, 07 Jan 2025 01:30:06 GMT  
		Size: 324.1 MB (324052296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4777a9c61f77fa4ba01d232c41a281a4f2669416dcf2a966ee788a7d60bf0307`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250105.0.295102` - unknown; unknown

```console
$ docker pull archlinux@sha256:7f9ecef7e3853105e82c3de3d19ef23318211a3656ba9bdd4cbf3a8a50b26ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208881dde28c504e4b93a5345dd6718dfbbe15eeff035120208988ed52cb1fa6`

```dockerfile
```

-	Layers:
	-	`sha256:957597259501490e469c8418ee89c128a9621ed33c5fa52137a2321b4a9c442a`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 12.2 MB (12164822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d12b515b47b52b249bb9e07785903d76faa1762d42281a49d36b1ce792e9870`  
		Last Modified: Tue, 07 Jan 2025 03:15:03 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
