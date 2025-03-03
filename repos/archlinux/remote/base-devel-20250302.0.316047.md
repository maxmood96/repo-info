## `archlinux:base-devel-20250302.0.316047`

```console
$ docker pull archlinux@sha256:61b9b05cf6a7a42aa1a32f0b00c92dcfc0b6acf3af2db1b86ab29f6605b21401
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20250302.0.316047` - linux; amd64

```console
$ docker pull archlinux@sha256:188ef5ce95b5a784984d9758c0cda67c284798500336ed4eed2bb15efe469389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280617641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad077ca48e15980d045d8adec7190650b679f318eaad53eec87704605c4a2b6`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.version=20250302.0.316047
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.revision=ae0527df18a9c5b94b28351b2265a20012d2fda0
# Sun, 02 Mar 2025 00:07:35 GMT
LABEL org.opencontainers.image.created=2025-03-02T00:07:35+00:00
# Sun, 02 Mar 2025 00:07:35 GMT
COPY /rootfs/ / # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250302.0.316047' /etc/os-release # buildkit
# Sun, 02 Mar 2025 00:07:35 GMT
ENV LANG=C.UTF-8
# Sun, 02 Mar 2025 00:07:35 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:21f5dcdde9037bc145a8f09b4dbc4c0ecf8cd531d80b207c214406f49fbd1be6`  
		Last Modified: Mon, 03 Mar 2025 19:13:19 GMT  
		Size: 280.6 MB (280608555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc006fc98655a856225002ded016e566c954840bbf607934b6f1947803dc1a15`  
		Last Modified: Mon, 03 Mar 2025 19:13:15 GMT  
		Size: 9.1 KB (9086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20250302.0.316047` - unknown; unknown

```console
$ docker pull archlinux@sha256:5d373902da7ba241e66d8ac6d3fc438584200531e842029ab3ee9808413a4ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.0 MB (11987649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e394d34ade0f93edb1efcb623348d73c688850a5cc6775ea96e0d4315a6874df`

```dockerfile
```

-	Layers:
	-	`sha256:54906d633b93a81f3961468d3d4be89ee28f899b3aca44c479c3a438176aaec5`  
		Last Modified: Mon, 03 Mar 2025 19:13:15 GMT  
		Size: 12.0 MB (11975895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8745b03003325ea5e1ea0e2aa309a67f25a7fadb09ee2f2623ef1187b89019b8`  
		Last Modified: Mon, 03 Mar 2025 19:13:15 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
