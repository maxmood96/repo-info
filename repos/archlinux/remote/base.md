## `archlinux:base`

```console
$ docker pull archlinux@sha256:fc897ab3c923fa324b1c9abf5ee08ac4f376092da2d9fec331294e8d54fedd10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:565f16a79515bef3b66439cc8ff03b754f41e76f0d431d0e3b4f3a5825cdeff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151308382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b92a769a168819a59a9d421b1a8c97fdaa87568298716446d17802605b0f44`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 24 Nov 2024 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
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
	-	`sha256:f524c82a4279ec25a2fddc9b69620d6dc38b8f1e7c8a6a4596478dbce8e96100`  
		Last Modified: Mon, 25 Nov 2024 20:24:17 GMT  
		Size: 151.3 MB (151300062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f061d5e0ca6d1f0bf9cd9b5efc6756a6cbfd81dd87011f27fd1bb5f0b9d8f075`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.3 KB (8320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:ceaeb0a9110116e81f1ba710eecc1284603f69e7c7af6fa657b326a6a7185c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0127b9a8c6982033cd69680b63f429fc8236f49e6f96d862ebee2eca2b8e477d`

```dockerfile
```

-	Layers:
	-	`sha256:1559809d9d4ffa0b705f8c637df23d12b8757acd5630123a17aa815b71498dfd`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a1505f67255a492bf8f693797a2ec5ef348ca48ea9d0499b8a97a2b4535290`  
		Last Modified: Mon, 25 Nov 2024 20:24:14 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json
