## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:5fb487a262dd7c25a26071b4d67daca47098433090727c23b71618a5cc3e5ecb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3f692909298cab4188877ac21a3bd294664b6653ddc2862785bd17980613fe6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304932717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56e15d495ca01bc634b5e96d4d7bfc6b2b3d25ed03c755f8dbc087196cabb91`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.version=20260628.0.549485
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 29 Jun 2026 19:09:30 GMT
LABEL org.opencontainers.image.created=2026-06-28T00:09:46+00:00
# Mon, 29 Jun 2026 19:09:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 29 Jun 2026 19:09:37 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260628.0.549485' /etc/os-release # buildkit
# Mon, 29 Jun 2026 19:09:37 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jun 2026 19:09:37 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:793b9865fc2e25877b456615434390b6feb8fbb2888e58f23a81e0d8f8586a22`  
		Last Modified: Mon, 29 Jun 2026 19:10:29 GMT  
		Size: 304.9 MB (304921264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07efb25f7f69f72f7093662826e83e1ee4e4fa7f632a6d95b6f5f7cd752a374f`  
		Last Modified: Mon, 29 Jun 2026 19:10:22 GMT  
		Size: 11.5 KB (11453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b7fa568e9a126719d275391d9bd65911ac25190316f3881459debb1eefae3b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14414573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001b19969c639bc8822d2713e27335069efb59fc7fdb9e93794ec31e4c10086b`

```dockerfile
```

-	Layers:
	-	`sha256:d18161be1e12b38f8bf95ec09582c689a582a1e737c478d17165feb387cf0825`  
		Last Modified: Mon, 29 Jun 2026 19:10:22 GMT  
		Size: 14.4 MB (14402861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610f818dcbb151019f45f8e705717767fb9c98449c83eba2e89c700bd24b0369`  
		Last Modified: Mon, 29 Jun 2026 19:10:22 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
