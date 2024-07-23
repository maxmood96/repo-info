## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a58fb33d8c7206869f7b718844ac8c849fa6a1ed811964153d33d41d096f600f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:50df1b242e2160d0d4cb7fa537e975bd2645fd7cd881a77f6e0210aea5f02587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151088755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15148a54b5fcc58f9d033bdc91d9d36a54bbb201fd202d2ff0ef79bb2f4e1f0e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d60d5665bb190f639c1d4f286977018d4342bc47593af30e0b92968fe432d0bc`  
		Last Modified: Mon, 22 Jul 2024 19:59:06 GMT  
		Size: 151.1 MB (151080489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad89e6a4db7258410d52ee2bf413c0ab30a2b3d955a29988cd17ec2da83a634a`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.3 KB (8266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:38afb58a07758e25bf1731f320aadbcdde0b32295909ecbeb9d2e0fe66cf5005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8110226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0a1b9732b6893ae31782a8d146307903a60a417b7d0713da3e062a8312bfef`

```dockerfile
```

-	Layers:
	-	`sha256:50be05d4c4748cce539e4ae26d202ada111e55183874695744f3e49ec8cdaa9f`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 8.1 MB (8098505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2d842272abbf169835e23a139787015b3f915dc85ca0b9c5466d38552014e9`  
		Last Modified: Mon, 22 Jul 2024 23:03:46 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
