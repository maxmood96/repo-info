## `archlinux:multilib-devel-20250810.0.398652`

```console
$ docker pull archlinux@sha256:ceeeca91f88305fcc3d59761f080368aacb113c1ea5f708920995e9ed3a159f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250810.0.398652` - linux; amd64

```console
$ docker pull archlinux@sha256:9c3d9e65a6d665d2b4c760f4df0bb75b6deb1187b455bb161dcebc8220bc9f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.3 MB (358324402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc68686ebb40e48897d5b92bb3333e06bd1213ba1fd76602a2533f0209a73ab9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250810.0.398652
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 10 Aug 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-08-10T00:07:35+00:00
# Sun, 10 Aug 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250810.0.398652' /etc/os-release # buildkit
# Sun, 10 Aug 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 10 Aug 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:71ca4fc96d00bd13faa0c13bb0699fd58f80215ed66560f5b200c969c5ebbd46`  
		Last Modified: Mon, 11 Aug 2025 20:17:20 GMT  
		Size: 358.3 MB (358314134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b176c205797d706d232f226326cdb8661940a88bfcb3ba704464585b00653bc5`  
		Last Modified: Mon, 11 Aug 2025 17:07:07 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250810.0.398652` - unknown; unknown

```console
$ docker pull archlinux@sha256:258b6fab39a9b9124f18790a2a065d37a7102ea05798f1493a8f5004040a32c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12344512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72d5e4161c5a7d8a86146940e9962d98d03eb35ab9105db383edee231032070`

```dockerfile
```

-	Layers:
	-	`sha256:4fed8fac575a94c0b42f20f24a3cf7f934f24cba15df71a0075c56b071f37207`  
		Last Modified: Mon, 11 Aug 2025 19:48:25 GMT  
		Size: 12.3 MB (12332701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80490166b61838f075b438b351c109682a4e470475787eb01d605c3eaac90a93`  
		Last Modified: Mon, 11 Aug 2025 19:48:26 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
