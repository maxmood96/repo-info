<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250504.0.344409`](#archlinuxbase-202505040344409)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250504.0.344409`](#archlinuxbase-devel-202505040344409)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250504.0.344409`](#archlinuxmultilib-devel-202505040344409)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:fcc0e315ba72175e77f5c351f1a79ff05fe5548431e842924b7b7cddb8240c08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:dd81e369a03ba6eb4f7f393c4cd301ea526ab4f55a295020ff801420c86f28d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160223578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7082ff5fac994457423065f5fdea3666a4b997f58104e4fc211c8aea24eaa228`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.version=20250427.0.341977
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.created=2025-04-27T00:07:36+00:00
# Sun, 27 Apr 2025 00:07:36 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250427.0.341977' /etc/os-release # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
ENV LANG=C.UTF-8
# Sun, 27 Apr 2025 00:07:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e18fb1fd7aa70b918f722641f4b9fd7ccbf14a4c10bbc5703fd8b3629d7316b8`  
		Last Modified: Mon, 28 Apr 2025 17:56:26 GMT  
		Size: 160.2 MB (160215211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24eb06ee43e332df084154c061500898f7a5a4afd81ac80a682e3d0f412fe2a`  
		Last Modified: Mon, 28 Apr 2025 17:56:16 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:ba660b65ebb337269a6cf93837c10a6a25dd706b21d10ddcc5e7556db7154661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8aabce9b779ef0c862d4477d380340fe42059584c12ead4d7ed0405a9216603`

```dockerfile
```

-	Layers:
	-	`sha256:c98a14340a37d51d0999d3525b0f5234909195a887c58d35714c9ddc75174a11`  
		Last Modified: Mon, 28 Apr 2025 17:56:17 GMT  
		Size: 8.2 MB (8164633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71858c18c25758d522bb71309d2824a90197c9fa317cc74dca37859594a0e3d5`  
		Last Modified: Mon, 28 Apr 2025 17:56:16 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250504.0.344409`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:d53a6f8e38e34d617d6da3635fa8be86568d7792838251cbb2d84d899dc8d752
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:919905a090e8d49ba5d7a1b62a26af6016389a085af0d0252f16985e2f457d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281771197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1c321285d574578c45f4d1dd1a74facdb5271887db7bf78f3d2a7e783a6f10`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.version=20250427.0.341977
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.created=2025-04-27T00:07:36+00:00
# Sun, 27 Apr 2025 00:07:36 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250427.0.341977' /etc/os-release # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
ENV LANG=C.UTF-8
# Sun, 27 Apr 2025 00:07:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:22e021f6cca4506347a8504ef5f7d98fb55f44265e6d381984cf83be8addc8b5`  
		Last Modified: Mon, 28 Apr 2025 17:56:34 GMT  
		Size: 281.8 MB (281762017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49958c0a82c2db177e9881e674cf552bfe465942bc6682b50c957d88399675c`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:78ab8f93f149ac6aa15e82b7b8d50f494de8ea994c9b18f27a5748c37eb66349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11998050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e855a60d201ea38495d8c496fad5e421ee1f776f1e325b588aad33af926cb4`

```dockerfile
```

-	Layers:
	-	`sha256:5f38931604a46f289adc88e5740283474134b52ed8e60b8a545e1a34b5f47d14`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 12.0 MB (11986296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2806408a7c642875f06e0ffab1769721eb5da70a433686ac43da0a8e3f181f9`  
		Last Modified: Mon, 28 Apr 2025 17:56:30 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250504.0.344409`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:fcc0e315ba72175e77f5c351f1a79ff05fe5548431e842924b7b7cddb8240c08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:dd81e369a03ba6eb4f7f393c4cd301ea526ab4f55a295020ff801420c86f28d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160223578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7082ff5fac994457423065f5fdea3666a4b997f58104e4fc211c8aea24eaa228`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.version=20250427.0.341977
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.created=2025-04-27T00:07:36+00:00
# Sun, 27 Apr 2025 00:07:36 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250427.0.341977' /etc/os-release # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
ENV LANG=C.UTF-8
# Sun, 27 Apr 2025 00:07:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:e18fb1fd7aa70b918f722641f4b9fd7ccbf14a4c10bbc5703fd8b3629d7316b8`  
		Last Modified: Mon, 28 Apr 2025 17:56:26 GMT  
		Size: 160.2 MB (160215211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24eb06ee43e332df084154c061500898f7a5a4afd81ac80a682e3d0f412fe2a`  
		Last Modified: Mon, 28 Apr 2025 17:56:16 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:ba660b65ebb337269a6cf93837c10a6a25dd706b21d10ddcc5e7556db7154661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8176604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8aabce9b779ef0c862d4477d380340fe42059584c12ead4d7ed0405a9216603`

```dockerfile
```

-	Layers:
	-	`sha256:c98a14340a37d51d0999d3525b0f5234909195a887c58d35714c9ddc75174a11`  
		Last Modified: Mon, 28 Apr 2025 17:56:17 GMT  
		Size: 8.2 MB (8164633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71858c18c25758d522bb71309d2824a90197c9fa317cc74dca37859594a0e3d5`  
		Last Modified: Mon, 28 Apr 2025 17:56:16 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:730c6a9a02deccc529aab379d4e1862461be510a49fd54c3c809d4104fee66a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:0ef15c9afbbce0bc61b86e0b1a1cccff48b886b2efeceb0992b25a0cd90d2365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331780513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a548c8d83b0af7a75c93f26629a75033fd47b085c8f3ef009b47a31e28550f72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.version=20250427.0.341977
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 27 Apr 2025 00:07:36 GMT
LABEL org.opencontainers.image.created=2025-04-27T00:07:36+00:00
# Sun, 27 Apr 2025 00:07:36 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250427.0.341977' /etc/os-release # buildkit
# Sun, 27 Apr 2025 00:07:36 GMT
ENV LANG=C.UTF-8
# Sun, 27 Apr 2025 00:07:36 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f65bc684ebcc882fc0c3c6bac39fe5e12352323433e0ae4ed3b90823f539b59a`  
		Last Modified: Mon, 28 Apr 2025 17:56:42 GMT  
		Size: 331.8 MB (331770222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbaa5643ba2de775c37e9d80d9254a5ea7a6210ea9732fa9a94815b9620ea2b`  
		Last Modified: Mon, 28 Apr 2025 17:56:37 GMT  
		Size: 10.3 KB (10291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2d2d59ebf71513f07e01139c7ffef315bb04b0021d79761b8131c1dec50e8a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12266647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6ec447bd0b3a2795e3c64c8bf442f45692c62af68507c98ee8b58f656d29a5`

```dockerfile
```

-	Layers:
	-	`sha256:b73d154edcc2141fc7e388ad0f2b9c20c8a5acf38bc82fbd93c1c456c7029961`  
		Last Modified: Mon, 28 Apr 2025 17:56:38 GMT  
		Size: 12.3 MB (12254836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8030ff0221cd09c9dacafcefc35b1fd821ef8248128b681226ca453f3f82661`  
		Last Modified: Mon, 28 Apr 2025 17:56:38 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250504.0.344409`

**does not exist** (yet?)
