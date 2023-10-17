## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:7c4e1da516627362dfd40c9c13a073ebaffb5235b9850ebcd6deb508a9f25dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:b10ae4fc21300a3fa02a38a555fec7caf5e6fdba9eb6c0dc4d9c9eed215635a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264987172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700620546cefaa4299585f515370a74fe2703fdf7087a56ed5a0cddda2a1c0ac`
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
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.version=20231015.0.185077
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.revision=e688cede58b6771ce1117271551c1f0c57113614
# Tue, 17 Oct 2023 00:23:33 GMT
LABEL org.opencontainers.image.created=2023-10-15T00:07:15+00:00
# Tue, 17 Oct 2023 00:23:44 GMT
COPY dir:edc81e4213180b4af98cf7d3cdb95101b56d8b3847d7ed2f35c74dad3808c889 in / 
# Tue, 17 Oct 2023 00:23:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20231015.0.185077' /etc/os-release
# Tue, 17 Oct 2023 00:23:47 GMT
ENV LANG=C.UTF-8
# Tue, 17 Oct 2023 00:23:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:cba449e246f567dae7b0628945c680e924813660f6110cd2760cdd4cfb76a353`  
		Last Modified: Tue, 17 Oct 2023 00:25:14 GMT  
		Size: 265.0 MB (264978249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6159d2f97894c6a8e686f9e98c78575b91a09a9c314d152ed68df0a4db2717d7`  
		Last Modified: Tue, 17 Oct 2023 00:24:38 GMT  
		Size: 8.9 KB (8923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
