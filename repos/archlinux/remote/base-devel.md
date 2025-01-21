## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:8999d2508a630f124deb8b4f7a493d03241dd684960832b23fb07ae5176c5cea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:5f0f68c1af64d9a2c1f39e5b6cf0103f0faa0d74e6cf38ea76995e130ef87c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278486744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537671745d28d2908e964be52931c8329c51be6a939d745113d8e216e59722ec`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.version=20250119.0.299327
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 19 Jan 2025 00:08:08 GMT
LABEL org.opencontainers.image.created=2025-01-19T00:08:08+00:00
# Sun, 19 Jan 2025 00:08:08 GMT
COPY /rootfs/ / # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250119.0.299327' /etc/os-release # buildkit
# Sun, 19 Jan 2025 00:08:08 GMT
ENV LANG=C.UTF-8
# Sun, 19 Jan 2025 00:08:08 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:c92ba3935010a1e30876df8fa9636cdf7561433736d82ba5021cf01744194742`  
		Last Modified: Tue, 21 Jan 2025 18:28:12 GMT  
		Size: 278.5 MB (278477706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1664055cd5c8342841ed838597cc1cba4c1ebffc0ac35829d49369397115d9`  
		Last Modified: Tue, 21 Jan 2025 18:28:08 GMT  
		Size: 9.0 KB (9038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:c39d380c77720b207501086bf9f25f19acb5ce303a16373c642d7157790c2d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11906438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9aabf00209b7f9f3d3036eb329862a44c10a2c87cfb275da6d452413d88e84a`

```dockerfile
```

-	Layers:
	-	`sha256:cccc3e23a7c5e122d6b3b2df9c2185a610e9f2aebd54d2026623d1f9fe146b08`  
		Last Modified: Tue, 21 Jan 2025 18:28:09 GMT  
		Size: 11.9 MB (11894684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da9fde35c48ec031f36362f00d3c24a0d6d80bae83ae1ed5fb8eb7bf8bd15b9`  
		Last Modified: Tue, 21 Jan 2025 18:28:08 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
