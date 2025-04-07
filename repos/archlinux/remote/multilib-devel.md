## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:b625f5d64812272a2969596a861d0fc2f9c88a391b9f7de7ca29a33cdbf4ec57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:4f2d98923a12665dd8520030d87bc54a15bd177437a78d20f673aba40ab3fd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331542097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54118882a98d870564b8c805d01b3a4dba5a0a1d98fb671cfb926a1c771ae34`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250406.0.331908
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-04-06T00:07:28+00:00
# Sun, 06 Apr 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250406.0.331908' /etc/os-release # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 06 Apr 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2b1771da912aba432c25dc8e466887ca1f92e7e753002ba2052e82815b5fca8f`  
		Last Modified: Mon, 07 Apr 2025 18:09:03 GMT  
		Size: 331.5 MB (331531784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056af4e3a52ede0d2a6b35a9a32d5396a3e311ab645a4b5938247a7729841ac9`  
		Last Modified: Mon, 07 Apr 2025 18:08:53 GMT  
		Size: 10.3 KB (10313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd907aa0b6a448746dcd77343f6765718774c79232906c1518efc840d3a692e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12262924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb700d418fafc1057559825d021cdf42bcae165187de01dda63716e2a919a6c`

```dockerfile
```

-	Layers:
	-	`sha256:e995abc01400339b580f5eebaeb8f6e7cc5bf5d0afb64ef92b03a95cd15ea500`  
		Last Modified: Mon, 07 Apr 2025 18:08:53 GMT  
		Size: 12.3 MB (12251113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59fb6373dfaee771421b1ae9f86e3bff2b882fa4f41ea15ffbda2359b6838aa9`  
		Last Modified: Mon, 07 Apr 2025 18:08:53 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
