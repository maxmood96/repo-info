## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:331b6b59d467abd4147d96cce5e4e898f70831247535bb132c92bb42b9fc0e7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:98ae1574320b75c976dc1b06c8842b7f423a419a0412e52db57182f5e1204c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323274751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f71697d69e335877143ef3db8c9be57d5e65b1bb6cc3323d4d3c228048de09`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.version=20241208.0.286830
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.created=2024-12-08T00:07:49+00:00
# Sun, 08 Dec 2024 00:07:49 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241208.0.286830' /etc/os-release # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Sun, 08 Dec 2024 00:07:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:85bf5fc2a5d09aa85a801947ae693f0790594124d9b5fec35315198a760bd3c9`  
		Last Modified: Mon, 09 Dec 2024 19:29:25 GMT  
		Size: 323.3 MB (323264555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6003d38f7667dc01b94e86f186c6b6991a0073ff6540a0a1d2f41b6bdd81b125`  
		Last Modified: Mon, 09 Dec 2024 19:29:20 GMT  
		Size: 10.2 KB (10196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:056279a3c32abee047977ed1d3fa4a7eb83f2cec748da7aaef170137039928a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12177618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8778e4469093ce2b77e8127d89850e12145115b7bf643a2bec6f31615398ae11`

```dockerfile
```

-	Layers:
	-	`sha256:2ef5e53052b4ca164a85cdcaccd97d2723f8c1ea6d31c8a7b1c9ae8f33b6d7f3`  
		Last Modified: Mon, 09 Dec 2024 19:29:20 GMT  
		Size: 12.2 MB (12165807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964d4d9ea5fb6ac9632b11d9980a82ce9d2550daed26b61509ca61bfc29fe570`  
		Last Modified: Mon, 09 Dec 2024 19:29:20 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
