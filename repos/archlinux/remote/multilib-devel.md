## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:19dcebdda856065d0384ab74ffa96eccb3d28cd789bc447c8226d19a4733d77c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:cc333cb344d8cb4915cb167b31480a0879303a790b555a64051dd40335669222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345062239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07513cb60684845d860b4812ff47411ab2131ed890f511fc33b3ae4f7aa765f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.version=20260118.0.482696
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Tue, 20 Jan 2026 17:26:09 GMT
LABEL org.opencontainers.image.created=2026-01-18T00:07:00+00:00
# Tue, 20 Jan 2026 17:26:09 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Jan 2026 17:26:17 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260118.0.482696' /etc/os-release # buildkit
# Tue, 20 Jan 2026 17:26:17 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jan 2026 17:26:17 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c9126e44ff2b632f68545a4b591fcdbfe6b0a5eb414c823621ffaa0e64e15b4b`  
		Last Modified: Tue, 20 Jan 2026 17:28:35 GMT  
		Size: 345.1 MB (345051773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4aba7bbe4bf25681eae44175c0000ca519f34e75e60d9021846669d1f7d734a`  
		Last Modified: Tue, 20 Jan 2026 17:27:37 GMT  
		Size: 10.5 KB (10466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bd4a94bc0c5d6e2c236d55727237144ca65376741502d2745451292d0f0e125f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12441683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46a63af9c62ba5b321040095a7cd86ea17a15a0526d50074365189f79ae731a`

```dockerfile
```

-	Layers:
	-	`sha256:60d19c113113aff0c089def5af1cdcdc8def6211c154e4d64cbf4efeb20b9e8b`  
		Last Modified: Tue, 20 Jan 2026 20:48:31 GMT  
		Size: 12.4 MB (12429915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f1b5635cfb41faeb7e5a11c7a7bc99cab8b3e5406afd89e2216bd002752b74`  
		Last Modified: Tue, 20 Jan 2026 20:48:39 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
