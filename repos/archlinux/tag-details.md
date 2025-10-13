<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20251012.0.434149`](#archlinuxbase-202510120434149)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20251012.0.434149`](#archlinuxbase-devel-202510120434149)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20251012.0.434149`](#archlinuxmultilib-devel-202510120434149)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:0423e31111e93087aef7a46f999a91e892a8d1b49e9de939e3e660e34ce42fe8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:c7f7b9545dd34e5e990b3dba126ac890dca86a19a76931d0de121fad65ba0830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165313794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db23cb19a4c6eca9c4cf961d71db72d3f5c248008bd8de249deab687952155ca`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:25614b3b15cb8475f385228ace25cfdcdc8d8dfcd68fd1ec0ad41ef2a0b6a5b7`  
		Last Modified: Mon, 13 Oct 2025 17:57:18 GMT  
		Size: 165.3 MB (165305454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c93813b9937c66e353d01fc7b735a1adc10009c67423b0aab18ec1ed5e86857`  
		Last Modified: Mon, 13 Oct 2025 17:57:08 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:c7ef8dbfe8001330188cc9e181a2808d99d9a63ac664b941ad8139369bd9f77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ada5774aa56fe9940eda50ff0140f7c6302f446a7efc8c4031f7df7d314f84`

```dockerfile
```

-	Layers:
	-	`sha256:31f2e6481e4179f7706a75b3895be983357599af96ab71a311bd7a2e2b884b06`  
		Last Modified: Mon, 13 Oct 2025 19:48:17 GMT  
		Size: 8.2 MB (8217611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798bcd34d6e682ba6aaadb75bd492c7c101a5883c926e86a59b1c7a8f3277d20`  
		Last Modified: Mon, 13 Oct 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251012.0.434149`

```console
$ docker pull archlinux@sha256:0423e31111e93087aef7a46f999a91e892a8d1b49e9de939e3e660e34ce42fe8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20251012.0.434149` - linux; amd64

```console
$ docker pull archlinux@sha256:c7f7b9545dd34e5e990b3dba126ac890dca86a19a76931d0de121fad65ba0830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165313794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db23cb19a4c6eca9c4cf961d71db72d3f5c248008bd8de249deab687952155ca`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:25614b3b15cb8475f385228ace25cfdcdc8d8dfcd68fd1ec0ad41ef2a0b6a5b7`  
		Last Modified: Mon, 13 Oct 2025 17:57:18 GMT  
		Size: 165.3 MB (165305454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c93813b9937c66e353d01fc7b735a1adc10009c67423b0aab18ec1ed5e86857`  
		Last Modified: Mon, 13 Oct 2025 17:57:08 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20251012.0.434149` - unknown; unknown

```console
$ docker pull archlinux@sha256:c7ef8dbfe8001330188cc9e181a2808d99d9a63ac664b941ad8139369bd9f77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ada5774aa56fe9940eda50ff0140f7c6302f446a7efc8c4031f7df7d314f84`

```dockerfile
```

-	Layers:
	-	`sha256:31f2e6481e4179f7706a75b3895be983357599af96ab71a311bd7a2e2b884b06`  
		Last Modified: Mon, 13 Oct 2025 19:48:17 GMT  
		Size: 8.2 MB (8217611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798bcd34d6e682ba6aaadb75bd492c7c101a5883c926e86a59b1c7a8f3277d20`  
		Last Modified: Mon, 13 Oct 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:87a967f07ba6319fc35c8c4e6ce6acdb4343b57aa817398a5d2db57bd8edc731
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3f87d6fd1d3575adf372fc3a89d121ada49c739e6874b686929a0c7688f96e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290402693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce4eac8f0e1b2294a65f237e72d1c2f1245917250421c5971f44720cf75a73e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:40a5c65700b7d7b9416f35272ff2779a3f3035c353228939aa7268bd91207d0b`  
		Last Modified: Mon, 13 Oct 2025 19:49:57 GMT  
		Size: 290.4 MB (290393539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b296d3961febf0ff21ae29828097127758a3e0c33c1d9a773190e62c10f5b`  
		Last Modified: Mon, 13 Oct 2025 18:11:15 GMT  
		Size: 9.2 KB (9154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:87221a39386272fb2224c1d549abad3a1006068b2e114c388e7197ffa7e45589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af776174d14756c9c8e7b84f821c6f233a5dd6220db892b39b36b6b28992398`

```dockerfile
```

-	Layers:
	-	`sha256:dc43627b48bcccd7efc9e7e39b71658b9413cd55547fba96351b98e9b58b70fe`  
		Last Modified: Mon, 13 Oct 2025 19:48:23 GMT  
		Size: 12.1 MB (12118947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f5e55db58632671fc5395c94a39ce7582e9b2a90267a2bcf9a4c4ef30aa968`  
		Last Modified: Mon, 13 Oct 2025 19:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251012.0.434149`

```console
$ docker pull archlinux@sha256:87a967f07ba6319fc35c8c4e6ce6acdb4343b57aa817398a5d2db57bd8edc731
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20251012.0.434149` - linux; amd64

```console
$ docker pull archlinux@sha256:3f87d6fd1d3575adf372fc3a89d121ada49c739e6874b686929a0c7688f96e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290402693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce4eac8f0e1b2294a65f237e72d1c2f1245917250421c5971f44720cf75a73e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:40a5c65700b7d7b9416f35272ff2779a3f3035c353228939aa7268bd91207d0b`  
		Last Modified: Mon, 13 Oct 2025 19:49:57 GMT  
		Size: 290.4 MB (290393539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1b296d3961febf0ff21ae29828097127758a3e0c33c1d9a773190e62c10f5b`  
		Last Modified: Mon, 13 Oct 2025 18:11:15 GMT  
		Size: 9.2 KB (9154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20251012.0.434149` - unknown; unknown

```console
$ docker pull archlinux@sha256:87221a39386272fb2224c1d549abad3a1006068b2e114c388e7197ffa7e45589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12130701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af776174d14756c9c8e7b84f821c6f233a5dd6220db892b39b36b6b28992398`

```dockerfile
```

-	Layers:
	-	`sha256:dc43627b48bcccd7efc9e7e39b71658b9413cd55547fba96351b98e9b58b70fe`  
		Last Modified: Mon, 13 Oct 2025 19:48:23 GMT  
		Size: 12.1 MB (12118947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f5e55db58632671fc5395c94a39ce7582e9b2a90267a2bcf9a4c4ef30aa968`  
		Last Modified: Mon, 13 Oct 2025 19:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:0423e31111e93087aef7a46f999a91e892a8d1b49e9de939e3e660e34ce42fe8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:c7f7b9545dd34e5e990b3dba126ac890dca86a19a76931d0de121fad65ba0830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165313794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db23cb19a4c6eca9c4cf961d71db72d3f5c248008bd8de249deab687952155ca`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:25614b3b15cb8475f385228ace25cfdcdc8d8dfcd68fd1ec0ad41ef2a0b6a5b7`  
		Last Modified: Mon, 13 Oct 2025 17:57:18 GMT  
		Size: 165.3 MB (165305454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c93813b9937c66e353d01fc7b735a1adc10009c67423b0aab18ec1ed5e86857`  
		Last Modified: Mon, 13 Oct 2025 17:57:08 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:c7ef8dbfe8001330188cc9e181a2808d99d9a63ac664b941ad8139369bd9f77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8229583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ada5774aa56fe9940eda50ff0140f7c6302f446a7efc8c4031f7df7d314f84`

```dockerfile
```

-	Layers:
	-	`sha256:31f2e6481e4179f7706a75b3895be983357599af96ab71a311bd7a2e2b884b06`  
		Last Modified: Mon, 13 Oct 2025 19:48:17 GMT  
		Size: 8.2 MB (8217611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798bcd34d6e682ba6aaadb75bd492c7c101a5883c926e86a59b1c7a8f3277d20`  
		Last Modified: Mon, 13 Oct 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:c2c53d463f00eecf02ba3f3bb4035cf4fb01b0937329a9043b848eb8d5a73820
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:90cf52c153f13d76d3e9f0049cae9d5bbb0d19a9cc432d2dda15d9eed81a983b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341722455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b304069c628e718c14841fb8537473e9dc595abc3e3f85b592eb97a2620a8b5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f4207c155a5d4e78745234ffe4f665ad0c58299bde28ced8e73f91fefb05c2f7`  
		Last Modified: Mon, 13 Oct 2025 20:08:45 GMT  
		Size: 341.7 MB (341712195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d78f276a546ef06488eca8700198fd0f1051dc02511ecf5ec4e0ed903d8bb`  
		Last Modified: Mon, 13 Oct 2025 17:58:28 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f6beada9dbed10e61f7f41ac38e9e7236eca1c44504f97db4af9636cde19e60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12399546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43065518a2fb97b4dbf8b62cd23ee1b3164d6f77d7c748bc83c585dec0204e06`

```dockerfile
```

-	Layers:
	-	`sha256:c9d16b54bbed4a9fef9d38691df582544e791c1f1d3a56f1614a3ab55c50e61e`  
		Last Modified: Mon, 13 Oct 2025 19:48:32 GMT  
		Size: 12.4 MB (12387735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01bd7d92fab6d6f458dbd52b87b59f5215048542ea41882846d84015a9741e5`  
		Last Modified: Mon, 13 Oct 2025 19:48:33 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251012.0.434149`

```console
$ docker pull archlinux@sha256:c2c53d463f00eecf02ba3f3bb4035cf4fb01b0937329a9043b848eb8d5a73820
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20251012.0.434149` - linux; amd64

```console
$ docker pull archlinux@sha256:90cf52c153f13d76d3e9f0049cae9d5bbb0d19a9cc432d2dda15d9eed81a983b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341722455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b304069c628e718c14841fb8537473e9dc595abc3e3f85b592eb97a2620a8b5`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.version=20251012.0.434149
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.revision=2ae497c16d7647c505b1cb39e19659d26193a5a0
# Sun, 12 Oct 2025 00:07:08 GMT
LABEL org.opencontainers.image.created=2025-10-12T00:07:08+00:00
# Sun, 12 Oct 2025 00:07:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251012.0.434149' /etc/os-release # buildkit
# Sun, 12 Oct 2025 00:07:08 GMT
ENV LANG=C.UTF-8
# Sun, 12 Oct 2025 00:07:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f4207c155a5d4e78745234ffe4f665ad0c58299bde28ced8e73f91fefb05c2f7`  
		Last Modified: Mon, 13 Oct 2025 20:08:45 GMT  
		Size: 341.7 MB (341712195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872d78f276a546ef06488eca8700198fd0f1051dc02511ecf5ec4e0ed903d8bb`  
		Last Modified: Mon, 13 Oct 2025 17:58:28 GMT  
		Size: 10.3 KB (10260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20251012.0.434149` - unknown; unknown

```console
$ docker pull archlinux@sha256:f6beada9dbed10e61f7f41ac38e9e7236eca1c44504f97db4af9636cde19e60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12399546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43065518a2fb97b4dbf8b62cd23ee1b3164d6f77d7c748bc83c585dec0204e06`

```dockerfile
```

-	Layers:
	-	`sha256:c9d16b54bbed4a9fef9d38691df582544e791c1f1d3a56f1614a3ab55c50e61e`  
		Last Modified: Mon, 13 Oct 2025 19:48:32 GMT  
		Size: 12.4 MB (12387735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a01bd7d92fab6d6f458dbd52b87b59f5215048542ea41882846d84015a9741e5`  
		Last Modified: Mon, 13 Oct 2025 19:48:33 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
