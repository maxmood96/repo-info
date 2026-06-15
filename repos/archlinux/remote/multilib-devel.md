## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9913645b0502208f2efdaa0c1bb34149fa59912b9f43556e6bf253e313bf227e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:72b64387a00eb1af2fde271b18ac92532ad8b810447fcde6c4858817b7b013dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325757133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1631f7fdcade9d29fa9ca86c566d7ad8ac97a548b86a57a25de9641b1cb826ef`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.version=20260614.0.544538
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 15 Jun 2026 18:38:48 GMT
LABEL org.opencontainers.image.created=2026-06-14T00:09:34+00:00
# Mon, 15 Jun 2026 18:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 15 Jun 2026 18:38:55 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260614.0.544538' /etc/os-release # buildkit
# Mon, 15 Jun 2026 18:38:55 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jun 2026 18:38:55 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5a7c0ae7636fdd5b0a3e918617dd5137091ba9d1fc005cea98693e7531a59bb2`  
		Last Modified: Mon, 15 Jun 2026 18:39:55 GMT  
		Size: 325.7 MB (325744576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf05f6fab31d37c6be2522ec8e5a555935626170962a5c71f2fcac0dea15bfdc`  
		Last Modified: Mon, 15 Jun 2026 18:39:46 GMT  
		Size: 12.6 KB (12557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0971ed3c722d880bdd3b9bd8a78c27d2fa8b55b91d2fe8eca349a9c02eb51ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14668911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7c7f10c7feb73ecb20f27b3794b8e7af8ccc30c142b6f41828afe92afbd18b`

```dockerfile
```

-	Layers:
	-	`sha256:ab338090c90a4a7e8f53f5c9487c81cb29d21b311ad6613026f049ca5c70f90f`  
		Last Modified: Mon, 15 Jun 2026 18:39:47 GMT  
		Size: 14.7 MB (14657143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b42d7364101d932e2da886bc700b8db70f2af6ddd4d3d0a664c14478ac1f75`  
		Last Modified: Mon, 15 Jun 2026 18:39:46 GMT  
		Size: 11.8 KB (11768 bytes)  
		MIME: application/vnd.in-toto+json
