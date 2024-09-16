## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:a584d21535afcd833ded9bbd6e0fc0907b203fcfa8b11669f853866bde0c0ed9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:50021a00197cd7c4d8903987f79f92bc47170becdf7f33c3eb53751ad7802bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272145934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a332277d0673794c29e114d8cf46e21748e498cc3d3aad0c1c1199a99fd0b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240915.0.262934
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-15T00:07:28+00:00
# Sun, 15 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240915.0.262934' /etc/os-release # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 15 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d23292aad988212b9982631af27846dc7074de944c9c7b732bb709fb1a408bfb`  
		Last Modified: Mon, 16 Sep 2024 17:57:22 GMT  
		Size: 272.1 MB (272136925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f81783a1cbaf12250e3d4b9d6c37907f02e0302f2904a724d5e357c9ade1e9`  
		Last Modified: Mon, 16 Sep 2024 17:57:18 GMT  
		Size: 9.0 KB (9009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bef09cc5829cc45485c5455297f6599c56d7c3d4968f375dfd6a80cb1ddc1a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21d2bd38b0fd06aa514231fca6a73927c72a8e62c64261e834d0a536414b683`

```dockerfile
```

-	Layers:
	-	`sha256:a02d99b8cb3ebcc1af8d3eaabdfe85f71bb3448b5365c682fd24c0c72f92a593`  
		Last Modified: Mon, 16 Sep 2024 17:57:19 GMT  
		Size: 11.9 MB (11900570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50d59023a8f8fd372339b84d5569b2f9ddcea99293100dcd541d147ae0351c0d`  
		Last Modified: Mon, 16 Sep 2024 17:57:18 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
