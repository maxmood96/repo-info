## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0a0024b86e4ec09652a3d98b1523509cfbbe47edea464ec775f41c8a506611bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4cf6853663815a5fc6b71ec234c4c3c56570bf325e54ffa298c4b701173aa3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271737229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff2dc87c647fce56a19da956611bbe7a811017385d380250806b60b374b047d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:298dc0d2952244fad2540d1cd7765c9b3beb1fae3ae90fe74a9d3339125caf9b`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 271.7 MB (271728156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8f652bae07bffcc8cfb894cf4f7bd10f8673e0ea5c49e087c9aad788dee476`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 9.1 KB (9073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:5dd1f62fab40309d3c7719203468ea51cad8e9e035d003dcb22561e21fc4e419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2562e9d770065dce7da13b06599ae58a1b08eca07cd3e524130caca2731142`

```dockerfile
```

-	Layers:
	-	`sha256:d1ffce5987530f281d0a6301f0592673236753a4e6af168a8e76d1bdc308fe72`  
		Last Modified: Mon, 26 Aug 2024 21:59:45 GMT  
		Size: 11.8 MB (11818188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef528f73d1ed1046bbdaf5dc47836287c8a5f5e5ba04e59006c303cd0baf0537`  
		Last Modified: Mon, 26 Aug 2024 21:59:44 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.in-toto+json
