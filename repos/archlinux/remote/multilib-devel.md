## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:071b4cb1f6db1871a75b5fa13e367fa0675d3a7b89837dec8b7086a70f8829ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:70645f647cd08d3f382fed4b38571c2aad78aeb575dd62a3c85abcf89e78d656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322031945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a43d2c52fc6c00026b3be459daf52b663135439774983ce94ea5d03fe127cfd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.version=20240929.0.266368
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 29 Sep 2024 00:07:44 GMT
LABEL org.opencontainers.image.created=2024-09-29T00:07:44+00:00
# Sun, 29 Sep 2024 00:07:44 GMT
COPY /rootfs/ / # buildkit
# Sun, 29 Sep 2024 00:07:44 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240929.0.266368' /etc/os-release # buildkit
# Sun, 29 Sep 2024 00:07:44 GMT
ENV LANG=C.UTF-8
# Sun, 29 Sep 2024 00:07:44 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d7b7f73b0b674cd33738487d735a88a1d8e00ae4f0a094aa513f8841d187c55d`  
		Last Modified: Mon, 30 Sep 2024 23:12:17 GMT  
		Size: 322.0 MB (322021855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0436639ec6db38a92616a17c93af27037cfc1b1e5439f061ed2bf66161797f`  
		Last Modified: Mon, 30 Sep 2024 23:12:09 GMT  
		Size: 10.1 KB (10090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:2d6fc250a4dc13839a029d53734a2b6fd2041b17a52cf948aed6378e7fef8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481d3ea760c1c4039e2b13c9ef290dfee13a7c3537b417aa850cbabbd8550a24`

```dockerfile
```

-	Layers:
	-	`sha256:757b9f215d8266fb6faa6938ae99995cfbcf36cf10eb9eb0b1f6cfc213b16fed`  
		Last Modified: Mon, 30 Sep 2024 23:12:10 GMT  
		Size: 12.2 MB (12167888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada334a1431c7dfb2e1c1fbb2e3e604d39d70cf1e7e458021b3f43d9dfc4ec49`  
		Last Modified: Mon, 30 Sep 2024 23:12:09 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
