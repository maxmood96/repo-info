## `archlinux:latest`

```console
$ docker pull archlinux@sha256:6de1a7bfb793f8d9e24a7d573234f60d011d16db546de5bd777b75707fd4aff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0ad58bc09ac5dc7ecdf43f5c2d221b23400dde42cbf3fb80e78c66046b941687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174702063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ead1ef039fbbda511c65e78867187fd636860f28f730e76f6c4611edd7ee5b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:45:56 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:45:56 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:46:00 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:46:00 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20856ddc4ee5b09c44cd703fdcd1da0f57d21ef8caa187e3a10bf779a45f1cf1`  
		Last Modified: Tue, 23 Dec 2025 20:48:33 GMT  
		Size: 174.7 MB (174693399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc1d7f7a8aa5d22544037dd9deddaee9f6566af860631995ff30b6e89b7fffa`  
		Last Modified: Tue, 23 Dec 2025 20:48:23 GMT  
		Size: 8.7 KB (8664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:40596493caab5ba46455b9e63e6ed339a00987189e4a7d424ee3d3480d0d7827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8395316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5145d5a218381984cac2862be053eef6b15e07d300b53e733676a140ae5065`

```dockerfile
```

-	Layers:
	-	`sha256:4dc37e756cc0d77c2318c75a70348b580ff40f542859cb2618d409e1358941ea`  
		Last Modified: Tue, 23 Dec 2025 20:48:17 GMT  
		Size: 8.4 MB (8383387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59babf91704b205b12b3453892a2c5823e20aaf34571a6b55478fe031d3fe819`  
		Last Modified: Tue, 23 Dec 2025 20:48:18 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
