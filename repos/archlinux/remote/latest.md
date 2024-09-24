## `archlinux:latest`

```console
$ docker pull archlinux@sha256:89c27a4ff1d7d36707f480e0a4592c36cf10f10f7a863a0edc25a66150b594ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:0f4020e179ffd4ffaeee875e0428db4725a70bad0b19d41a4a67c5ab9ad25a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151192144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37aeb8ca57b911c97101b8d388be4d9d01e2269eb2f8c378a16e27b7cd860cb`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240922.0.264758
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 22 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-22T00:07:28+00:00
# Sun, 22 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240922.0.264758' /etc/os-release # buildkit
# Sun, 22 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 22 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:417c3484ea7545ab975fe7bb5b75979245a2dfe8ac68e5440d7a91ed7fc96b91`  
		Last Modified: Tue, 24 Sep 2024 01:00:26 GMT  
		Size: 151.2 MB (151183919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266f74849237343d38f8d4e64d975434645d47398e77a13f83062ff0690f86c7`  
		Last Modified: Tue, 24 Sep 2024 01:00:25 GMT  
		Size: 8.2 KB (8225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:de41d4f09b4f9fc50d5f2d0a649262588cdfd6aff537216de99611aabe5f0b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 KB (11502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878e7d008da41e32c961fc3f5791e23658da41a32321a0bbdc1554277962662`

```dockerfile
```

-	Layers:
	-	`sha256:769812e6e0b1c94a3b53ad312b9b10ffa81a682d9687c57691904cc75d078164`  
		Last Modified: Tue, 24 Sep 2024 01:00:24 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.in-toto+json
