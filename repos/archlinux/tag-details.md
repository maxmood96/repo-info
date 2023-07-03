<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20230702.0.161694`](#archlinuxbase-202307020161694)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20230702.0.161694`](#archlinuxbase-devel-202307020161694)
-	[`archlinux:latest`](#archlinuxlatest)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:417c338ddd030f678ae1d5f7885cef7075d191434f98d2e9fc3d0ab10de9fc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:7a11444763f4de82939c50854370f5ab456ff8122466a596fc4e6e633e10b51b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146098519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e53dcc9ea40823c17746aa4cca3fab1bd77f9975d8a7c1277223ab471f1f6f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 27 Jun 2023 01:00:41 GMT
LABEL org.opencontainers.image.version=20230625.0.160368
# Tue, 27 Jun 2023 01:00:41 GMT
LABEL org.opencontainers.image.revision=e4875c7e3688c1c0863f1e70cdea9da73d03cbcd
# Tue, 27 Jun 2023 01:00:41 GMT
LABEL org.opencontainers.image.created=2023-06-25T00:07:45+00:00
# Tue, 27 Jun 2023 01:00:47 GMT
COPY dir:fac066235c37f5375f835af7ac97fbd1f1a73ee1a73c10ca8be0d8d1a135cd63 in / 
# Tue, 27 Jun 2023 01:00:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230625.0.160368' /etc/os-release
# Tue, 27 Jun 2023 01:00:49 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jun 2023 01:00:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b0df6823d2a59ffb3aef67ab23b23d6069260a64fd94a1d8e33c5175ed709854`  
		Last Modified: Tue, 27 Jun 2023 01:02:30 GMT  
		Size: 146.1 MB (146090454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac947a47866f8435c06dad9f8a5fbfc4774e8178050d6a89ca4c086bf09316`  
		Last Modified: Tue, 27 Jun 2023 01:02:11 GMT  
		Size: 8.1 KB (8065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-20230702.0.161694`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:811d77e132ea207feced7591c2bc9c6a08ae1699edf4ddfc74880001374d1c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:23ad4f5906a06a2a28e9757c3dbfb150a694f6e144676e30265c765c90a30cbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262917667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeabcad2e34db4df48bb5d6d4c96d331a0d4356869351e21bf81fa6812814af0`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:20:54 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:20:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 27 Jun 2023 01:01:40 GMT
LABEL org.opencontainers.image.version=20230625.0.160368
# Tue, 27 Jun 2023 01:01:40 GMT
LABEL org.opencontainers.image.revision=e4875c7e3688c1c0863f1e70cdea9da73d03cbcd
# Tue, 27 Jun 2023 01:01:41 GMT
LABEL org.opencontainers.image.created=2023-06-25T00:07:48+00:00
# Tue, 27 Jun 2023 01:01:51 GMT
COPY dir:4072e12be121cb240c4731420fc55b0972a780cf05c2372dc0fda96d8ce7ef96 in / 
# Tue, 27 Jun 2023 01:01:54 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230625.0.160368' /etc/os-release
# Tue, 27 Jun 2023 01:01:54 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jun 2023 01:01:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a158e4de0ce35b3c68e74275f4a480ed7f4e0f0a8915cf5a8a726e6a4e63323b`  
		Last Modified: Mon, 26 Jun 2023 05:55:08 GMT  
		Size: 262.9 MB (262908768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9bc45e9bc54e13e90041cb280538dea4ceb31cd3dc6317c936e9b26a889bba`  
		Last Modified: Tue, 27 Jun 2023 01:02:42 GMT  
		Size: 8.9 KB (8899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `archlinux:base-devel-20230702.0.161694`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:417c338ddd030f678ae1d5f7885cef7075d191434f98d2e9fc3d0ab10de9fc84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:7a11444763f4de82939c50854370f5ab456ff8122466a596fc4e6e633e10b51b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146098519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e53dcc9ea40823c17746aa4cca3fab1bd77f9975d8a7c1277223ab471f1f6f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jun 2023 18:19:57 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 27 Jun 2023 01:00:41 GMT
LABEL org.opencontainers.image.version=20230625.0.160368
# Tue, 27 Jun 2023 01:00:41 GMT
LABEL org.opencontainers.image.revision=e4875c7e3688c1c0863f1e70cdea9da73d03cbcd
# Tue, 27 Jun 2023 01:00:41 GMT
LABEL org.opencontainers.image.created=2023-06-25T00:07:45+00:00
# Tue, 27 Jun 2023 01:00:47 GMT
COPY dir:fac066235c37f5375f835af7ac97fbd1f1a73ee1a73c10ca8be0d8d1a135cd63 in / 
# Tue, 27 Jun 2023 01:00:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20230625.0.160368' /etc/os-release
# Tue, 27 Jun 2023 01:00:49 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jun 2023 01:00:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b0df6823d2a59ffb3aef67ab23b23d6069260a64fd94a1d8e33c5175ed709854`  
		Last Modified: Tue, 27 Jun 2023 01:02:30 GMT  
		Size: 146.1 MB (146090454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac947a47866f8435c06dad9f8a5fbfc4774e8178050d6a89ca4c086bf09316`  
		Last Modified: Tue, 27 Jun 2023 01:02:11 GMT  
		Size: 8.1 KB (8065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
