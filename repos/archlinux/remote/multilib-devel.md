## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9323d3b3c7820c46482b0bb6e923de50c6c57559c6b24da2fba20080e38ec756
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:86480447275383bee14322c6cd282de8077c14ba012d9cebc3a036f380c4835f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (345049834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ddc12e4505f7caae20b2c36fe036f533d21a79bb0a56dabcb3cd3795003cdf`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.version=20260111.0.480139
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.revision=0d7c4c0017584f9bcb495105cc412d6575f04564
# Mon, 12 Jan 2026 19:43:13 GMT
LABEL org.opencontainers.image.created=2026-01-11T00:07:19+00:00
# Mon, 12 Jan 2026 19:43:13 GMT
COPY /rootfs/ / # buildkit
# Mon, 12 Jan 2026 19:43:20 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260111.0.480139' /etc/os-release # buildkit
# Mon, 12 Jan 2026 19:43:20 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jan 2026 19:43:20 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:493685d34efc1b3b976004964157c27a3d5de3f6b952a5fd469441213132444e`  
		Last Modified: Mon, 12 Jan 2026 19:45:46 GMT  
		Size: 345.0 MB (345039388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bec5dba24b86b8db48c9e22afb803190afd87c8c62598a7d8666417400dfaa5`  
		Last Modified: Mon, 12 Jan 2026 19:44:22 GMT  
		Size: 10.4 KB (10446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0231aba07e41078e2bf076ffae7128bd2e0fe6c743cb106f51ae54dcc84c7a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12441705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7ca0862b02cf40fb5dace81e3b0b79702f7d0dcef76168c30ee13929f4a71d`

```dockerfile
```

-	Layers:
	-	`sha256:dd9b612d05efa0c7fc376d50fc4d9cdd1eb36d9581c83b433f619bd38068b400`  
		Last Modified: Mon, 12 Jan 2026 20:48:31 GMT  
		Size: 12.4 MB (12429937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32410d291a859c1a18167d95dc899ab3e1f80aa649da27a260b3e839db719f39`  
		Last Modified: Mon, 12 Jan 2026 20:48:32 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
