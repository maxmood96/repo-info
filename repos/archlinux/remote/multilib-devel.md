## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:adcffcfea1c51f5eec3c4148eeaaed1ac97d679e9b25f0bd0ec4e22c13f48c8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:88ee1f24b14bc630da17d6dd53a6db50c79c1ea5e53596d2e0c55f5d935a51ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337450182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c68b54b5dfb52d74e02d11581f0577772c742313566db82cb8cc6086cd737e5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.version=20250504.0.344409
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 04 May 2025 00:08:02 GMT
LABEL org.opencontainers.image.created=2025-05-04T00:08:01+00:00
# Sun, 04 May 2025 00:08:02 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 May 2025 00:08:02 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250504.0.344409' /etc/os-release # buildkit
# Sun, 04 May 2025 00:08:02 GMT
ENV LANG=C.UTF-8
# Sun, 04 May 2025 00:08:02 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a5e319f88d304e0213ee6c6ae459d746be69c6ef8cad6865299d35887f760047`  
		Last Modified: Mon, 05 May 2025 17:14:34 GMT  
		Size: 337.4 MB (337439881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5510fe49e46a4f921e21993c2caf96ecba65b6b58d1ce0c57681969c098510af`  
		Last Modified: Mon, 05 May 2025 17:14:29 GMT  
		Size: 10.3 KB (10301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:a65d55931814a0f691ef7d7647dd1fd180734235ce6affb9b8b1007d6a35965e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12306626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec5d6a911da22bb86057ce9f722660343cdadd2f5e2c4aa0734f11509db80a`

```dockerfile
```

-	Layers:
	-	`sha256:c19a59b5ce9192c347f7ea77e44239b3ed06e441fa8b286adb21a00c7eed0894`  
		Last Modified: Mon, 05 May 2025 17:14:29 GMT  
		Size: 12.3 MB (12294815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e64278f3ade57a2949068a02551b1800b42334ff052856754dc969cdc5bd0b0`  
		Last Modified: Mon, 05 May 2025 17:14:29 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
