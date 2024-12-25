## `archlinux:multilib-devel-20241222.0.291122`

```console
$ docker pull archlinux@sha256:67704f0a23cb6c4f127cc0f273f9980ed295f7eb9ce427e6f4177c1a0f4d08bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241222.0.291122` - linux; amd64

```console
$ docker pull archlinux@sha256:06b88c7713d80627f71d38f3bc4098759e1f11efb3497f1a4b293d276d53651e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323697247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0847da9bca4d728a7ae8b61e844fa1da1971717e14d97beab7d4817b300361`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241222.0.291122
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-12-22T00:07:56+00:00
# Sun, 22 Dec 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241222.0.291122' /etc/os-release # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 22 Dec 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4bbe098a76a09b2e2fddeefd75ddf1e3f6efff78d5b7e29f298df0963e2d73a0`  
		Last Modified: Tue, 24 Dec 2024 21:33:42 GMT  
		Size: 323.7 MB (323687046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486374b3ba3fde819abf241b81da0fc83841d5d1200b2a96e256cbe76fb57a04`  
		Last Modified: Tue, 24 Dec 2024 21:33:35 GMT  
		Size: 10.2 KB (10201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241222.0.291122` - unknown; unknown

```console
$ docker pull archlinux@sha256:022e1290962ff7e859ae28f621c044d87973357c6a58ff2ddabfa5a984404cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12163576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bac4cde9a8fedfd5564b62cff4c324f9e8e14e080c9ffab534a426c613ab398`

```dockerfile
```

-	Layers:
	-	`sha256:1e933bbcc018b86add4a62ce900a0322c353dd7f9d4382cc4514ccf5329078d8`  
		Last Modified: Tue, 24 Dec 2024 21:33:36 GMT  
		Size: 12.2 MB (12151765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d0adb43149d3b3467b83b59975adae53ba0852d1e37ec3e09daf3a31b124f9a`  
		Last Modified: Tue, 24 Dec 2024 21:33:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
