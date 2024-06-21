## `archlinux:base`

```console
$ docker pull archlinux@sha256:7ddb28e525cda55998a80d147967865193d170b0cf75c999ff2e3116d8f95a32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:7b5aa07f86a6958bb072227e18e76ef37e59c65bff56a45aab695def2ddecd64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (147995398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fa6eaece3899bac1ab0691353fb328faf435634a0c82d1c88c28a504cb4ab2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d9884827b07bb5df1be9734d10e7db68899aedbb38552f40a11adf399debdaaf`  
		Last Modified: Wed, 08 May 2024 21:11:13 GMT  
		Size: 148.0 MB (147987269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9688c28db8a0d21798afbc20a23e0aadbd14555ae21887d45c163c68d3d3042`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 8.1 KB (8129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:edd980ef21dd76a28f8dfe72bb908a399dc7f2c4d5eab344d6628425531ed009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7958197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501496497dd59052086180961a0179bcea141bf4a3f609cc0bc5bb1c9c7e0743`

```dockerfile
```

-	Layers:
	-	`sha256:1c0a8beb9dde291cfa74a6db9f2d39b1234b54c1c06c229ee48cd020680c3acb`  
		Last Modified: Thu, 20 Jun 2024 20:55:12 GMT  
		Size: 7.9 MB (7946476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcad92faec2ae7ecdcfa6fff658061c3b359bbfa206c9b348cc76f28c361e165`  
		Last Modified: Thu, 20 Jun 2024 20:55:11 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
