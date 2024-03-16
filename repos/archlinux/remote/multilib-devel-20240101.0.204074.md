## `archlinux:multilib-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:c0dc3c22dc0ee2bc758c62038b4ed5026af98970361b488e68cafa4384d5dccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:multilib-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:bdabdaf70259e439876c7d29ce85b2217be95601544553b8e029c7322e8542e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316045008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9feecb236dcf9e4ae3a84719eea979bd3cdd1b6d184aa492d7304964b8f18861`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:10:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:10:39 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:10:51 GMT
COPY dir:75c66889520f549930c0f406d7a42c7d20e2d1d2e662322c69dc3a2dcb5d5bc5 in / 
# Sat, 16 Mar 2024 06:10:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:10:55 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:10:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f377e15cb8d612a50f6c51ebcee45ab2e4b9221e4dc99f177dc54b529f9f0edf`  
		Last Modified: Mon, 01 Jan 2024 19:20:55 GMT  
		Size: 316.0 MB (316034966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc436cc52de3b0668da7c860873c75ff908ba8966eebc758a7c95e6cb0b4b5e`  
		Last Modified: Sat, 16 Mar 2024 06:11:30 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
