## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:597974c156be3b466a0cedb0b450766bd829662454545e3289221dfe876dbc21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0e001ad3f885fe9513e544ea99b312a3eae37d8215fee826b5dc84f9af5c14f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341113550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f03b1918cd1635881b2693dd1b8be969a7d45a37560f5b65e34a810339df5a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250921.0.423275
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 21 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-21T00:07:14+00:00
# Sun, 21 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250921.0.423275' /etc/os-release # buildkit
# Sun, 21 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 21 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:05c59540b3238557a896596168f7d03a73c3f68ec38fe506f2d8a4284d8d06e9`  
		Last Modified: Mon, 22 Sep 2025 20:02:38 GMT  
		Size: 341.1 MB (341103287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda24d2c9dd8dcb2064b1b05f2e896214bf788520ebc8622cdc250c3e2eee16d`  
		Last Modified: Mon, 22 Sep 2025 16:53:05 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c14fa21d2076c22888d3c2799f718653b8b22fb928390218d5fc83bb32b4fad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12398996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608e18bff9222928a445bccd1dd3350c3ffdba686fd848795802d32667c4c275`

```dockerfile
```

-	Layers:
	-	`sha256:810bcf02a4239cc21e8393bdca5be31c4b112888d9db15e188606b500977deef`  
		Last Modified: Mon, 22 Sep 2025 19:48:31 GMT  
		Size: 12.4 MB (12387185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15ab221638ce572d95472f09d6d451b6198e8c82171f00824664d9f40ed3a3f0`  
		Last Modified: Mon, 22 Sep 2025 19:48:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
