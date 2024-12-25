## `archlinux:base-devel-20241222.0.291122`

```console
$ docker pull archlinux@sha256:6112d42cc02db807bc8aeb512331d22be93f678ba68a4e4cafefa152da97c0ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241222.0.291122` - linux; amd64

```console
$ docker pull archlinux@sha256:8d61f3ed74f269272e70df5e40195fc5308b400b9ed9da88c03d0e380604c612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273856065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2f651a08c1f04fe4eb40a719e7200a8848e5f13311b11ac914622dd1e3cf56`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241222.0.291122
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Dec 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-12-22T00:07:56+00:00
# Sun, 22 Dec 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241222.0.291122' /etc/os-release # buildkit
# Sun, 22 Dec 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 22 Dec 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7f4b5c3559686ed19ef1a63b1048727d14f71087a8f2e482d930dee90ac25b19`  
		Last Modified: Tue, 24 Dec 2024 21:33:14 GMT  
		Size: 273.8 MB (273846983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ea974a1247e9562262166cec5caa8e8f0cd897256fdccb8cdfd3c8008c4bba`  
		Last Modified: Tue, 24 Dec 2024 21:33:11 GMT  
		Size: 9.1 KB (9082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241222.0.291122` - unknown; unknown

```console
$ docker pull archlinux@sha256:7f516d7f3691dd40b709869b6ad47eae2925ac07bf07155d79fe7eff496a5c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11895046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324e5c9e86c044d42b86b4c483fdb67ae04ffd772269813058f11b8ce24a9f74`

```dockerfile
```

-	Layers:
	-	`sha256:001f3f15c7341e61ca0de99604726afc118d6de52fb9ed456c8672cf4548dc51`  
		Last Modified: Tue, 24 Dec 2024 21:33:11 GMT  
		Size: 11.9 MB (11883292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e644f21426b048723151e4d607b46caca834906cd0c7573d20fad233937f5a`  
		Last Modified: Tue, 24 Dec 2024 21:33:11 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
