## `archlinux:base`

```console
$ docker pull archlinux@sha256:c8501ab8b970205491501ba01d9bce9a04d70537fc15596360f1ce1011b08569
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:a45700aba9079ee52d41d080d1aed39066e0867aa9beebcc695cd111c21964e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151190914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94a7c8f8266f9cdbd578e1d5fb550dd9f2311b523b23c648418db6356490234`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.version=20240929.0.266368
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.created=2024-09-29T00:07:44+00:00
# Sun, 29 Sep 2024 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Sep 2024 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240929.0.266368' /etc/os-release # buildkit
# Sun, 29 Sep 2024 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 29 Sep 2024 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7ddbe2be8d389ca48dffe33e9c2cc9cc42a697902051e41777c3f38d5d133529`  
		Last Modified: Mon, 30 Sep 2024 23:11:22 GMT  
		Size: 151.2 MB (151182688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37561576c475eac7174073f448cc4d7cb50010a8824c054d93b01d3405485cc`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.2 KB (8226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:695ef93d80927410e8e69ecc29b51d94ef292b2ecb33bdc992a1e7ac8f8ec76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8114006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe361d1914f43ddd2e074e8ee3108ae79f040e50dff66ad09105afe9a122995`

```dockerfile
```

-	Layers:
	-	`sha256:fa44779a3be51b65fa3d5501ca4f91aa2096b037ec0f2f5893afdc1144496195`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 8.1 MB (8102285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40dd1c955fb739aa9dfb1b8ea50a71e4e1e088472d8543c9d9fea18a0ec26a1`  
		Last Modified: Mon, 30 Sep 2024 23:11:20 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json
