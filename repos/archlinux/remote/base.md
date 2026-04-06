## `archlinux:base`

```console
$ docker pull archlinux@sha256:b4df475619469581537637ceaace6075f4912ea1cd6db6b99d463e3a72969d04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:bada17b14eeb70c3926e67951ac95291548c25a4b4c83b73c846838e5e292700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128815340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0861fbb9176ee3054b4213768d899fcaa75ed245638766f323fa8f8a81d439b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.version=20260405.0.511327
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 06 Apr 2026 18:07:40 GMT
LABEL org.opencontainers.image.created=2026-04-05T00:07:03+00:00
# Mon, 06 Apr 2026 18:07:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 06 Apr 2026 18:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260405.0.511327' /etc/os-release # buildkit
# Mon, 06 Apr 2026 18:07:42 GMT
ENV LANG=C.UTF-8
# Mon, 06 Apr 2026 18:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9ea86d6f9b5d6505c95a0472fee5fc3797e6b14e31f3f8d9907664194475576`  
		Last Modified: Mon, 06 Apr 2026 18:08:08 GMT  
		Size: 128.8 MB (128806757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd69c77b3164c13f3b81ca340f9329fe8cd6ab2d5b0a767ed9438c9ce57e086`  
		Last Modified: Mon, 06 Apr 2026 18:08:04 GMT  
		Size: 8.6 KB (8583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:1429e29b3e97f6373434a9ce20d6378dbe0aa43e0f7d4b7f6f70d011ce6e3717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8161782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775bda38ab896d13059ff45727e36db3eb165c71145e061ce32cbcab69390baa`

```dockerfile
```

-	Layers:
	-	`sha256:9393903773d2b6d03edb153adeeb133754d305ec85b78da2d4fcf12cee9c9914`  
		Last Modified: Mon, 06 Apr 2026 18:08:05 GMT  
		Size: 8.1 MB (8149853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8956b74e0052461ee4aa05135480c83f001d32562eb5be820af55c3e1b6be179`  
		Last Modified: Mon, 06 Apr 2026 18:08:05 GMT  
		Size: 11.9 KB (11929 bytes)  
		MIME: application/vnd.in-toto+json
