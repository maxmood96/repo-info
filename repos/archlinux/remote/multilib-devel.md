## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:77812793dd9b43776c5dba213f12b2be2078c835204ef1a91f60d5fb09a8b1cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f2658db6097fb27ecb07d8a3d69352caef97e4df0526fb56b10bffd5e3a966a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322377273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230a73359d2903240dee464607d85d24caae35e7a166be303c5da59d1ce8c0ee`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.version=20241201.0.284684
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 01 Dec 2024 00:07:55 GMT
LABEL org.opencontainers.image.created=2024-12-01T00:07:55+00:00
# Sun, 01 Dec 2024 00:07:55 GMT
COPY /rootfs/ / # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241201.0.284684' /etc/os-release # buildkit
# Sun, 01 Dec 2024 00:07:55 GMT
ENV LANG=C.UTF-8
# Sun, 01 Dec 2024 00:07:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:388a41f6c3933873f2781188065a2fc5a7a89bc7f669b9e9cfcc65845fca3266`  
		Last Modified: Mon, 02 Dec 2024 20:24:48 GMT  
		Size: 322.4 MB (322367076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55adff7b28c71e59b3ccfa5554f730945942a9e64a3da63b7fd9d1f6f37559fa`  
		Last Modified: Mon, 02 Dec 2024 20:24:44 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a5cbe4590ee01c3d3d373b941ee66bfe3ef69ec957064892328cb87a5de80cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11376e310ba181242373c53de127130ecc88cb3050e8425d486f7d4f650a435e`

```dockerfile
```

-	Layers:
	-	`sha256:917b1e23e6e52d622e41a3a44af4daeea162ffd6000866abc2c5ca5b0c57b6d3`  
		Last Modified: Mon, 02 Dec 2024 20:24:44 GMT  
		Size: 12.2 MB (12165176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8e9710b3ee74ed6a73145eecdb933b8e450ffdc6bfce7895b5b4a265848d9da`  
		Last Modified: Mon, 02 Dec 2024 20:24:44 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
