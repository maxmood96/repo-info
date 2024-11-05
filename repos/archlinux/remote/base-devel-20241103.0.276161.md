## `archlinux:base-devel-20241103.0.276161`

```console
$ docker pull archlinux@sha256:2e394a68150cdde8d1c4f7f9d9a6a9d8e21fd56c041d8607003c53ffabf0aaa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241103.0.276161` - linux; amd64

```console
$ docker pull archlinux@sha256:afb417afa1aa9433e5cbb534602c84724d936b54187eef1049dde903e762ceff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272414900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dceeedcc610103f29bcba2d6623c514263cb1f7d7af4ef7b9a76691321147e4c`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.version=20241103.0.276161
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 03 Nov 2024 00:07:41 GMT
LABEL org.opencontainers.image.created=2024-11-03T00:07:41+00:00
# Sun, 03 Nov 2024 00:07:41 GMT
COPY /rootfs/ / # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241103.0.276161' /etc/os-release # buildkit
# Sun, 03 Nov 2024 00:07:41 GMT
ENV LANG=C.UTF-8
# Sun, 03 Nov 2024 00:07:41 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:4198ddba3601b79804e83b86e3bd89492c3560e4d2b70023f815a6c1da87d4fa`  
		Last Modified: Mon, 04 Nov 2024 22:04:48 GMT  
		Size: 272.4 MB (272405834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d808f95be0a6a37bbfec58f9ba340d523244d539ed88dd902c5cfe843051b37a`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 9.1 KB (9066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241103.0.276161` - unknown; unknown

```console
$ docker pull archlinux@sha256:446a216eb8179bf22bd785e0e686c195dd071cd65957d97f2e5b359efa4671f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11969317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89434f94497f1ab173de723829496cb5b07a7f6811dda65f623c47f6acb8e4b2`

```dockerfile
```

-	Layers:
	-	`sha256:0da84a7317d277c17044fed3a2482b9ddd1acc30edbfbd8dc22fe81649074351`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 12.0 MB (11957780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68367567a5c40510009c8cc0193620d653143687b4ec518a3d71a5be5eca62e`  
		Last Modified: Mon, 04 Nov 2024 22:04:44 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json
