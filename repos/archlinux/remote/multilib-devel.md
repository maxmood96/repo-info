## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9711b4be47a416b61be5b704e5d0c2151f9433aae0bc0a28605413da314a2835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:fe7de951e3c9afde1c7c9212c1d0243de19a2f049b09d83713d486bf190a9d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321999667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f74b571feb32a8a6fe653d921a42a30124e0bc4969a1faea33a4482b80a05a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240915.0.262934
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-15T00:07:28+00:00
# Sun, 15 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240915.0.262934' /etc/os-release # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 15 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:49ede7ca1d036d7b0e613f74870a3c54440fde21de83c98af88d9e67a86bb40a`  
		Last Modified: Mon, 16 Sep 2024 17:57:32 GMT  
		Size: 322.0 MB (321989535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced223c1b6c1510942f6067b949d97fabf7753365280443cf865a0cda1d61162`  
		Last Modified: Mon, 16 Sep 2024 17:57:28 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:05a144ecade139135171171a711654474b17071aa37683bdd1a654e89b1c06e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc3c2c563084daa3f259763729c8946a517337df80599093de4650790d2bb85`

```dockerfile
```

-	Layers:
	-	`sha256:2cff3358a1d6eb51475f87ba0040ec955100c828ea4e3d0baca2ddb279fce1c6`  
		Last Modified: Mon, 16 Sep 2024 17:57:28 GMT  
		Size: 12.2 MB (12167919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00322cdee2cfdfbc1c0021a409cbaf4adffac4d445e10e0548065cb4a172c50`  
		Last Modified: Mon, 16 Sep 2024 17:57:28 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json
