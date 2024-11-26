## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:0803542df524cbf98632815130e842e442132fc2acdf6efd40333b9ae3ab8843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:6f6846e2335c587e9cc8f0fc7fc6894b8a7bbd9282b9efee67b7af74108e7562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272432368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538f4ef9da5e85838e12574192127c343054c4b0730ef0a4c35dff1e56498f16`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.version=20241124.0.282387
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.created=2024-11-24T00:07:35+00:00
# Sun, 24 Nov 2024 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241124.0.282387' /etc/os-release # buildkit
# Sun, 24 Nov 2024 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 24 Nov 2024 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:1b6f7e9affed36df2233412893aa6e4f821d730b29f3ace9ac9c3927c04cc2a6`  
		Last Modified: Mon, 25 Nov 2024 20:24:55 GMT  
		Size: 272.4 MB (272423296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd750ddf004134fa8657e503b627f7f9b20ecd15bf02e22eef11df93da10e3a`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:979cdf626a17bc7ada8b3f28f1a4e88842e85e72c61eece6111e154e4a35ebbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd83b9b97ecfbbb7f183eaaff607a43a5e55813637679875dc0e2a3b39a519f9`

```dockerfile
```

-	Layers:
	-	`sha256:2adc875c40f574d6f22094972fde3e047d24cfec5b0af49f5c44d83050dd98f5`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 11.9 MB (11895700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94408f0bd73fe2ed86b15821f95c9f1684d90deae8e17c1413fbd8aa5766af23`  
		Last Modified: Mon, 25 Nov 2024 20:24:52 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
