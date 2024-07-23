## `archlinux:base`

```console
$ docker pull archlinux@sha256:76fbb2a91a9c06b05372eb2c2e0a0edf19a864258284e2dad2002c96f776c031
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:26355e4be5736c53efac48531b80d0ea1b32513e7e5d972098dd21a17cd72e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e895e05153b430a2a12984c31a25e52e9d23ab3bc71f1a314ccca1dd2171ae7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d60d5665bb190f639c1d4f286977018d4342bc47593af30e0b92968fe432d0bc`  
		Last Modified: Mon, 22 Jul 2024 19:59:06 GMT  
		Size: 151.1 MB (151080489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56de0cb20f43c946371788cf57a2e4218c3aef7c9f3b5e136296f03f54645dfb`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 8.3 KB (8291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:73075f0609136245902753e42fecec5b3bfcbd6bc13fbc7d518eb17bd66b4955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f95a0f7c288ccfb9d74945c79034e1da3d3df3b73508815159f4b796787a5f`

```dockerfile
```

-	Layers:
	-	`sha256:29241b1b22ea97bde5a201e66a13d3fdf2048792ab418e5f03ac7f197a0a9a88`  
		Last Modified: Mon, 22 Jul 2024 19:59:04 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5030466b8633e0e22c1645a53d8de4cb31d8fb8a7026642e5e524adbbecba71`  
		Last Modified: Mon, 22 Jul 2024 19:59:03 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
