## `archlinux:base`

```console
$ docker pull archlinux@sha256:5906892165fc79b4e282e36f24802528bcee2bd2896982ad771045341e15db5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:0ad2f00a305657ced5001f8d41d3dfd6429a8069e4bb3eab890dc232537719ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.3 MB (152291760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8964901e692515f9bdd5bb6d16e6cb3af6739a6fc6afb3ef299f42411b15a85b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.version=20241208.0.286830
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 08 Dec 2024 00:07:49 GMT
LABEL org.opencontainers.image.created=2024-12-08T00:07:49+00:00
# Sun, 08 Dec 2024 00:07:49 GMT
COPY /rootfs/ / # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241208.0.286830' /etc/os-release # buildkit
# Sun, 08 Dec 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Sun, 08 Dec 2024 00:07:49 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:a657cefe89310565e146e5ba7877550e1460875ce9c57e91c29918efa9e922a0`  
		Last Modified: Mon, 09 Dec 2024 19:28:35 GMT  
		Size: 152.3 MB (152283443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf988a8d22c1d5021726e9d622a45c020c406f160ae3a8eb4096a6772f75f7d`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 8.3 KB (8317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:4ea970ea8d720070e3faa9bbd7c8bbbca96a82cd3a114d697cfa97ac56c90257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8095271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab491e7d7847963c80975ff0fc5de6c820de1df7806af8e2963d9625b14b736`

```dockerfile
```

-	Layers:
	-	`sha256:e28dc204826342bda6e9648087fc071d774364d5a3db020d143b779bc4327a68`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 8.1 MB (8083299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ac5064e13be4ec53093c68dba80349dc7347e674a4cfd7b6d9dd948355ceaa6`  
		Last Modified: Mon, 09 Dec 2024 19:28:33 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
