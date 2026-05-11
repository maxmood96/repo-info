## `archlinux:base`

```console
$ docker pull archlinux@sha256:ceac417c19645d21630c120fa123942aa1fc5988faab14e67222013cb11f31bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:32c78c548c1a3f9db43bc25fb9f47d8bf5efff49a1da3810bb60790b4202d657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131511495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45009a24046a032770858133dc2c7f4b2eea1e6a3d906b75c56fb88f96f34fb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.version=20260510.0.525573
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Mon, 11 May 2026 20:56:45 GMT
LABEL org.opencontainers.image.created=2026-05-10T00:08:50+00:00
# Mon, 11 May 2026 20:56:45 GMT
COPY /rootfs/ / # buildkit
# Mon, 11 May 2026 20:56:48 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260510.0.525573' /etc/os-release &&     true # buildkit
# Mon, 11 May 2026 20:56:48 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 20:56:48 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3d6f988521c0f63d0d9be9472f740277503098197ef95adefcb2921bb2b446bd`  
		Last Modified: Mon, 11 May 2026 20:57:14 GMT  
		Size: 131.5 MB (131502821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eed74326c7599894f6babe815e15a3c9e7cb284a9522a087eefee14d20d9cf`  
		Last Modified: Mon, 11 May 2026 20:57:10 GMT  
		Size: 8.7 KB (8674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:6882afc9a444525dbb3a960636f1d4b9905610ce27ebe8e30044fa0130c1e1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5810a06a5b92fa08adce5ae7d52d7970a918174143ad4d9c686c1a34dd39331c`

```dockerfile
```

-	Layers:
	-	`sha256:b9dee7d539cec58db13f26a82812000611b74500f5b8147e558c440942cce1ef`  
		Last Modified: Mon, 11 May 2026 20:57:11 GMT  
		Size: 8.2 MB (8182986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ee1f5d25548a50f808be1213d6b539d0ae32f3e7799e4c55c922ac8c67696b`  
		Last Modified: Mon, 11 May 2026 20:57:10 GMT  
		Size: 12.0 KB (12007 bytes)  
		MIME: application/vnd.in-toto+json
