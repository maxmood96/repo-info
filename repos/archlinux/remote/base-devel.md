## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0a03ad573989e8df9d62ac9d52600a6fb0778016bf5990716a19063e05ebe3c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3a7cfcea321a33e492d28e1ba7faa09c7116fa0b18130b0e313afc6e112db4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292239239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c7c42a0ceccb0d9acbbcde3b86dc975ab88abc0a5a3f636f845eeda15e7992`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.version=20251221.0.472429
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 23 Dec 2025 17:47:14 GMT
LABEL org.opencontainers.image.created=2025-12-21T00:07:18+00:00
# Tue, 23 Dec 2025 17:47:14 GMT
COPY /rootfs/ / # buildkit
# Tue, 23 Dec 2025 17:47:21 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251221.0.472429' /etc/os-release # buildkit
# Tue, 23 Dec 2025 17:47:21 GMT
ENV LANG=C.UTF-8
# Tue, 23 Dec 2025 17:47:21 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:89181a90e29d471acbe88cfa5249d4c5667ae6f755e5b0ee25efa11e859ecd1e`  
		Last Modified: Tue, 23 Dec 2025 20:50:24 GMT  
		Size: 292.2 MB (292230049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1a51baa86ca2df506297f2f8b201e37e45d83a13dee8bea2896ef70f3a91b0`  
		Last Modified: Tue, 23 Dec 2025 20:50:10 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8beeca215f557f2c746b24efcf35d95c4ca24ef4e9b6c83ffccf67319fef015b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12157440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cba3e49d6c249b4f7940b31acb8ac22cd5aaf74d1183338616074247b9a1529`

```dockerfile
```

-	Layers:
	-	`sha256:12e3b44f6616703d84d4a038f5da6fcf8b277c544ecd2b9192d383cd5be52b7d`  
		Last Modified: Tue, 23 Dec 2025 20:48:25 GMT  
		Size: 12.1 MB (12145730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0247de5bb34306e5acc92458b0ccea9a310e19bb8ab7fb36cee08dc92b0b3d0`  
		Last Modified: Tue, 23 Dec 2025 20:48:26 GMT  
		Size: 11.7 KB (11710 bytes)  
		MIME: application/vnd.in-toto+json
