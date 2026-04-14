## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:3fc2ead62b076c22a52de9356a2fdae5267a6b367d9738fc1603bddaf33e3168
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:17244fb6581e539cc7582d0245ea93743efcad4c627ab78f0ed97f6f80427238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e999681263a5c23a0ea934cdf7a39ab4ddc6fd4693e2c53997a620b2e4e9a581`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.version=20260412.0.513370
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 13 Apr 2026 17:48:07 GMT
LABEL org.opencontainers.image.created=2026-04-12T00:06:50+00:00
# Mon, 13 Apr 2026 17:48:07 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 17:48:13 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260412.0.513370' /etc/os-release # buildkit
# Mon, 13 Apr 2026 17:48:13 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 17:48:13 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:58f17d36b1f875da33d63bcf8aca97555ff01fd66e8541aa5ba8046f40f02bde`  
		Last Modified: Mon, 13 Apr 2026 17:49:04 GMT  
		Size: 269.2 MB (269241935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b812d701975c8357fdd24cf8b88562d605ff90a39c598732dd8cf60faf2477aa`  
		Last Modified: Mon, 13 Apr 2026 17:48:58 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:e4dea3319f9fb499ee404b78bcdda52e5353bec086842311f24f130c8b66323f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12246414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4831d50e6b528c2eb42c5b602d70f3c272838e63e126237ba9db773aa1b9d052`

```dockerfile
```

-	Layers:
	-	`sha256:129b444e2b9c38ae6eae5ea7ae02a5626150812c5b5567277820b172bc6898f0`  
		Last Modified: Mon, 13 Apr 2026 17:48:58 GMT  
		Size: 12.2 MB (12234646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:466953aaadf55676730564b99e589d6133a87673fe345bfe02699e3e518b9854`  
		Last Modified: Mon, 13 Apr 2026 17:48:57 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
