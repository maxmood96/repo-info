## `archlinux:multilib-devel-20250323.0.325468`

```console
$ docker pull archlinux@sha256:0d40c633ded387dc78a60e0531be2919d49a806f1598806ce3273c450828982c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20250323.0.325468` - linux; amd64

```console
$ docker pull archlinux@sha256:bb312cbc334d954dc2b8ecfb383b1535a9e7113a428aa22ad20cf8b081d0c761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330783652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174f6c8590415dc08e5f8cb2a419264bc5795d06a63d3442f0f72875a52955a8`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.version=20250323.0.325468
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 23 Mar 2025 00:07:47 GMT
LABEL org.opencontainers.image.created=2025-03-23T00:07:47+00:00
# Sun, 23 Mar 2025 00:07:47 GMT
COPY /rootfs/ / # buildkit
# Sun, 23 Mar 2025 00:07:47 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250323.0.325468' /etc/os-release # buildkit
# Sun, 23 Mar 2025 00:07:47 GMT
ENV LANG=C.UTF-8
# Sun, 23 Mar 2025 00:07:47 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:de449b0731eb708eeb75009dcbf892824b3b5cfda5b66dfb60c188546482aa32`  
		Last Modified: Mon, 24 Mar 2025 17:03:31 GMT  
		Size: 330.8 MB (330773385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d548c9ad1069a866f72c221621c6fdf8c32de58fc0871c39e7e458c72e94ceb`  
		Last Modified: Mon, 24 Mar 2025 17:03:25 GMT  
		Size: 10.3 KB (10267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20250323.0.325468` - unknown; unknown

```console
$ docker pull archlinux@sha256:404418faa55d6ff3644c0057b90ad45fb8274817b707a6f8f9b3ed62ea9424b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12260001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9909e6dc27e4849f713bfe7f472a32e7fed2b6a8799f4a0ae65469b35813165`

```dockerfile
```

-	Layers:
	-	`sha256:d923b7efdce58d4dbf0c055128bbc5e7b96c8c05e7cc35ed4b150ac00dc6b999`  
		Last Modified: Mon, 24 Mar 2025 17:03:26 GMT  
		Size: 12.2 MB (12248190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7a398e8fc6857df01b143f4dcdd75cd9d448bcb9c8fd63c666abfb12ad259c3`  
		Last Modified: Mon, 24 Mar 2025 17:03:25 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
