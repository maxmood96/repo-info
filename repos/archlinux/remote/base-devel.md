## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:839e930e2fa6d6f2e0b2005402c42c42b4e4be030337e0a311b17678b517f657
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:8555624e8fd75d0a2e8f2f9a71f2c61b41501e41c5b07eb9cb0a3d1d7b630600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245813711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e946df517cb7ba7b9b11d514fc11b9bc55690008beb58122fca9645755b5c92`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.version=20260215.0.490969
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 17 Feb 2026 18:12:46 GMT
LABEL org.opencontainers.image.created=2026-02-15T00:06:54+00:00
# Tue, 17 Feb 2026 18:12:46 GMT
COPY /rootfs/ / # buildkit
# Tue, 17 Feb 2026 18:12:52 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260215.0.490969' /etc/os-release # buildkit
# Tue, 17 Feb 2026 18:12:52 GMT
ENV LANG=C.UTF-8
# Tue, 17 Feb 2026 18:12:52 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d56ae5d19c1d2f04ea452d8de4fea13755b24651da53787d2422b538a07bb424`  
		Last Modified: Tue, 17 Feb 2026 18:13:38 GMT  
		Size: 245.8 MB (245804589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba4a8dca53d5f3f5abcab43ef7f312f7fba6c98c2708a39fc0e7d5d18986e9`  
		Last Modified: Tue, 17 Feb 2026 18:13:34 GMT  
		Size: 9.1 KB (9122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:6c220e5d999ed75e22dbedf1a3e40b399fd67b6449af7b7c0d5aeb79e8f5cb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12233626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e8461ab9fac244de925df5a0292fee96e0e5ecab8aa3514547366f7398600`

```dockerfile
```

-	Layers:
	-	`sha256:25ae73fffaac92346a92a6aaeb0b895e9104cb2a93cb6b547bfb6638fa7b0b44`  
		Last Modified: Tue, 17 Feb 2026 18:13:34 GMT  
		Size: 12.2 MB (12221916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31952edc35976610789df4f03c0745e06ff562c48ad555d009adc47327e08a5`  
		Last Modified: Tue, 17 Feb 2026 18:13:34 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json
