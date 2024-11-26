<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241124.0.282387`](#archlinuxbase-202411240282387)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241124.0.282387`](#archlinuxbase-devel-202411240282387)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241124.0.282387`](#archlinuxmultilib-devel-202411240282387)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:fc897ab3c923fa324b1c9abf5ee08ac4f376092da2d9fec331294e8d54fedd10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:565f16a79515bef3b66439cc8ff03b754f41e76f0d431d0e3b4f3a5825cdeff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151308382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b92a769a168819a59a9d421b1a8c97fdaa87568298716446d17802605b0f44`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f524c82a4279ec25a2fddc9b69620d6dc38b8f1e7c8a6a4596478dbce8e96100`  
		Last Modified: Mon, 25 Nov 2024 20:24:17 GMT  
		Size: 151.3 MB (151300062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061d5e0ca6d1f0bf9cd9b5efc6756a6cbfd81dd87011f27fd1bb5f0b9d8f075`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.3 KB (8320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:ceaeb0a9110116e81f1ba710eecc1284603f69e7c7af6fa657b326a6a7185c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0127b9a8c6982033cd69680b63f429fc8236f49e6f96d862ebee2eca2b8e477d`

```dockerfile
```

-	Layers:
	-	`sha256:1559809d9d4ffa0b705f8c637df23d12b8757acd5630123a17aa815b71498dfd`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a1505f67255a492bf8f693797a2ec5ef348ca48ea9d0499b8a97a2b4535290`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241124.0.282387`

```console
$ docker pull archlinux@sha256:fc897ab3c923fa324b1c9abf5ee08ac4f376092da2d9fec331294e8d54fedd10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241124.0.282387` - linux; amd64

```console
$ docker pull archlinux@sha256:565f16a79515bef3b66439cc8ff03b754f41e76f0d431d0e3b4f3a5825cdeff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151308382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b92a769a168819a59a9d421b1a8c97fdaa87568298716446d17802605b0f44`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f524c82a4279ec25a2fddc9b69620d6dc38b8f1e7c8a6a4596478dbce8e96100`  
		Last Modified: Mon, 25 Nov 2024 20:24:17 GMT  
		Size: 151.3 MB (151300062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061d5e0ca6d1f0bf9cd9b5efc6756a6cbfd81dd87011f27fd1bb5f0b9d8f075`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.3 KB (8320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241124.0.282387` - unknown; unknown

```console
$ docker pull archlinux@sha256:ceaeb0a9110116e81f1ba710eecc1284603f69e7c7af6fa657b326a6a7185c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0127b9a8c6982033cd69680b63f429fc8236f49e6f96d862ebee2eca2b8e477d`

```dockerfile
```

-	Layers:
	-	`sha256:1559809d9d4ffa0b705f8c637df23d12b8757acd5630123a17aa815b71498dfd`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a1505f67255a492bf8f693797a2ec5ef348ca48ea9d0499b8a97a2b4535290`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0803542df524cbf98632815130e842e442132fc2acdf6efd40333b9ae3ab8843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6f6846e2335c587e9cc8f0fc7fc6894b8a7bbd9282b9efee67b7af74108e7562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272432368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538f4ef9da5e85838e12574192127c343054c4b0730ef0a4c35dff1e56498f16`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1b6f7e9affed36df2233412893aa6e4f821d730b29f3ace9ac9c3927c04cc2a6`  
		Last Modified: Mon, 25 Nov 2024 20:24:55 GMT  
		Size: 272.4 MB (272423296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd750ddf004134fa8657e503b627f7f9b20ecd15bf02e22eef11df93da10e3a`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:979cdf626a17bc7ada8b3f28f1a4e88842e85e72c61eece6111e154e4a35ebbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd83b9b97ecfbbb7f183eaaff607a43a5e55813637679875dc0e2a3b39a519f9`

```dockerfile
```

-	Layers:
	-	`sha256:2adc875c40f574d6f22094972fde3e047d24cfec5b0af49f5c44d83050dd98f5`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 11.9 MB (11895700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94408f0bd73fe2ed86b15821f95c9f1684d90deae8e17c1413fbd8aa5766af23`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241124.0.282387`

```console
$ docker pull archlinux@sha256:0803542df524cbf98632815130e842e442132fc2acdf6efd40333b9ae3ab8843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241124.0.282387` - linux; amd64

```console
$ docker pull archlinux@sha256:6f6846e2335c587e9cc8f0fc7fc6894b8a7bbd9282b9efee67b7af74108e7562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272432368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538f4ef9da5e85838e12574192127c343054c4b0730ef0a4c35dff1e56498f16`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1b6f7e9affed36df2233412893aa6e4f821d730b29f3ace9ac9c3927c04cc2a6`  
		Last Modified: Mon, 25 Nov 2024 20:24:55 GMT  
		Size: 272.4 MB (272423296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd750ddf004134fa8657e503b627f7f9b20ecd15bf02e22eef11df93da10e3a`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241124.0.282387` - unknown; unknown

```console
$ docker pull archlinux@sha256:979cdf626a17bc7ada8b3f28f1a4e88842e85e72c61eece6111e154e4a35ebbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd83b9b97ecfbbb7f183eaaff607a43a5e55813637679875dc0e2a3b39a519f9`

```dockerfile
```

-	Layers:
	-	`sha256:2adc875c40f574d6f22094972fde3e047d24cfec5b0af49f5c44d83050dd98f5`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 11.9 MB (11895700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94408f0bd73fe2ed86b15821f95c9f1684d90deae8e17c1413fbd8aa5766af23`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:fc897ab3c923fa324b1c9abf5ee08ac4f376092da2d9fec331294e8d54fedd10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:565f16a79515bef3b66439cc8ff03b754f41e76f0d431d0e3b4f3a5825cdeff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151308382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b92a769a168819a59a9d421b1a8c97fdaa87568298716446d17802605b0f44`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f524c82a4279ec25a2fddc9b69620d6dc38b8f1e7c8a6a4596478dbce8e96100`  
		Last Modified: Mon, 25 Nov 2024 20:24:17 GMT  
		Size: 151.3 MB (151300062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061d5e0ca6d1f0bf9cd9b5efc6756a6cbfd81dd87011f27fd1bb5f0b9d8f075`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.3 KB (8320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:ceaeb0a9110116e81f1ba710eecc1284603f69e7c7af6fa657b326a6a7185c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0127b9a8c6982033cd69680b63f429fc8236f49e6f96d862ebee2eca2b8e477d`

```dockerfile
```

-	Layers:
	-	`sha256:1559809d9d4ffa0b705f8c637df23d12b8757acd5630123a17aa815b71498dfd`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a1505f67255a492bf8f693797a2ec5ef348ca48ea9d0499b8a97a2b4535290`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:21ee00acf5700be693c441245103c1a379fe5be67d095629e60a3e2d48de7e4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b6ba00ddf979ccdfa8f91ffe50679dcfd8e626b26395a58a5cbbc0991e3f174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322288757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cc884d991aa3d8a713d7a55a07032b534ad2e37082fb6a9ffdd5acaac4ec77`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a6264ef3f56194f7e1c6232cf9df5491f14cd5a516e567990264e87feae1d721`  
		Last Modified: Mon, 25 Nov 2024 20:25:12 GMT  
		Size: 322.3 MB (322278518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4801d8c4cbc3bdbc6548534820c5c5d771d66f25c77feb931358bb8109474b83`  
		Last Modified: Mon, 25 Nov 2024 20:25:02 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:85dbdc55e30e0bb61c95cbe3f212e8bb00be5053554b882c8728450e482f1d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b609b4af0dbdd86a5d1cc10764efcec7acd269cc251cc2a369029924e440b1`

```dockerfile
```

-	Layers:
	-	`sha256:43ca7f46cad5b757d77d5e5e50162a155ad2a0e727d70606b7d8375aa909dfd9`  
		Last Modified: Mon, 25 Nov 2024 20:25:03 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94666142745f37a235589a36d2449ab4ebcb1a36048b6492776617d876742101`  
		Last Modified: Mon, 25 Nov 2024 20:25:02 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241124.0.282387`

```console
$ docker pull archlinux@sha256:21ee00acf5700be693c441245103c1a379fe5be67d095629e60a3e2d48de7e4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241124.0.282387` - linux; amd64

```console
$ docker pull archlinux@sha256:b6ba00ddf979ccdfa8f91ffe50679dcfd8e626b26395a58a5cbbc0991e3f174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322288757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cc884d991aa3d8a713d7a55a07032b534ad2e37082fb6a9ffdd5acaac4ec77`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a6264ef3f56194f7e1c6232cf9df5491f14cd5a516e567990264e87feae1d721`  
		Last Modified: Mon, 25 Nov 2024 20:25:12 GMT  
		Size: 322.3 MB (322278518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4801d8c4cbc3bdbc6548534820c5c5d771d66f25c77feb931358bb8109474b83`  
		Last Modified: Mon, 25 Nov 2024 20:25:02 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241124.0.282387` - unknown; unknown

```console
$ docker pull archlinux@sha256:85dbdc55e30e0bb61c95cbe3f212e8bb00be5053554b882c8728450e482f1d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b609b4af0dbdd86a5d1cc10764efcec7acd269cc251cc2a369029924e440b1`

```dockerfile
```

-	Layers:
	-	`sha256:43ca7f46cad5b757d77d5e5e50162a155ad2a0e727d70606b7d8375aa909dfd9`  
		Last Modified: Mon, 25 Nov 2024 20:25:03 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94666142745f37a235589a36d2449ab4ebcb1a36048b6492776617d876742101`  
		Last Modified: Mon, 25 Nov 2024 20:25:02 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
