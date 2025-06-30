## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:2898517074c8894a121e3d31abd8b53e4d2db3860dc65b65090bb3676fa76d69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:143d404abb92f57ab35eba564f6e82f6985310aa6bebbb260c6d6ea3b47bcc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338952093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0086058769539afa8b0b5268270995457b03c08a6969e8e25fda269cd345225`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.version=20250629.0.373469
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 29 Jun 2025 00:07:42 GMT
LABEL org.opencontainers.image.created=2025-06-29T00:07:42+00:00
# Sun, 29 Jun 2025 00:07:42 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250629.0.373469' /etc/os-release # buildkit
# Sun, 29 Jun 2025 00:07:42 GMT
ENV LANG=C.UTF-8
# Sun, 29 Jun 2025 00:07:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b7495dd7e7362f16e7984d450d18e86d1828969cbf83c12c7bf463e6f9c65f41`  
		Last Modified: Mon, 30 Jun 2025 20:07:31 GMT  
		Size: 338.9 MB (338941824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b88b1aa8688a12df44810e87e48833d28c4d76fb5efcb289d4a1ba5e3f9b0f3`  
		Last Modified: Mon, 30 Jun 2025 17:17:53 GMT  
		Size: 10.3 KB (10269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:85f673e640516f266a6d75bee1930c9173890e41202bbf8a8c6d203925a9125d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12290950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60ec85a0384ddab020a1f56f5553bcd72a804db6426cb2d93480d18801a0300`

```dockerfile
```

-	Layers:
	-	`sha256:4c52e50b7e8a55a45b5a66f25005c1bc224c9723d8afa0b6db44cac3ac74f7ea`  
		Last Modified: Mon, 30 Jun 2025 19:48:27 GMT  
		Size: 12.3 MB (12279140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da321d6a9913d67f6a952b330e436a30aa2a459ecedaa3d681d733eec44905e`  
		Last Modified: Mon, 30 Jun 2025 19:48:28 GMT  
		Size: 11.8 KB (11810 bytes)  
		MIME: application/vnd.in-toto+json
