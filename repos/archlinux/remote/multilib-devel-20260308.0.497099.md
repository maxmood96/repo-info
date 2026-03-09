## `archlinux:multilib-devel-20260308.0.497099`

```console
$ docker pull archlinux@sha256:86bcf11a2af9cd87997f08806ca3c2a05d32af3161a9158aae5f95a08eaf019e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260308.0.497099` - linux; amd64

```console
$ docker pull archlinux@sha256:91471305f14d1bed5e4661f35c1429431365c76979b06520790f3812193ad21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268002870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6387a0e3ee19e7bf9612c69de2f89cf273838a7442cefbc9f309e38e1dcb07`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.version=20260308.0.497099
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 09 Mar 2026 17:59:26 GMT
LABEL org.opencontainers.image.created=2026-03-08T00:06:40+00:00
# Mon, 09 Mar 2026 17:59:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 09 Mar 2026 17:59:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260308.0.497099' /etc/os-release # buildkit
# Mon, 09 Mar 2026 17:59:31 GMT
ENV LANG=C.UTF-8
# Mon, 09 Mar 2026 17:59:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:262510de7e37ef25bb8872186940e06f3b8fce0ed8899d504cf10f7ca2fed259`  
		Last Modified: Mon, 09 Mar 2026 18:00:19 GMT  
		Size: 268.0 MB (267992546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17a20878b942e4b5f45e3f2c37fe8aaa04cc63d08eaa5cae076cd265a8c3e0b`  
		Last Modified: Mon, 09 Mar 2026 18:00:13 GMT  
		Size: 10.3 KB (10324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260308.0.497099` - unknown; unknown

```console
$ docker pull archlinux@sha256:c846217d0c3212b438bf8c659f05e356aaf026e314ccdfe732d92c72f73ec2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12167066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7b5746361122ba377504b95b7d2242b6cbb14a5592ba018e93a514ca14aa13`

```dockerfile
```

-	Layers:
	-	`sha256:89d1b3748bf48a88ab3dd44e22cd192f8541c6cc11475bb606802119ac38fc6c`  
		Last Modified: Mon, 09 Mar 2026 18:00:13 GMT  
		Size: 12.2 MB (12155298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cb7b585297a25f362afb00bcb9848679417aa1fdbcee09ea9a13de7fc3c5c9e`  
		Last Modified: Mon, 09 Mar 2026 18:00:14 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
