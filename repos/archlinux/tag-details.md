<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250126.0.301347`](#archlinuxbase-202501260301347)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250126.0.301347`](#archlinuxbase-devel-202501260301347)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250126.0.301347`](#archlinuxmultilib-devel-202501260301347)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:812644fa7bb7790deb91c55fb694461706103288dead4395694efad4b0bf0212
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c2a6685fa6fe41de064ce806e155c3f367e42f8c02d15570f52d2b4ba5caa3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157334876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8fbefc2e63ce88ef835bff4d3ff4c0906baf135554deb2244d0c0a8dcf7a14`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250119.0.299327
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-01-19T00:08:08+00:00
# Sun, 19 Jan 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250119.0.299327' /etc/os-release # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 19 Jan 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ef0a06159f178582f6820b464891259a020e96afae5a51a076479517af6a6379`  
		Last Modified: Tue, 21 Jan 2025 18:27:46 GMT  
		Size: 157.3 MB (157326594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e904b75d0c092101c50846fabc53329f343e9e93855cfd2119eb6eadd874727`  
		Last Modified: Tue, 21 Jan 2025 18:27:43 GMT  
		Size: 8.3 KB (8282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:3dda6e0140abfa378ad3150852aff571fbb3b3fa8bcdecf0deee3d30eb71d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8099800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b3ce04b04f1ff54c01c0ccc7d775790aa3b4f1c4ec36a8d53da441f3f05ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f075b4062b31c5f8386b8609cf6db46bb5316956d606018e2426111e37f8ec37`  
		Last Modified: Tue, 21 Jan 2025 18:27:44 GMT  
		Size: 8.1 MB (8087828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2887791265e4c0a8cb098575aa1c502cca46cc6d89ca545b827b57fd508e986b`  
		Last Modified: Tue, 21 Jan 2025 18:27:44 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250126.0.301347`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:8999d2508a630f124deb8b4f7a493d03241dd684960832b23fb07ae5176c5cea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5f0f68c1af64d9a2c1f39e5b6cf0103f0faa0d74e6cf38ea76995e130ef87c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278486744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537671745d28d2908e964be52931c8329c51be6a939d745113d8e216e59722ec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250119.0.299327
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-01-19T00:08:08+00:00
# Sun, 19 Jan 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250119.0.299327' /etc/os-release # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 19 Jan 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c92ba3935010a1e30876df8fa9636cdf7561433736d82ba5021cf01744194742`  
		Last Modified: Tue, 21 Jan 2025 18:28:12 GMT  
		Size: 278.5 MB (278477706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1664055cd5c8342841ed838597cc1cba4c1ebffc0ac35829d49369397115d9`  
		Last Modified: Tue, 21 Jan 2025 18:28:08 GMT  
		Size: 9.0 KB (9038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c39d380c77720b207501086bf9f25f19acb5ce303a16373c642d7157790c2d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11906438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aabf00209b7f9f3d3036eb329862a44c10a2c87cfb275da6d452413d88e84a`

```dockerfile
```

-	Layers:
	-	`sha256:cccc3e23a7c5e122d6b3b2df9c2185a610e9f2aebd54d2026623d1f9fe146b08`  
		Last Modified: Tue, 21 Jan 2025 18:28:09 GMT  
		Size: 11.9 MB (11894684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da9fde35c48ec031f36362f00d3c24a0d6d80bae83ae1ed5fb8eb7bf8bd15b9`  
		Last Modified: Tue, 21 Jan 2025 18:28:08 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250126.0.301347`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:812644fa7bb7790deb91c55fb694461706103288dead4395694efad4b0bf0212
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c2a6685fa6fe41de064ce806e155c3f367e42f8c02d15570f52d2b4ba5caa3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157334876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8fbefc2e63ce88ef835bff4d3ff4c0906baf135554deb2244d0c0a8dcf7a14`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250119.0.299327
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-01-19T00:08:08+00:00
# Sun, 19 Jan 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250119.0.299327' /etc/os-release # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 19 Jan 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ef0a06159f178582f6820b464891259a020e96afae5a51a076479517af6a6379`  
		Last Modified: Tue, 21 Jan 2025 18:27:46 GMT  
		Size: 157.3 MB (157326594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e904b75d0c092101c50846fabc53329f343e9e93855cfd2119eb6eadd874727`  
		Last Modified: Tue, 21 Jan 2025 18:27:43 GMT  
		Size: 8.3 KB (8282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:3dda6e0140abfa378ad3150852aff571fbb3b3fa8bcdecf0deee3d30eb71d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8099800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4b3ce04b04f1ff54c01c0ccc7d775790aa3b4f1c4ec36a8d53da441f3f05ba1`

```dockerfile
```

-	Layers:
	-	`sha256:f075b4062b31c5f8386b8609cf6db46bb5316956d606018e2426111e37f8ec37`  
		Last Modified: Tue, 21 Jan 2025 18:27:44 GMT  
		Size: 8.1 MB (8087828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2887791265e4c0a8cb098575aa1c502cca46cc6d89ca545b827b57fd508e986b`  
		Last Modified: Tue, 21 Jan 2025 18:27:44 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:ff6470d224bb12bb677a6b08a6124a9b008f3ea3b69703cc84625e0ce4602fd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:95a4ea960d5ddda41f534cb47aa833e0ab1311577a6ecb6ad6f25a36f66415ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328347414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4797ad20713e5f74fc1dba1d956832c9cb11e214884f872614d757634b379b2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250119.0.299327
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-01-19T00:08:08+00:00
# Sun, 19 Jan 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250119.0.299327' /etc/os-release # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 19 Jan 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5d7fac93d56c1bd297bc1d6bfd88706513aebd832974fd49c8b251f381157415`  
		Last Modified: Tue, 21 Jan 2025 18:28:41 GMT  
		Size: 328.3 MB (328337189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dd54ca61fdf27372b360d168518b8c0d98f2dd1ec4317534b4572ba93cc401`  
		Last Modified: Tue, 21 Jan 2025 18:28:35 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f77ba332d5c101dba25b236bfdba894211f57f575514744e9dc8d65d11d4115c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12175015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd206ec2c5dfc6423da23a7599c1d9c41d17306a50ca964aaf35da895095832f`

```dockerfile
```

-	Layers:
	-	`sha256:df24ec1b18f79dec2c2c9e8df22562c87c2e719fd05a1ef53adc337265b7f9e7`  
		Last Modified: Tue, 21 Jan 2025 18:28:35 GMT  
		Size: 12.2 MB (12163204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c61aad88faf255738d0ed376dda4ac8a18dde8e9a949ef3f2074e143692ee81`  
		Last Modified: Tue, 21 Jan 2025 18:28:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250126.0.301347`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
