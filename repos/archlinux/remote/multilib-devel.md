## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:74c759e625389806b3553d7c5a0d95d26618428883ebeab775a68b6f40ad35ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b47bcac2a43bf0857b4397fad9be6cc18be1a8f35f11a27b39506d9932decd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330623643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58e84aa3cf0a9087fff5fdd8656f92fd208b9de89c0c62334aa7f85c0b5f637`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250302.0.316047
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-03-02T00:07:35+00:00
# Sun, 02 Mar 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250302.0.316047' /etc/os-release # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 02 Mar 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:8523c5c460860703ca90183e37ae7db9d135d3191690aca4536d4a832ada5be1`  
		Last Modified: Mon, 03 Mar 2025 19:13:17 GMT  
		Size: 330.6 MB (330613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0241c1f953725c2e9dd779092b62b12f27247841a3dbe3d331f2c14126ebb331`  
		Last Modified: Mon, 03 Mar 2025 19:13:12 GMT  
		Size: 10.3 KB (10255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:4355bbb255fa34a842705eb9748b6739f11fbb74d2d0c949621b0106f9a92660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12256221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f444cdf961017b6bb633f1ec1a7653068999ec44f747258ec89233180d77b6ce`

```dockerfile
```

-	Layers:
	-	`sha256:f93007251547515c009447d22715c8552dd88c48bb53bbf23c95d974cabb744d`  
		Last Modified: Mon, 03 Mar 2025 19:13:12 GMT  
		Size: 12.2 MB (12244410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59e51e77aa926b1683d6d5746611689fef2415f1bb3d1cd8c3fe268a776e257`  
		Last Modified: Mon, 03 Mar 2025 19:13:12 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
