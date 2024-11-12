## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:7a39d39fcc4bfc0abeca6fdd1064509a612538ce22206768ca7ef3ef81fd7a51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:57f0118f8c73054be806187d37afebc17194b15e663f311e700c3f9cca94e4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272433328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f049d7f4555385959b8687d7898fc6a411b845c1dc024a92f77496de9fdd8ec7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
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
	-	`sha256:6f216b571f44a239d4f4c6d69a1dda566c45a9a44e799822dafdc9b32f5d6668`  
		Last Modified: Mon, 11 Nov 2024 18:58:44 GMT  
		Size: 272.4 MB (272424247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1051c98b6a187ac6033c013d3376afdc3935110349271e7c1c36c306f148cae0`  
		Last Modified: Tue, 12 Nov 2024 02:02:22 GMT  
		Size: 9.1 KB (9081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:f89a43946028fa555e133fd1942260cc8cbc275595b4837af000c98eb19ccc3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0d7b863a6d92d53cbc6cabd4b657ca8b0923c6af6bb5bffa70eb2a1dcfe6d8`

```dockerfile
```

-	Layers:
	-	`sha256:06ed292fa3bb88f128c9c4542e56ba497f3769192cc4a9927b41818d7bd24757`  
		Last Modified: Tue, 12 Nov 2024 02:02:23 GMT  
		Size: 11.9 MB (11895685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b9bf5afd42073eaedb1c4e90fb651823e0ed3184a678d85abc12de650cb8ac`  
		Last Modified: Tue, 12 Nov 2024 02:02:22 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
