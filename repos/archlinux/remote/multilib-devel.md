## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:973e63a746e98bc3dddf3413cd7cee3f6b9fc8de82514b6148247e2377fd8e75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5b0411eb075d715a50043661da62120614db5bfeeede079d14be45a98c3c3988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323695018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1db025db8e7ea6ea6026f5abf0bc67b2b86a3db26907f2e7a4193f849365ad3`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8c71d34480bb730e614fccaf4fdaec4f8fb129bdc3b8894eeedbb5c560a24b9f`  
		Last Modified: Mon, 16 Dec 2024 18:29:42 GMT  
		Size: 323.7 MB (323684798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c9ba2ebeeafc2947b037a964cae144a0560b9ba5bf49df78519b9e9df5ee6`  
		Last Modified: Mon, 16 Dec 2024 18:29:35 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9b0b66148c3b46fd3ef4defea8305e5e5614ceabd5bcd0a8c59d4a1428da343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12183700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf91482063b88dc991538a26f55253c47974bc0f31dc62473154ce9b6b8cea43`

```dockerfile
```

-	Layers:
	-	`sha256:1fa6c3dfe13b4f13991a156daa36781b8ca6336bf6421d0447e6925e039c885f`  
		Last Modified: Mon, 16 Dec 2024 18:29:36 GMT  
		Size: 12.2 MB (12171890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8257273bb029eed1577b8891c02891d90c29d7d69cd9ce7f14cc86c2ec2511c7`  
		Last Modified: Mon, 16 Dec 2024 18:29:35 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
