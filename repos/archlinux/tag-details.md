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
$ docker pull archlinux@sha256:287bf95d97e4f952a94a1f4a83008c6a547405bacc44173bda151231a3c843aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:2fcdd55448255f87dd337ef5c0fdbd5e4fec432345db1aa5faea4bf2764b4ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165272341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9925fab8d3a14258be073f974b684d4e3c0dca839377532315bc0ee5eb518463`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f76ba238a84a63b71e658023be058526928f3de0dcb19747c2a10d5a20567f04`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 165.3 MB (165263996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433a31b7d4e549851b2b1b22b37d84ace4122c21d1306cabef775c79b768e9d`  
		Last Modified: Wed, 08 Oct 2025 22:17:30 GMT  
		Size: 8.3 KB (8345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:5bc4356d023bc6436fa562af8aab4c70d81ef6f2217668dcbac5df92a0e00932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c212077f98283752080e16cd84308808b4e5a6e48c482e92ba0ea011cc35d1`

```dockerfile
```

-	Layers:
	-	`sha256:dd3da87224e2605d5a9f6bafcfe74158dadc7b2f93e29df5d86cad4f4f210ec4`  
		Last Modified: Thu, 09 Oct 2025 01:48:16 GMT  
		Size: 8.2 MB (8218248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b217a78d6ac772cf60fbe59f8a67b70089940e7c9d30e29798b9b96ec644999`  
		Last Modified: Thu, 09 Oct 2025 01:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20251012.0.434149`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:06ab929f935145dd65994a89dd06651669ea28d43c812f3e24de990978511821
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:30dc190c4baad79bec6c090ab5e191971c047bdbf46a42dc0b9f96f76ed8829c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290344778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2eea33bc78b82446896bba5041f365f4673f14a4b911faa3e1e9e3a40230e67`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:31bd40284997e57aafb1578009aa7ac3eb161d57ef18a8620487b68765949955`  
		Last Modified: Mon, 06 Oct 2025 19:48:54 GMT  
		Size: 290.3 MB (290335625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b88a441effdd8287e2e42f35004762e13b92b7480aea9d88eddd9fb5476def1`  
		Last Modified: Wed, 08 Oct 2025 22:17:28 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f7292395dfad4dc5ec10af2544719fbaae94fafd8aa1a8314460abe641182df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12131338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46ce5463edc30aed1e21f629b2534e5d4b36b06ebf94432cc83f632200065f`

```dockerfile
```

-	Layers:
	-	`sha256:f83ae8a539ccc59097f9ffbb130234faf5bb2e9b7f57d3a7b5a89fe65c27b7ec`  
		Last Modified: Thu, 09 Oct 2025 01:48:23 GMT  
		Size: 12.1 MB (12119584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc55e6c33fa26628a504a97fae9f502aeb81c37cb8cc1e77be0594c9bd712b00`  
		Last Modified: Thu, 09 Oct 2025 01:48:24 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20251012.0.434149`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:287bf95d97e4f952a94a1f4a83008c6a547405bacc44173bda151231a3c843aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2fcdd55448255f87dd337ef5c0fdbd5e4fec432345db1aa5faea4bf2764b4ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165272341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9925fab8d3a14258be073f974b684d4e3c0dca839377532315bc0ee5eb518463`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:f76ba238a84a63b71e658023be058526928f3de0dcb19747c2a10d5a20567f04`  
		Last Modified: Mon, 06 Oct 2025 19:48:34 GMT  
		Size: 165.3 MB (165263996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433a31b7d4e549851b2b1b22b37d84ace4122c21d1306cabef775c79b768e9d`  
		Last Modified: Wed, 08 Oct 2025 22:17:30 GMT  
		Size: 8.3 KB (8345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:5bc4356d023bc6436fa562af8aab4c70d81ef6f2217668dcbac5df92a0e00932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c212077f98283752080e16cd84308808b4e5a6e48c482e92ba0ea011cc35d1`

```dockerfile
```

-	Layers:
	-	`sha256:dd3da87224e2605d5a9f6bafcfe74158dadc7b2f93e29df5d86cad4f4f210ec4`  
		Last Modified: Thu, 09 Oct 2025 01:48:16 GMT  
		Size: 8.2 MB (8218248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b217a78d6ac772cf60fbe59f8a67b70089940e7c9d30e29798b9b96ec644999`  
		Last Modified: Thu, 09 Oct 2025 01:48:17 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9f6f04ef67cea4f618e10c45817c50dbd7e575bddff5fa4d71a38ac55bcc781b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3b8be9f0edbf296a5dc67ec43dc322dc4c6c4da7464d53e78c7f50284fa414d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341657928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b29667e376d3033990daed8f956ad8162f511ac82a5ecf9c3a2de844016646`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.version=20251005.0.430597
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 05 Oct 2025 00:07:46 GMT
LABEL org.opencontainers.image.created=2025-10-05T00:07:46+00:00
# Sun, 05 Oct 2025 00:07:46 GMT
COPY /rootfs/ / # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20251005.0.430597' /etc/os-release # buildkit
# Sun, 05 Oct 2025 00:07:46 GMT
ENV LANG=C.UTF-8
# Sun, 05 Oct 2025 00:07:46 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:57d32341d0b304edbdd20efcf9481afeb1fb71b457948c77d909ebc150363d3e`  
		Last Modified: Mon, 06 Oct 2025 19:51:26 GMT  
		Size: 341.6 MB (341647654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64da822fa5ec92466fb9b1d251f582d911d9c790c885007dab622a1d327b871`  
		Last Modified: Wed, 08 Oct 2025 22:18:19 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:1d3bd5c105654c180708d87ee1ddc01a2b20595c2309e80aefad7a4e7426bcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12400183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e817dec3eb673f3f94149ce924e8fa36ba53824d7d5c8278d5ef9baec098d5`

```dockerfile
```

-	Layers:
	-	`sha256:9ad82c0988e315385a06db740bb36b328c4e594c9e47be33aa65ddca196b3ec8`  
		Last Modified: Thu, 09 Oct 2025 01:48:31 GMT  
		Size: 12.4 MB (12388372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845fd47d51db66d960eeac4ce73f2e97b31281b40ebcb1f8cfc41f0532798327`  
		Last Modified: Thu, 09 Oct 2025 01:48:32 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20251012.0.434149`

**does not exist** (yet?)
