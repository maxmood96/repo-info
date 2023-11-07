## `archlinux:latest`

```console
$ docker pull archlinux@sha256:8e483c0185181a27f90d7c102a01078dd03b979904a0a74f31ad20e6134862bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:db8f0aa15c9bf71a6389f86f9b42e08f26411fe5dacf9bbf80491984dc33af74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147023418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18d28ca83aa4b06111699bff12359bb8f54bda1a5d754a77e3387c5cf937b39`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:22:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Nov 2023 23:20:34 GMT
LABEL org.opencontainers.image.version=20231105.0.189722
# Mon, 06 Nov 2023 23:20:34 GMT
LABEL org.opencontainers.image.revision=49b83e2f5501273bb46fde02768ab2064b88c8f0
# Mon, 06 Nov 2023 23:20:34 GMT
LABEL org.opencontainers.image.created=2023-11-05T00:07:59+00:00
# Mon, 06 Nov 2023 23:20:40 GMT
COPY dir:17c81daef01cefbff0304de2f541f3e15daacec5fb3fc441674c59e64f93cf69 in / 
# Mon, 06 Nov 2023 23:20:42 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231105.0.189722' /etc/os-release
# Mon, 06 Nov 2023 23:20:42 GMT
ENV LANG=C.UTF-8
# Mon, 06 Nov 2023 23:20:42 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6650e58cdd086241112cb6cc5a331ab100bb97cce9496966cb063e0adeb9965f`  
		Last Modified: Mon, 06 Nov 2023 23:22:22 GMT  
		Size: 147.0 MB (147015295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b341dfc42134f5496d8b0edd42fad5339f689411cf7cb26a3679ddbf7a4686`  
		Last Modified: Mon, 06 Nov 2023 23:22:02 GMT  
		Size: 8.1 KB (8123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
