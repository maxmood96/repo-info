## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:f15064b187aea96308a0252d1eacf514a2ee89aad6d44811f52b733fa9a5e42b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:3b828fb58696aab68e5c77350473a332a1746aa44f81a2bc8ad437dce0abb58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247372829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387ed57ebe179807b0f90dd1dafa11a3727c36be26c5355b2f6284fd4d027e18`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.version=20260419.0.517065
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 20 Apr 2026 21:47:34 GMT
LABEL org.opencontainers.image.created=2026-04-19T00:06:37+00:00
# Mon, 20 Apr 2026 21:47:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 20 Apr 2026 21:47:39 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260419.0.517065' /etc/os-release # buildkit
# Mon, 20 Apr 2026 21:47:39 GMT
ENV LANG=C.UTF-8
# Mon, 20 Apr 2026 21:47:39 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c3378b69ab420a6d8805fc88b36f1e41c1f0e83ddf2b2a9e2ff29467b9fa207a`  
		Last Modified: Mon, 20 Apr 2026 21:48:25 GMT  
		Size: 247.4 MB (247363642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad874ddd508cea21e6b14d5038ef0bd201a630e83994d91016b7e5eea408178`  
		Last Modified: Mon, 20 Apr 2026 21:48:17 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:af5cccb41808f62d766c1000aa926fc02a9c19234265172b65f84183a6241d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11993879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1b1b694fec3bee4fe2546cb2ec92355480b15894829b0d683ae6c5f0dd6b42`

```dockerfile
```

-	Layers:
	-	`sha256:af1ba5c2778e02d12f899d96accbb3382acf1d50a41c80162dcdc642db7680c8`  
		Last Modified: Mon, 20 Apr 2026 21:48:17 GMT  
		Size: 12.0 MB (11982168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5300d4d87819feb21d19f2504cbba80a9efc9bf0c8d5d8e5998de4c61c405e6c`  
		Last Modified: Mon, 20 Apr 2026 21:48:17 GMT  
		Size: 11.7 KB (11711 bytes)  
		MIME: application/vnd.in-toto+json
