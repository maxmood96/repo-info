## `archlinux:multilib-devel-20240714.0.246936`

```console
$ docker pull archlinux@sha256:f77f1216dccbe2b6bac979ad9d15d8c7bdea1427e819bf0bccf28903b607ac7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240714.0.246936` - linux; amd64

```console
$ docker pull archlinux@sha256:0c0119d5d50de6828327a26d5d8456dd2b88b3ff3d73a1d9d01219375220eec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321414198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6d4c7d9ff9c616b20eaf607e77cd232a555a1b09c8fcbbdb50207d13f531e2`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20240714.0.246936
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 14 Jul 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-07-14T00:07:41+00:00
# Sun, 14 Jul 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240714.0.246936' /etc/os-release # buildkit
# Sun, 14 Jul 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 14 Jul 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:574ead718729478e82012992114b94cd6cd0c20a841ec243e96a2e52d690b52f`  
		Last Modified: Mon, 15 Jul 2024 20:03:08 GMT  
		Size: 321.4 MB (321403991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bda69f104b310390aac9c744b6a53a0051f0fd002f03d3f24b9398ca541dbe`  
		Last Modified: Mon, 15 Jul 2024 20:03:00 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240714.0.246936` - unknown; unknown

```console
$ docker pull archlinux@sha256:31983fa9823b2855d7bd067ad82fcfb09090b25978e93c43334878faa5520fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12066311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a400b999aa8af87af952079b49ef1714eba8016ed8b4c14ff6ed2c9acabc30`

```dockerfile
```

-	Layers:
	-	`sha256:742fc773e69ab5230202ee942be7ffe0a0577a26016a229eebcf9b29b4fe3510`  
		Last Modified: Mon, 15 Jul 2024 20:03:01 GMT  
		Size: 12.1 MB (12054751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37a1c1deddca3e59a74a1cc29ffff02cfb5c00be376740f673b7ace798331da`  
		Last Modified: Mon, 15 Jul 2024 20:03:00 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
