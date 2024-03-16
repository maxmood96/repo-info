## `archlinux:base-devel-20240101.0.204074`

```console
$ docker pull archlinux@sha256:10ce20a6f7e0844e2b0cbe367dc32b584dfbfa9dc068712d119b192c5c83b637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20240101.0.204074` - linux; amd64

```console
$ docker pull archlinux@sha256:095d7d25a366555f47926b4ff5b8e2284b671499310ee3b5e270a77b7f3cdffb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266238377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b8abb90a6e1b1a62cd58dc9c2e8f1f91ed3fd1820f5dd12e2e80afb6234eaf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:09:20 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:09:21 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:09:31 GMT
COPY dir:26a13fc3a1ba45fe2c4b0785d8b1a68ce5991bc4fbd4c078f8b86bf9c621781e in / 
# Sat, 16 Mar 2024 06:09:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:09:35 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:09:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:444f393ce858c4b3035c5cb5e2e6b5b46661dd73311818d48dead4150ac68209`  
		Last Modified: Mon, 01 Jan 2024 19:20:00 GMT  
		Size: 266.2 MB (266229441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874e70007832dd23b4111f786258826ced23964005f0e37dabb80e2327ed9128`  
		Last Modified: Sat, 16 Mar 2024 06:11:23 GMT  
		Size: 8.9 KB (8936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
