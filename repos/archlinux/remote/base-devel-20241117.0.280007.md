## `archlinux:base-devel-20241117.0.280007`

```console
$ docker pull archlinux@sha256:b8906906ba3fc092362810f44a46e2efdd9bea0b86a075cf6d464301fe766fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241117.0.280007` - linux; amd64

```console
$ docker pull archlinux@sha256:7c8c5ee4da753afd1a63da937eb1bbb38ce586ef8e76d7838bbf6a5a38a30d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272453880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c71c86b853cfd8c37635aa1c227fefb2bb241a18d7db66b53418aaf16124381`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5b83ed2a07fc5b4755ce19ed6a1ac373d387788e07c69b468c6073cb817f4993`  
		Last Modified: Mon, 18 Nov 2024 19:06:01 GMT  
		Size: 272.4 MB (272444827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed70366604336ab8983a33dc73fff4ad41780e7bcec86e107c0e53987f67808`  
		Last Modified: Mon, 18 Nov 2024 19:05:57 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241117.0.280007` - unknown; unknown

```console
$ docker pull archlinux@sha256:74594d43463779a0e9b5064adcb68cb4b481100c6d9d2020720e93928b530493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2a1c23d3a723c92b8a8eee9b0e0ae234701055a81cd3189f487a8945c92225`

```dockerfile
```

-	Layers:
	-	`sha256:20137dc0db65abb533a40bf51f6b78e06af95c80873c342c71f3735fa5f7bbd0`  
		Last Modified: Mon, 18 Nov 2024 19:05:58 GMT  
		Size: 11.9 MB (11895700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6839eff8f9915f011a4f8e08cf641e6dc6de80281d37235b50d7f9b1728446`  
		Last Modified: Mon, 18 Nov 2024 19:05:57 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json
