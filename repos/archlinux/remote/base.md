## `archlinux:base`

```console
$ docker pull archlinux@sha256:ecb9460597467ddf638230a32bb67da0684a389612685e9a8fb23e7f7313b00a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:1e0c18173ffb7db8ce33172877859d2ca46c389eb360d60223149ff05541014d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151325564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1167d898dcca01fee7ad5f79869047ce289554d8cf928710a186e38ca3254d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:15fadeb05ca19b88f7dfdf81f8e4cefc7ab99c44cbc924c48b0bb47f1c7d38e8`  
		Last Modified: Mon, 18 Nov 2024 19:05:53 GMT  
		Size: 151.3 MB (151317267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f586b9bd7bce518d97d0723d1c4125ea1b141ee62172df90c48f5b7f3d6dd3d7`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 8.3 KB (8297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:dfdeb345f89d664ea88e32befeb610d42a99b8cf46a716a07586aaa9f67fa7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d102dae4023c30998fd61dc5e1eee55333295f72c134946fb51ca7d7618e8`

```dockerfile
```

-	Layers:
	-	`sha256:be42b2efa522d11a6e899421577e2b7276ba390869772faeba1d6c75dfeb84ae`  
		Last Modified: Mon, 18 Nov 2024 19:05:49 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fcdae8235ea3b296690ca48b1b2e82fd511804bb22aeb8637a1811dad99091`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
