## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:6455ac31ed0d5f0fbd0f534ef3be9b18de5bda5d1c89e0482bc701d14d4e2bef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:17a0d8bc467497f4245007c0969e42c1c4e679c75932aa60ade0c88b166216c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.4 MB (343393677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd00528193253ec8633b53549063fe9fd16cb792aaf0baf86e5d4a09a1db93b6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.version=20251214.0.467559
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.revision=7bdde954b0e096cd16f488d38ae69035783e5862
# Thu, 18 Dec 2025 00:29:01 GMT
LABEL org.opencontainers.image.created=2025-12-14T00:07:15+00:00
# Thu, 18 Dec 2025 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251214.0.467559' /etc/os-release # buildkit
# Thu, 18 Dec 2025 00:29:09 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 00:29:09 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7b1e20b4fe65799151a60bf5d121f5f6f83fcd2aca9d80b1b2515a189308c3fd`  
		Last Modified: Mon, 15 Dec 2025 18:34:37 GMT  
		Size: 343.4 MB (343383370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a33c1bca70186f8c39bbc030c8d90520413062e000fe4f7bf591df1c2b5abd`  
		Last Modified: Thu, 18 Dec 2025 00:30:08 GMT  
		Size: 10.3 KB (10307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9c65c7622ac836cbe353b8a53e983ba743dc9b03e45a7c33a51e8a9cd41250d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12411722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d0ad4c303e019fc1250c5e620187a06087f0d6daa420d34789ed3110b4bcfe1`

```dockerfile
```

-	Layers:
	-	`sha256:6d9bab6330d8043df3604ceeb286b5a8f752c4f6d2831434175f45a330c42a4a`  
		Last Modified: Thu, 18 Dec 2025 02:48:31 GMT  
		Size: 12.4 MB (12399954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddaa5f6bf808068817ad2f978a0b0fc14400c0b2a367c5f05b32fdb966a238ee`  
		Last Modified: Thu, 18 Dec 2025 02:48:32 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
