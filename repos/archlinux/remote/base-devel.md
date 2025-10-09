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
