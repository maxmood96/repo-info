## `archlinux:multilib-devel-20241006.0.268140`

```console
$ docker pull archlinux@sha256:7ffbac0e553cdbe7a05cd35a71843f564ac358bded672a70aa6a83393acfbf36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241006.0.268140` - linux; amd64

```console
$ docker pull archlinux@sha256:1b8c82f5f76c649bf1cb15f1d5ad719ac7e65bf82122a3257ba292ecf8b7bcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322032803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10cc2bb4a0eea00ab100c4267b0c5fa2ad168ed98a52f7958e3010892758187`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.version=20241006.0.268140
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 06 Oct 2024 00:07:56 GMT
LABEL org.opencontainers.image.created=2024-10-06T00:07:56+00:00
# Sun, 06 Oct 2024 00:07:56 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241006.0.268140' /etc/os-release # buildkit
# Sun, 06 Oct 2024 00:07:56 GMT
ENV LANG=C.UTF-8
# Sun, 06 Oct 2024 00:07:56 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ed7f81b56ae3922a2cb3615198765a6dda3043659a53fdf1d921877520b781fa`  
		Last Modified: Mon, 07 Oct 2024 19:59:39 GMT  
		Size: 322.0 MB (322022685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d2b8de4f4f15dd6257d07071aba84d668121d3b5ef4f8879b82e178dbcbf15`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 10.1 KB (10118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241006.0.268140` - unknown; unknown

```console
$ docker pull archlinux@sha256:4e3405e7758a1d979a5c5d04a1bbf358c39d63f9951355619a08fc0bf5c81261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2c19d5c6200c96c48b3f0e467ece42a49bf1d90a733824f79d22fef91e1d9f`

```dockerfile
```

-	Layers:
	-	`sha256:38f254e2895409bdc5f108c0803279c05d4cc0928dd3d44463fa4d0c47ebddfc`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 12.2 MB (12167879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7223f88a5db52a94dcebf542b4b52a8d3f41d7944db5ed61ef0dc3a9816bc40`  
		Last Modified: Mon, 07 Oct 2024 19:59:35 GMT  
		Size: 11.6 KB (11565 bytes)  
		MIME: application/vnd.in-toto+json
