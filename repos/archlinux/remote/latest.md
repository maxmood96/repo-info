## `archlinux:latest`

```console
$ docker pull archlinux@sha256:2dbd72d1e5510e047db7f441bf9069e9c53391b87e04e5bee3f379cd03cec060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:85dc960fa1b01560091e6de62b09c4ad99c35cf818f6a7e2b2118a57f712bcb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147996205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cda8061254a9e2a6c1b57275e0c71174788b3775346fa3511d67163ad90be34`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sat, 16 Mar 2024 06:08:22 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Sat, 16 Mar 2024 06:08:23 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Sat, 16 Mar 2024 06:08:29 GMT
COPY dir:500a387e180f5288f7f6cc8c9e7245548b04a53ce9c569583f3e160673182bf9 in / 
# Sat, 16 Mar 2024 06:08:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release
# Sat, 16 Mar 2024 06:08:31 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 06:08:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a82a64c3a8439c75d8e584181427b073712afd1454747bec3dcb84bcbe19ac5`  
		Last Modified: Mon, 01 Jan 2024 19:19:12 GMT  
		Size: 148.0 MB (147988087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403a73115b61227673ac6c1a8802a4b3d939967a9efef31fee246a3acd790895`  
		Last Modified: Sat, 16 Mar 2024 06:11:15 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
