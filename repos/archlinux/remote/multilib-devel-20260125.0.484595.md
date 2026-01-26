## `archlinux:multilib-devel-20260125.0.484595`

```console
$ docker pull archlinux@sha256:851211871a857f4c39cc703205f3aa85f2b1a0a9cff021ece26eaf93235e960d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20260125.0.484595` - linux; amd64

```console
$ docker pull archlinux@sha256:de3b7b81814d75dac610d07a37c9fd8c3c18a1f39a01953cde0cf0447af0cb74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345103946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fced90a89536058b2bc132e511c546b05d84b700643e992b7e6c32a4d57320`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 26 Jan 2026 19:36:33 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Mon, 26 Jan 2026 19:36:33 GMT
COPY /rootfs/ / # buildkit
# Mon, 26 Jan 2026 19:36:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Mon, 26 Jan 2026 19:36:41 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 19:36:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b082aaf37d1f8448ecdf12a68276aa8babba8acde9f2d22a3396b4db41c0684d`  
		Last Modified: Mon, 26 Jan 2026 19:37:38 GMT  
		Size: 345.1 MB (345093462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ade524dd32242b793eb6b3bee4ac59174d6b53eb1308ba36b081931ef571bad`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 10.5 KB (10484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20260125.0.484595` - unknown; unknown

```console
$ docker pull archlinux@sha256:083a1414ca8b4ed7962181c42f413b0da2048aceab4152f3d6876a494811693b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12442787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d7e88a2d9fde05a5f7a6079b450d7a69db662ad4727c672d63d0c595fe564f`

```dockerfile
```

-	Layers:
	-	`sha256:38498fe0ce3a3f4c8fa23d7a31d195215881bab55b4cb1bb21f5f07aa40aa3ba`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 12.4 MB (12431019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4760a625a618838fa060efea86e8e33345f1053c49b3e6a7c99482708164a5`  
		Last Modified: Mon, 26 Jan 2026 19:37:29 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
