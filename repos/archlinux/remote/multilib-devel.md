## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:996271fe443a25059a31bae6863db63df6e090d8e81d4cdda7bb6a214c3d64ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:d33a25b63b044fe7db4b635f8b8e269f0f61d1b8012185ce8e2312b2a1d67bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322055353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c538f252b2b78620cb60b4de1f422977526c2b9f2b6686b47d8bdec4e3fc9c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.version=20241027.0.273886
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 27 Oct 2024 00:07:38 GMT
LABEL org.opencontainers.image.created=2024-10-27T00:07:38+00:00
# Sun, 27 Oct 2024 00:07:38 GMT
COPY /rootfs/ / # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241027.0.273886' /etc/os-release # buildkit
# Sun, 27 Oct 2024 00:07:38 GMT
ENV LANG=C.UTF-8
# Sun, 27 Oct 2024 00:07:38 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:826dcc06a75ff2538ee33ec9ad2888004cf6fbedaa6be4d815b2860824d9f2b4`  
		Last Modified: Mon, 28 Oct 2024 17:58:05 GMT  
		Size: 322.0 MB (322045198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8b3e30305e384e9de73f35d0185bcd40fbe39574152d686d8b39a00169e5c6`  
		Last Modified: Mon, 28 Oct 2024 17:57:59 GMT  
		Size: 10.2 KB (10155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:76d67f961cd5fe6d3ace9d34b7169bc44374801a7778595fdd5db6da21ea590e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12231028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21456cda2ce4b72ae58b39460c8becde13cd7c8dd421a8bd40ccf997847f95bf`

```dockerfile
```

-	Layers:
	-	`sha256:f233fe4a18354999f5a6e562c448bdc7a4e133c18a39830a0c89a042b77bd557`  
		Last Modified: Mon, 28 Oct 2024 17:58:00 GMT  
		Size: 12.2 MB (12219434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f334fa056038032813133136ccb698bcf7a0f27e0094116df1ae0c1470201b`  
		Last Modified: Mon, 28 Oct 2024 17:57:59 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json
