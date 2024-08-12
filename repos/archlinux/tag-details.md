<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240811.0.253648`](#archlinuxbase-202408110253648)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240811.0.253648`](#archlinuxbase-devel-202408110253648)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240811.0.253648`](#archlinuxmultilib-devel-202408110253648)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:8491d740e45a25973466338d5dbd2c7df0ee8cfd63630a1670cbc460ed29c2e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0db05c077b83d0633ed5982360d72ac0be820ad44c795d30315ec1c8c8c98bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922403024bb4b5ff42ce62a5f4b881a44b00aec4882eb101cec0e12517f4a750`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.version=20240804.0.251467
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.created=2024-08-04T00:07:42+00:00
# Sun, 04 Aug 2024 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240804.0.251467' /etc/os-release # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 04 Aug 2024 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a6a8793ab4a390ccb9a9d4b63cdb245eb3554e35a10b6ec55fd9290d9f49b64b`  
		Last Modified: Mon, 05 Aug 2024 18:57:39 GMT  
		Size: 151.1 MB (151146462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81de2b29bdc9c6d44c28908121359cdeb092f385843c871c08d5e8ef2428fb8e`  
		Last Modified: Mon, 05 Aug 2024 18:57:37 GMT  
		Size: 8.3 KB (8281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:7cab0cd882bbcdef6a6e33c4e7b28a3dd4e911c15f45a632e09c7fcd3700efb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad285fffff5513cf1e8ed5aa0289246d7bf92affece23a024e97c9d5d073be77`

```dockerfile
```

-	Layers:
	-	`sha256:0a29d830aa9d47e8e716ee0fe9de65cf09842a86dc78c609c47d97ab740f161b`  
		Last Modified: Mon, 05 Aug 2024 18:57:37 GMT  
		Size: 8.1 MB (8103848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f3ad9550f0bbc894406f00141fa95e2df4bbabc6f0fccf6cb50cd0ca0fd8d80`  
		Last Modified: Mon, 05 Aug 2024 18:57:37 GMT  
		Size: 11.7 KB (11720 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240811.0.253648`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:c305b803b54a7877f8d551a4fe9a9f752e0e9864b8a1610b4e71bc7db4767884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:301e30d7e1f37a0a3ee30f2c4e1194446813e422e557abbcc3e7d7b49aecdf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271639364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1142d5059d74b3f69b4243adcdaf3f64c26262676d01521d86815307f0f3e08`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.version=20240804.0.251467
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.created=2024-08-04T00:07:42+00:00
# Sun, 04 Aug 2024 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240804.0.251467' /etc/os-release # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 04 Aug 2024 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cd42ad71951d952b7df3bba39dc476212995b6bcba36ab9813fb49d17af1934d`  
		Last Modified: Mon, 05 Aug 2024 18:58:10 GMT  
		Size: 271.6 MB (271630324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d95748fa34168a987aabf9f4e47214da0a18f81a9b58afcee78052328451a50`  
		Last Modified: Mon, 05 Aug 2024 18:58:06 GMT  
		Size: 9.0 KB (9040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c60ba377779485b8570900ecd1af26225233d49ed0e9c66392eff6798b1cc0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11805402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47612b8d80b046f3033455f3f996ba13afacf5a0cf051105d814edc991bd51f3`

```dockerfile
```

-	Layers:
	-	`sha256:f95a845709520dd0def02b2ad6103bbca4fadabe5f91b8f5563aa372b56614e3`  
		Last Modified: Mon, 05 Aug 2024 18:58:06 GMT  
		Size: 11.8 MB (11793899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22d6cf7770cd2664ad92893518b2d1a9a9cbf945535bf4655576e235db172b2d`  
		Last Modified: Mon, 05 Aug 2024 18:58:06 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240811.0.253648`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:8491d740e45a25973466338d5dbd2c7df0ee8cfd63630a1670cbc460ed29c2e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0db05c077b83d0633ed5982360d72ac0be820ad44c795d30315ec1c8c8c98bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151154743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922403024bb4b5ff42ce62a5f4b881a44b00aec4882eb101cec0e12517f4a750`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.version=20240804.0.251467
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.created=2024-08-04T00:07:42+00:00
# Sun, 04 Aug 2024 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240804.0.251467' /etc/os-release # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 04 Aug 2024 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a6a8793ab4a390ccb9a9d4b63cdb245eb3554e35a10b6ec55fd9290d9f49b64b`  
		Last Modified: Mon, 05 Aug 2024 18:57:39 GMT  
		Size: 151.1 MB (151146462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81de2b29bdc9c6d44c28908121359cdeb092f385843c871c08d5e8ef2428fb8e`  
		Last Modified: Mon, 05 Aug 2024 18:57:37 GMT  
		Size: 8.3 KB (8281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:7cab0cd882bbcdef6a6e33c4e7b28a3dd4e911c15f45a632e09c7fcd3700efb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad285fffff5513cf1e8ed5aa0289246d7bf92affece23a024e97c9d5d073be77`

```dockerfile
```

-	Layers:
	-	`sha256:0a29d830aa9d47e8e716ee0fe9de65cf09842a86dc78c609c47d97ab740f161b`  
		Last Modified: Mon, 05 Aug 2024 18:57:37 GMT  
		Size: 8.1 MB (8103848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f3ad9550f0bbc894406f00141fa95e2df4bbabc6f0fccf6cb50cd0ca0fd8d80`  
		Last Modified: Mon, 05 Aug 2024 18:57:37 GMT  
		Size: 11.7 KB (11720 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:16a5c1e25bbfe5de4d04944f5a6ebdf49e8517a14451cb9587f5185129467161
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6bb5912933272ebe9eb8e21a1b97993b1ab8e1ddaf274ae8f2280194afe479bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321524297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1161492424c04ae736a6eb14251b8e79163426b0213ec0d36a4fc58d172c66d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.version=20240804.0.251467
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 04 Aug 2024 00:07:42 GMT
LABEL org.opencontainers.image.created=2024-08-04T00:07:42+00:00
# Sun, 04 Aug 2024 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240804.0.251467' /etc/os-release # buildkit
# Sun, 04 Aug 2024 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 04 Aug 2024 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e84faef981553e49ef881afdcdc205918123010107a998eadc5fa3573a44ea81`  
		Last Modified: Mon, 05 Aug 2024 18:58:22 GMT  
		Size: 321.5 MB (321514113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c192d2661aebb550035aeda900a25ed59b022c0b42a6034031463bc6d15922`  
		Last Modified: Mon, 05 Aug 2024 18:58:17 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3c4820c32b6883e48ca2918725e3fac98d78fdd108f50f9a0df4a3091375479c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12072744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d23d9f92f8ddf22cb27652f9ad105de9bd761430fd75e65ebf4808b1b92b32e`

```dockerfile
```

-	Layers:
	-	`sha256:9a9d97c4003f6d5f3e2f4a28c5e4a3bd4cb74ad2ff52ace3fe11446af6fa7df0`  
		Last Modified: Mon, 05 Aug 2024 18:58:17 GMT  
		Size: 12.1 MB (12061186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2de089a1b11192ab1bee8c4ab60f7aa1e0b020b4f6557f630fe3e7102cdd098`  
		Last Modified: Mon, 05 Aug 2024 18:58:17 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240811.0.253648`

**does not exist** (yet?)
