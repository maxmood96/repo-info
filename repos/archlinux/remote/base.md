## `archlinux:base`

```console
$ docker pull archlinux@sha256:ae7491066c2f96861d7b442aef512974138c2004b8bf5b2aacda6b8fd9e112fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:068aa6bfc1e735cdf9be3dbf66327011f99126656f479168f479d68b28181106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159152424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d4665b7362f3c2d04392ddec5964b72d305e3640a5e99430f3a4be00c2d6f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250302.0.316047
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-03-02T00:07:35+00:00
# Sun, 02 Mar 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250302.0.316047' /etc/os-release # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 02 Mar 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:51e5f99a23d6af0dc9c3bb45943e9950d7aa3a815eaedd81e944b1f0999c88e1`  
		Last Modified: Mon, 03 Mar 2025 19:12:43 GMT  
		Size: 159.1 MB (159144057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb7f519a524771019f49e25f7c55ea730a29becb5d3e6e1d72af226714dc5d9`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:a3990677d69dabc03809ed735990bcaf7d6af24e1f51193a9102ee09da08f668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8167471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cf10d6ccdeb296a6be5048270c7cc3902e7a0af18c72669b90b697cf8890af`

```dockerfile
```

-	Layers:
	-	`sha256:a8f854c114c75d52c5dce84540c6aab80a1d12432f599145aeca4c709a7eedd9`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 8.2 MB (8155499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4ae77eb4717a10f5b21a1ef6933ea61dd0a091558d99a23a67258833568dc7`  
		Last Modified: Mon, 03 Mar 2025 19:12:39 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
