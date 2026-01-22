## `archlinux:base-devel-20260118.0.482696`

```console
$ docker pull archlinux@sha256:d2bd09bd30dc1199ba6f35bc575292957a4a24377fb137d0f999817bc29adc17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260118.0.482696` - linux; amd64

```console
$ docker pull archlinux@sha256:54635d6ebf2fd2b0e61f53550764e4e23b9ec5cfb3461405e2ee91a3181c0a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293739464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f912e82db9a80c6e81598df987caccc156e03351f1a9a1455f6f3291700697`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:26:03 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:26:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:26:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:26:10 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:26:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1824341832c208f8b5ba9f73dd22bb8fa28ca60dfce33b1abdf6eafd18c27adb`  
		Last Modified: Tue, 20 Jan 2026 20:48:31 GMT  
		Size: 293.7 MB (293730101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da34fdd0475f9731bef22d34dce153980aedf456f92bc1a9d30819c789a732b0`  
		Last Modified: Tue, 20 Jan 2026 17:26:54 GMT  
		Size: 9.4 KB (9363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260118.0.482696` - unknown; unknown

```console
$ docker pull archlinux@sha256:705af7fe0b24fedc32e39bed3783793b010e14df70da5dfbb3fc56c1130c8ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12172833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b859631d3430bb2d1a4541e9fd7b3e1f9dba67547de638f226bdfcd3726b2c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1ec821b643c5be5385d65d19ebfc9d735fa7568b65d08b6d55466f7bfe29610a`  
		Last Modified: Tue, 20 Jan 2026 17:26:55 GMT  
		Size: 12.2 MB (12161122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3356d37d4f7a290ab5e1f719bf29e9ad20d76500f7adc8dc11574f0cf5779cb9`  
		Last Modified: Tue, 20 Jan 2026 17:26:54 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
