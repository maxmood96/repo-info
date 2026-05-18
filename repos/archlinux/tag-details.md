<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20260517.0.530531`](#archlinuxbase-202605170530531)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20260517.0.530531`](#archlinuxbase-devel-202605170530531)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20260517.0.530531`](#archlinuxmultilib-devel-202605170530531)

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

## `archlinux:base-20260517.0.530531`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:6ec1f5073a94d877ae97ebf68e507f709b395c7a90005fe92d9db1c21f933077
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:80ee11bda3cb40c46061bbc91db00e3eb8e6147cb17189b4dc9554e501c791a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254000910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed09359b140a8876e61214bec59f1cde93757b75162d07afdb5c04e9d01cab3f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.version=20260510.0.525573
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Mon, 11 May 2026 20:57:44 GMT
LABEL org.opencontainers.image.created=2026-05-10T00:08:50+00:00
# Mon, 11 May 2026 20:57:44 GMT
COPY /rootfs/ / # buildkit
# Mon, 11 May 2026 20:57:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260510.0.525573' /etc/os-release &&     true # buildkit
# Mon, 11 May 2026 20:57:49 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 20:57:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:45e67d8175df84610a18968cd899c0f1ca5acf749b8fc9a24dc8f7035e56010b`  
		Last Modified: Mon, 11 May 2026 20:58:35 GMT  
		Size: 254.0 MB (253991742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376abe05a3122ee96f2b50c9d6adf26e4ed30b70f3aecf3f320590b853e67f9d`  
		Last Modified: Mon, 11 May 2026 20:58:29 GMT  
		Size: 9.2 KB (9168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:73a825d32cfe541e3c112bdd851f6968e5ef241b4e88f3d8ef3e7015ca9e5f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (12048111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f1dfba0a6be5e8b752412b7682e85c615e71f08430b816c2697e4dca2c81fb`

```dockerfile
```

-	Layers:
	-	`sha256:ac3b99348eff9b35f9d117d7df1d35ae987c7d7b30a37b113788be2e3016cc22`  
		Last Modified: Mon, 11 May 2026 20:58:29 GMT  
		Size: 12.0 MB (12036322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08208c9270af4154939b3ffc42299b11b25c25113bb61ab7d9aabbdf36018946`  
		Last Modified: Mon, 11 May 2026 20:58:29 GMT  
		Size: 11.8 KB (11789 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20260517.0.530531`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ceac417c19645d21630c120fa123942aa1fc5988faab14e67222013cb11f31bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

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

### `archlinux:latest` - unknown; unknown

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

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:5649fdf8c653154c63de0060d73374896442000449782df138cc59b25d1cfa50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ff211158b1cd8274f3bb9c1acf9b4168161ab56f160b3907c12d4c5134265d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276392393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6ed11403ee45267b87af765a2d8a70c009f9c580084564438c6215a4e882d8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.version=20260510.0.525573
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.revision=b43ff00eac5d363450c033c3387cf566bc5650a0
# Mon, 11 May 2026 20:59:06 GMT
LABEL org.opencontainers.image.created=2026-05-10T00:08:50+00:00
# Mon, 11 May 2026 20:59:06 GMT
COPY /rootfs/ / # buildkit
# Mon, 11 May 2026 20:59:12 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260510.0.525573' /etc/os-release &&     true # buildkit
# Mon, 11 May 2026 20:59:12 GMT
ENV LANG=C.UTF-8
# Mon, 11 May 2026 20:59:12 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4fe2236d6036cbfee9f99ef331f485222aeb03985c18221fa01995136a88c822`  
		Last Modified: Mon, 11 May 2026 21:00:00 GMT  
		Size: 276.4 MB (276382020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fffb86b76bb626b28e556361bb2419fc9a6e2df10170906bf7a3a52202d8ee`  
		Last Modified: Mon, 11 May 2026 20:59:54 GMT  
		Size: 10.4 KB (10373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:ed33f8da54e0cb1b86cbc14c557eb9efc28d5765ae81d4b73dada291e16b714c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12318913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d4f0b7c493eb72e26740d1c9bc3ad6b3aec4e6db8c944f6920f8aa406b8647`

```dockerfile
```

-	Layers:
	-	`sha256:8f144e63e694b70b73393656fd5878787d571c0d3d74ba77e709c02f06157926`  
		Last Modified: Mon, 11 May 2026 20:59:55 GMT  
		Size: 12.3 MB (12307063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d019e227ac1e5a8d778de8b71114f66ad9a529ec2997bc9999c9993a44bde6`  
		Last Modified: Mon, 11 May 2026 20:59:54 GMT  
		Size: 11.8 KB (11850 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20260517.0.530531`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
