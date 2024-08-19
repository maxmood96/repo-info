## `archlinux:multilib-devel-20240818.0.255804`

```console
$ docker pull archlinux@sha256:8cc78a4be8187154c85b6b86b31e0d5f32f308c98a1ef5a5f017dcf804aa886c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20240818.0.255804` - linux; amd64

```console
$ docker pull archlinux@sha256:04abbe09ca0c911252f652215e2af0158e45e55a8d7121d55091ef9fd284d186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321631214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a66ed08b0753a74276dacabc149348c5df2c10b3e5892092d8223631a26f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.version=20240818.0.255804
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.created=2024-08-18T00:07:58+00:00
# Sun, 18 Aug 2024 00:07:58 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240818.0.255804' /etc/os-release # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 18 Aug 2024 00:07:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:461b8e0f36a974d10a4a68614097d8c97bc72bffc076091c4f99f4da2a7c4750`  
		Last Modified: Mon, 19 Aug 2024 17:58:20 GMT  
		Size: 321.6 MB (321621015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b414534c83a12bc64b75c8dc755917109916e743ad43b65dc765b3df2bd058c1`  
		Last Modified: Mon, 19 Aug 2024 17:58:15 GMT  
		Size: 10.2 KB (10199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20240818.0.255804` - unknown; unknown

```console
$ docker pull archlinux@sha256:d80aa1ce622836554dcf63dd99ee84fb31e5c7c731520a6ee81f8446f7a1f3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc830055c1405a0292b3aa0a099105a708148c26bfefa335337d005b5ddc5e9`

```dockerfile
```

-	Layers:
	-	`sha256:f3a38db00163f734fbb964073b4a4a7f3d159679230532cf4ade44afa14f18d9`  
		Last Modified: Mon, 19 Aug 2024 17:58:16 GMT  
		Size: 12.1 MB (12085462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeb1b6ff87f8417bc493bec00e926de21dcfc0ca887dfc560c8c325d06353d0`  
		Last Modified: Mon, 19 Aug 2024 17:58:15 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
