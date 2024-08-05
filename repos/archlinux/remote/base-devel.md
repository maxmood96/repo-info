## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c305b803b54a7877f8d551a4fe9a9f752e0e9864b8a1610b4e71bc7db4767884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:301e30d7e1f37a0a3ee30f2c4e1194446813e422e557abbcc3e7d7b49aecdf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271639364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1142d5059d74b3f69b4243adcdaf3f64c26262676d01521d86815307f0f3e08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.version=20240804.0.251467
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.created=2024-08-04T00:07:42+00:00
# Sun, 04 Aug 2024 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240804.0.251467' /etc/os-release # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 04 Aug 2024 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cd42ad71951d952b7df3bba39dc476212995b6bcba36ab9813fb49d17af1934d`  
		Last Modified: Mon, 05 Aug 2024 18:58:10 GMT  
		Size: 271.6 MB (271630324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95748fa34168a987aabf9f4e47214da0a18f81a9b58afcee78052328451a50`  
		Last Modified: Mon, 05 Aug 2024 18:58:06 GMT  
		Size: 9.0 KB (9040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c60ba377779485b8570900ecd1af26225233d49ed0e9c66392eff6798b1cc0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11805402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47612b8d80b046f3033455f3f996ba13afacf5a0cf051105d814edc991bd51f3`

```dockerfile
```

-	Layers:
	-	`sha256:f95a845709520dd0def02b2ad6103bbca4fadabe5f91b8f5563aa372b56614e3`  
		Last Modified: Mon, 05 Aug 2024 18:58:06 GMT  
		Size: 11.8 MB (11793899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d6cf7770cd2664ad92893518b2d1a9a9cbf945535bf4655576e235db172b2d`  
		Last Modified: Mon, 05 Aug 2024 18:58:06 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
