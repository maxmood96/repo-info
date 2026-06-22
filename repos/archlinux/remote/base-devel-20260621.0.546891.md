## `archlinux:base-devel-20260621.0.546891`

```console
$ docker pull archlinux@sha256:cf028aee853281ba9b3cba41b49f7ad4836275256226938ab619e0f05b1e6105
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20260621.0.546891` - linux; amd64

```console
$ docker pull archlinux@sha256:9e9da3122b537ad94f22c8c6f89c1e3f253f3a1e22944364a061c75a041705da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303476484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a526da64be671b23ef83f536caa4cef2a32735775c66f2236da1faa549c44ed`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.version=20260621.0.546891
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.revision=34b87485162b028c8d957bdcd2674359d883cd21
# Mon, 22 Jun 2026 19:45:03 GMT
LABEL org.opencontainers.image.created=2026-06-21T00:09:09+00:00
# Mon, 22 Jun 2026 19:45:03 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 19:45:10 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20260621.0.546891' /etc/os-release # buildkit
# Mon, 22 Jun 2026 19:45:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:45:10 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:62643db854ce653b16203b398b46ee50dab761672d23297d03123adb232575e2`  
		Last Modified: Mon, 22 Jun 2026 19:46:02 GMT  
		Size: 303.5 MB (303465083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af39dfe94e24e71fad2521b922aff4ed726e224913d162d050cbcf17dbc532f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20260621.0.546891` - unknown; unknown

```console
$ docker pull archlinux@sha256:be48dd7af8c2581120437086d384ec198c4904e81dc99368d10d4b074495688a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14391790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182f008c3d3c04bd2a451a101f2d03e12bf162658c49f995254cb653be318010`

```dockerfile
```

-	Layers:
	-	`sha256:7657b4e8bce2843760e0550f8b92cd02f33275daa81be6edfde2a0b2e7ebe3ec`  
		Last Modified: Mon, 22 Jun 2026 19:45:56 GMT  
		Size: 14.4 MB (14380078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e360c05349f29d112ac8780a6d69629726f81182c0927a0e5dec9cc0835a0f`  
		Last Modified: Mon, 22 Jun 2026 19:45:55 GMT  
		Size: 11.7 KB (11712 bytes)  
		MIME: application/vnd.in-toto+json
