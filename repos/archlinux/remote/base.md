## `archlinux:base`

```console
$ docker pull archlinux@sha256:6417af93a50740f2c88503b098e780c9edf5ee00aa156021c28bcfffe226f57d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:32ef0b1658af994e1a9be54043970c161c5b8ff2be057687bdb73a7e00fa9f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128328916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f1bdc4343b235a9f79259a7cfe88dd5013999144cbb2d88f329dc548b5b653`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.version=20260301.0.494762
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 02 Mar 2026 19:12:06 GMT
LABEL org.opencontainers.image.created=2026-03-01T00:06:43+00:00
# Mon, 02 Mar 2026 19:12:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260301.0.494762' /etc/os-release # buildkit
# Mon, 02 Mar 2026 19:12:10 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 19:12:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:30309458937ad265aaf28267249ee4c81fb36b01436042e1db699fbd376aae51`  
		Last Modified: Mon, 02 Mar 2026 19:12:36 GMT  
		Size: 128.3 MB (128320326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec592b6ce77ee4468ee080ecd79e1bc2f27389cb69b2c80752a7fd8080fc86`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 8.6 KB (8590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:186b9184d0d19d1a05967aa36da7d77d883c0b953fddfec571e2e7332b636d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8488859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d84ac9548c5ce774ad930f5e4c4d83b81f524654787834005b985690e0a997`

```dockerfile
```

-	Layers:
	-	`sha256:09304ff833801dc2643fd2617438e4e3143ae559b89f4e018972ce135a0fc764`  
		Last Modified: Mon, 02 Mar 2026 19:12:31 GMT  
		Size: 8.5 MB (8476930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fdcaf245f3775c930a42adf12c7f7dcb9b7384e41bcb134483417d3fcebd1d9`  
		Last Modified: Mon, 02 Mar 2026 19:12:30 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
