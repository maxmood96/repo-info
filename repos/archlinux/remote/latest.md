## `archlinux:latest`

```console
$ docker pull archlinux@sha256:94fa4d61453deb8841cccedd44320d294bcd9c1ebda0e3743b6cd9b330ca2280
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:98cbe6f236b494bac0fe22e68e50236c32781486fd00215eea0d4bc846c9bdbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151295122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f94599caa7b1c56b66c13f52be7cb482d5e8b42a7e152a879b13fd199df965e`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2facfc8e7394aecded27d459bdc7e393d42a5694c20c8355bb630acf3cfcc63d`  
		Last Modified: Mon, 11 Nov 2024 18:58:14 GMT  
		Size: 151.3 MB (151286801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d34984b69372bc8fa38097f4041aec4b71cce3e69d5c40026a50eab75361e2a`  
		Last Modified: Tue, 12 Nov 2024 02:02:02 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:69dd7b30e365a33c23338a9addb82377d94fa6ff5276ad132ab8749e4a8963ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80871409f20de5cfe87141ceaccecfbc123e988756dda3bf9bafcdc410fdc2c`

```dockerfile
```

-	Layers:
	-	`sha256:bb1364842a7793c836d3a6e9aa5a833212ff7df139f9d12b80045318b99cc397`  
		Last Modified: Tue, 12 Nov 2024 02:02:02 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a8cb0198f3136bb51afaac71eb4863bc8dbc9a8549d4671e874b311036be87b`  
		Last Modified: Tue, 12 Nov 2024 02:02:02 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json
