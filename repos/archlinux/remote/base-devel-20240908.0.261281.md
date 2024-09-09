## `archlinux:base-devel-20240908.0.261281`

```console
$ docker pull archlinux@sha256:82d29f4616cbe45e42887f0369dceea6b67768e8ac99c925155e47d1ed3c82cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20240908.0.261281` - linux; amd64

```console
$ docker pull archlinux@sha256:a882417f30e2193e42078ab847fccaadc88ffb77b10bd2363d27cd913bc6c869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272290652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82180bf4d936f57230c788e5b2a3049aeb2fbee773da3e63751e9e6cacf9c00a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.version=20240908.0.261281
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Sep 2024 00:07:27 GMT
LABEL org.opencontainers.image.created=2024-09-08T00:07:27+00:00
# Sun, 08 Sep 2024 00:07:27 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240908.0.261281' /etc/os-release # buildkit
# Sun, 08 Sep 2024 00:07:27 GMT
ENV LANG=C.UTF-8
# Sun, 08 Sep 2024 00:07:27 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b036fa806bbbda498e1d11af9ea2e9f0da818b514273180d0d800a03cb9b15d8`  
		Last Modified: Mon, 09 Sep 2024 19:04:53 GMT  
		Size: 272.3 MB (272281606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27595973d89a3e1e051da627231a077d3a8863053b980857795e0dcaf478ad2a`  
		Last Modified: Mon, 09 Sep 2024 19:04:49 GMT  
		Size: 9.0 KB (9046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20240908.0.261281` - unknown; unknown

```console
$ docker pull archlinux@sha256:633bdf2e7bb1670387d4bb8d207a0d204c1046bcf0d12fd308195d6ce4eda44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11913861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dece966292a85e07badf559ea4efcf80af377088af670107d0388a57193115`

```dockerfile
```

-	Layers:
	-	`sha256:b38e4c18f5d27aa9536c9506fdad1abc41e66fddd82d022e51495d28be2f5273`  
		Last Modified: Mon, 09 Sep 2024 19:04:50 GMT  
		Size: 11.9 MB (11902358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a8659b2b8584b1743849eaf36973b789ea3a77d0b7871899ee06d17eb9c96a9`  
		Last Modified: Mon, 09 Sep 2024 19:04:50 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
