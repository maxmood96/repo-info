## `archlinux:base-devel-20231105.0.189722`

```console
$ docker pull archlinux@sha256:86dff0159c92057b1f3760faa04896482040eec0530df89b0c8bfb478bf77761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel-20231105.0.189722` - linux; amd64

```console
$ docker pull archlinux@sha256:d26fbd1b7efac6a9eb0857ed1e6210d108014a5849f26cac84745fe4cb79e5a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265206628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaad85b58b18b64210f19f90491ca16500921b814f19854d946b528d8261027`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Tue, 17 Oct 2023 00:23:32 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 06 Nov 2023 23:21:32 GMT
LABEL org.opencontainers.image.version=20231105.0.189722
# Mon, 06 Nov 2023 23:21:32 GMT
LABEL org.opencontainers.image.revision=49b83e2f5501273bb46fde02768ab2064b88c8f0
# Mon, 06 Nov 2023 23:21:32 GMT
LABEL org.opencontainers.image.created=2023-11-05T00:08:02+00:00
# Mon, 06 Nov 2023 23:21:43 GMT
COPY dir:3550f6b9193a286f703115e97e1d82d1e61fba67f8bb35b3952c182575027ce8 in / 
# Mon, 06 Nov 2023 23:21:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231105.0.189722' /etc/os-release
# Mon, 06 Nov 2023 23:21:47 GMT
ENV LANG=C.UTF-8
# Mon, 06 Nov 2023 23:21:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:ba0909463babfa15827029a5c52246e81df7c3815ff4b87c7e1ef16a6effa2b5`  
		Last Modified: Mon, 06 Nov 2023 23:23:10 GMT  
		Size: 265.2 MB (265197694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee403973285d673f668bc27322379203a529cc1c62a42e3c7974de7ea7d2075`  
		Last Modified: Mon, 06 Nov 2023 23:22:33 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
