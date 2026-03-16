## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9f93fc410174cc8c461a733d5e84c636953e0cace5e26fb703a2bac4dc20883b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:1723ca2122ed3d1fe388bd48d6cd6071e26c18fb83b98c145c87ec16250ef43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268113548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1f6f26373a20f5464d36ea04b76637aa92df15f290c4f6d0e6c9ed39abfcb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.version=20260315.0.500537
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 16 Mar 2026 16:43:14 GMT
LABEL org.opencontainers.image.created=2026-03-15T00:06:55+00:00
# Mon, 16 Mar 2026 16:43:14 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Mar 2026 16:43:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260315.0.500537' /etc/os-release # buildkit
# Mon, 16 Mar 2026 16:43:20 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 16:43:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9585199d402ed4a8daa2621af9bef196ee78246c0b82a569389353b29e3d6d47`  
		Last Modified: Mon, 16 Mar 2026 16:44:19 GMT  
		Size: 268.1 MB (268103225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ec90be4bc540148d43ef202747b0d81081c54c38cdb6b7da7dc282014e2bee`  
		Last Modified: Mon, 16 Mar 2026 16:44:05 GMT  
		Size: 10.3 KB (10323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:310a3ecfde65c5d865304617198204fdf01810c5278521cd742e05518a62dab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12168354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da9feb30b550b19b8feb3609d52cbeba7ddb0f6f576c10f34bb9a0b951e7d1b9`

```dockerfile
```

-	Layers:
	-	`sha256:3a23b6f972d8163e5c2a602d9635ffb4d3e7411524be03f82d66c4711387768f`  
		Last Modified: Mon, 16 Mar 2026 16:44:06 GMT  
		Size: 12.2 MB (12156586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90cd3a4741716d55f07ee42cbc4f25640ec9a74d4fccbef2f4ca77cb688a414`  
		Last Modified: Mon, 16 Mar 2026 16:44:05 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
