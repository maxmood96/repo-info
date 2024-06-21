## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9af24109ecfd2ad28a671b60339ec5aa04175a8bc3b1ed62627f7f863a2d5447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f460c106c5d1615b6f1b8c14c3d0319b18dd392ea02bc07c1a428dd439c94f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316042490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78aa48b5f0c7aee075ed233131704097080f29e2f7848188f3d42a26c420b03f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.version=20240101.0.204074
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.revision=98cd79111dd530447f491d547d14f3c38e227e46
# Mon, 01 Jan 2024 19:08:40 GMT
LABEL org.opencontainers.image.created=2024-01-01T19:08:40+00:00
# Mon, 01 Jan 2024 19:08:40 GMT
COPY /rootfs/ / # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240101.0.204074' /etc/os-release # buildkit
# Mon, 01 Jan 2024 19:08:40 GMT
ENV LANG=C.UTF-8
# Mon, 01 Jan 2024 19:08:40 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:35515117493e52c38adb77412e5d70e1c716a60977e0d1bad3b1ed7e46700be3`  
		Last Modified: Wed, 29 May 2024 19:57:38 GMT  
		Size: 316.0 MB (316032410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb0b4faa739fd457842297c3fb0985f236ed38fc608e05d3005c0c580335c3`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 10.1 KB (10080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:db257f729b69366a7567c71548db340876c5758cd4bdb240cb0c2ad404fc877b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11887002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bb3b23fe40aa145c11e55cfce61382b3052408f1bf3a4e79eb8fe3ba5d11d9`

```dockerfile
```

-	Layers:
	-	`sha256:1d6130046940a135ea4800a943cb3a126ffae3c87470f1c98efce450541ec75a`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 11.9 MB (11875442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a64d29207bcc3b3262247db9bad2b94a39ec29f9f57114a773bc023299199aa`  
		Last Modified: Thu, 20 Jun 2024 20:55:33 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json
