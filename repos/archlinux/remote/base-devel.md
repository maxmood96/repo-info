## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:3d31f40bcc1906a600cfd60ca402704f6c8255ff7ea6d7924e007c531fc0a967
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7e0a3a332be4c9cacfb32ab4048efd0f0886851862965aa034247be9ae456279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281546207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84fea2e6f3fb8948b31851ce4272f436d3b934f76a5616b680bcfcb3748870a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.version=20250406.0.331908
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.created=2025-04-06T00:07:28+00:00
# Sun, 06 Apr 2025 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250406.0.331908' /etc/os-release # buildkit
# Sun, 06 Apr 2025 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 06 Apr 2025 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:34b1058b6f6cc11aa7a452f023b91e3f5a3b87ece19c6f6ccfbf890893b3657f`  
		Last Modified: Mon, 07 Apr 2025 18:03:53 GMT  
		Size: 281.5 MB (281537033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0b2ffd56f55b5b4806373f362e9b24bb7ed6de316e33f9ddf0c6431d659bb9`  
		Last Modified: Mon, 07 Apr 2025 18:03:48 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3ed84327f4596f0a78d18256f930f21e60c395495c41e02549c519646ee9e5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11994332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27cb2805a16c90414b17683929835c9d0517523ca4c9cb230b16ecf008b2b2d`

```dockerfile
```

-	Layers:
	-	`sha256:3bda438186c9981ccd73624fcad54d60dff7b440fa512f9e645671b2c11b9d8e`  
		Last Modified: Mon, 07 Apr 2025 18:03:48 GMT  
		Size: 12.0 MB (11982578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7c1e887b4dbdac0a0583cf264d9da2b81341d4fb9de1338808e052477dfeca`  
		Last Modified: Mon, 07 Apr 2025 18:03:48 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
