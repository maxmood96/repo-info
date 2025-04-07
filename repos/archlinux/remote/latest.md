## `archlinux:latest`

```console
$ docker pull archlinux@sha256:95e914e8b16eb07c8660c4352c1530a52dcf829038f1f65233543fee28a78d6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:2bc4e27fb84da173ba06756de32def4daa6450d36817e2cb8f39ff498d42186c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.0 MB (160022478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f933370266099185a60baadf9d7af78d42b832d85988cc38ce640567795ada`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 06 Apr 2025 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:5d0dd26df6b775844a45d3d2b4ab2164f22c5a0888f1445e2c34f23e6135fad8`  
		Last Modified: Mon, 07 Apr 2025 18:03:41 GMT  
		Size: 160.0 MB (160014123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407b29e0f093892f642e2c89f45844893b21cf4c0154a5c693eac0fdb96aa969`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 8.4 KB (8355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:9017f22a54b74878f9b33d53d9cc571fe6bb5c9337f33939d4e7868ac805cbbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8174118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee256ca5e285ed7cf2e424a47011a1152f7068560949aae0c164042915750f8e`

```dockerfile
```

-	Layers:
	-	`sha256:2454f49832f802d70ca4a6ffba68d9c8606613d2260b7f57782720f7f9004a76`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 8.2 MB (8162146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d86d4aa84108478c1065e2746660d1f38fa76c5196875ee8591ce5d099ad5336`  
		Last Modified: Mon, 07 Apr 2025 18:03:37 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
