## `archlinux:base`

```console
$ docker pull archlinux@sha256:876f1f601e5fe6ceda682ac9b0a8df06be695fe9e2c85d04f48a877f17e46b45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:89639d3a2d102158ab5a6668dc340a6e5cf1acf12f78b55b508b8c38da461869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151290858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad78b172bfc727fc18ce09cce74fd6d4a8ad10c59b9b9413cf5c3edb778dbb7c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:7304439b608ad119a822a6f2749be0e4b54b6c5c50120b1a68128aec0fe54ffc`  
		Last Modified: Mon, 04 Nov 2024 22:04:33 GMT  
		Size: 151.3 MB (151282558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcbeaf6513208b6048f8bbeeb0de6d113a1929a56d42de734c75663a9c8bdd1`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 8.3 KB (8300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d9b5f14825ea774e8ef2679fb1e019a853037a93fb14677b2648d4f8b3921014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8155940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8970fad62e2319137e450f4343c170ab08155549250df72f2b338afa082f100`

```dockerfile
```

-	Layers:
	-	`sha256:1e57a5d6f7993e35f506921a12b9c8fedf8f523b519d8e9f726877b604f5f68b`  
		Last Modified: Mon, 04 Nov 2024 22:04:30 GMT  
		Size: 8.1 MB (8144185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76660bc2012d08e0e3a04b9a9b6c5e3b933dcbfa01252b0451f4c0e933e59afd`  
		Last Modified: Mon, 04 Nov 2024 22:04:29 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json
