## `archlinux:base`

```console
$ docker pull archlinux@sha256:8fe9851fcd8bd23ea0e6bfa99483d8778e40b45e0fd7bb8188c94cbdd8c25a38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:7b7bba26926c8bae835082a400fc0b5615a91fa3cfa56183ffede8ab69d3f8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164323307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b444b8a5550863744f1d1c07cef8a7137a9ed15c80631234658a74765e55eca9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250914.0.420821
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-14T00:07:14+00:00
# Sun, 14 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250914.0.420821' /etc/os-release # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 14 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9ed1b528ba03ff7a3bb0ffaccb1317530ae62b73bc0294667d34c927515d4136`  
		Last Modified: Mon, 15 Sep 2025 17:47:17 GMT  
		Size: 164.3 MB (164314969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e711ed963937def6a325b6ec32aca2cf29018e0d5e6d9f8b0d4cdab61791cf0`  
		Last Modified: Mon, 15 Sep 2025 17:00:09 GMT  
		Size: 8.3 KB (8338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:a5ec181549203664e58112d11d192d26785c36b7c1004aff1aae4bed2ea94042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96c8eeba9a9e8631242ea6723ce107c17819f95172e82fdd54ab3e75e8b4df2`

```dockerfile
```

-	Layers:
	-	`sha256:3900cebcc0b1edb531d3da51fd836f7a1e11c925e71fd88b1eccffbda043cad2`  
		Last Modified: Mon, 15 Sep 2025 19:48:17 GMT  
		Size: 8.2 MB (8182745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6119ef2b478ab0b116046a9bec2dffc49acfeaca24e0b6c9a90489537cecd2`  
		Last Modified: Mon, 15 Sep 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
