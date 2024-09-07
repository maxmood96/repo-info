## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:10912b44e838dd335ff9bcb38995c4807bbe8aa293623190afb3afd2716760de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:eff11b75a9bc18500f7d71b4cce218dde3483a05a02139eb4b3efb31da889fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321627596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ae1e385fa3ca79af934bfcfd4bdd1273b8ec5152ea3953424dcd302074d874`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20240825.0.257728
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 25 Aug 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-08-25T00:07:35+00:00
# Sun, 25 Aug 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240825.0.257728' /etc/os-release # buildkit
# Sun, 25 Aug 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 25 Aug 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:b39c3f3d5831908f56eae8d8bceedb49c7424402515d9cf9b1feb3ba6c022781`  
		Last Modified: Mon, 26 Aug 2024 21:59:50 GMT  
		Size: 321.6 MB (321617407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0ba7ee9a3b8b9b42fdce4d1f2c978a00e0c0a19a83a4e96752beb6e8a39cc7`  
		Last Modified: Fri, 06 Sep 2024 23:16:19 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0b811b6d24805858211a5c565f2d8f752a1fc3ece91eb130c201f60f3061855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49213f8b851b3c29d88b3e8b302b4a1f776557358da20274d1242f17425e7fae`

```dockerfile
```

-	Layers:
	-	`sha256:4b24a7253625f628d2c7b94757fde4664420b577841f858c78d1a010852537ad`  
		Last Modified: Fri, 06 Sep 2024 23:16:19 GMT  
		Size: 12.1 MB (12085490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e51c63051759cef7e90e1c7694d3db27d97a990e39666f462e16456ab891d13`  
		Last Modified: Fri, 06 Sep 2024 23:16:19 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
