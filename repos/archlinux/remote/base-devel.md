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
		Last Modified: Tue, 07 Jan 2025 01:29:59 GMT  
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
		Last Modified: Tue, 07 Jan 2025 03:15:10 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
