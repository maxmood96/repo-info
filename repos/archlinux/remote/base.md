## `archlinux:base`

```console
$ docker pull archlinux@sha256:4585b6322b40a28877dbe2363c7281dd046d9289300a36f58edc207ed1c8db90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:09e04a8a3e454c0c3349a57cd55723300d675aaa3c9316583f4e092290a9e241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176268096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565265df54812b4519894e6d690dd2b19d5d1fefc81e8bb325e4ccc2fb729c60`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.version=20260125.0.484595
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Wed, 28 Jan 2026 02:14:25 GMT
LABEL org.opencontainers.image.created=2026-01-25T00:06:59+00:00
# Wed, 28 Jan 2026 02:14:25 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260125.0.484595' /etc/os-release # buildkit
# Wed, 28 Jan 2026 02:14:28 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:14:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:53d8c63f0ad88bc2d676416ee3944854719f04009c45944d88d5fc62b58a46d2`  
		Last Modified: Mon, 26 Jan 2026 19:35:56 GMT  
		Size: 176.3 MB (176259322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb0318c5d907dd630183122cc0e398efa682d9e87262c08e1a42453f89881cb`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:978f9926de3a1e20127fdb92661d4e1963e30aa0b573899b0fe90f179a01e346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8410748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7462992050a70ad73f1d556e805d8785a19ffdd471d169d8897483e4c9ae3fd`

```dockerfile
```

-	Layers:
	-	`sha256:c2609cd1cc40277c4e3ccd82558b96c15ea9128a314d16a3b7042079b560ee50`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 8.4 MB (8398819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d81a3b55b35bade08946f84782dd563d97c014bcfbea47f897fc1eb7badd30`  
		Last Modified: Wed, 28 Jan 2026 02:14:56 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
