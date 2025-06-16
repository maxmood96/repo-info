## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:3f808d41e09261904a04709fc210a154ee56f6a9c369a15a70c2dfac5adab498
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:00ddc0f2cdfa19e54f164037d768901f8fb81a1aa6a5b2907d259a6729be2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287711663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb635301b5860ac61bbf7aa404a7a2e5faa5f9b4aa967be5853c38db48f92f8e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.version=20250615.0.365905
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 15 Jun 2025 00:07:56 GMT
LABEL org.opencontainers.image.created=2025-06-15T00:07:56+00:00
# Sun, 15 Jun 2025 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250615.0.365905' /etc/os-release # buildkit
# Sun, 15 Jun 2025 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 15 Jun 2025 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f4798adc81b48051de112e7ae73136962449d8ea7e2ca5cdbcffd11241616ca6`  
		Last Modified: Mon, 16 Jun 2025 19:48:43 GMT  
		Size: 287.7 MB (287702494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65be26e0401c45bc2b22a0dd51d271a1871ab19334ad3d6666642834777440`  
		Last Modified: Mon, 16 Jun 2025 17:01:13 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a990984f400a942a705a6fdcf7085eb5208dc5c4bb00ee28d43149eae4618e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12020639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98ec7d24ae2fd24ae85ac68e926c15933606972f67aff8dbdefd3d43d9509c6`

```dockerfile
```

-	Layers:
	-	`sha256:138ee4a5418a46961fbb719f21969fcdef5019ae0a60f2b6a249917cf2a6add1`  
		Last Modified: Mon, 16 Jun 2025 19:48:22 GMT  
		Size: 12.0 MB (12008885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480974f87c503ea017d9f3ad42cc3ab8ab1d5b4a0659cd99055e2502f2e6c48f`  
		Last Modified: Mon, 16 Jun 2025 19:48:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
