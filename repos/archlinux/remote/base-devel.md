## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:cc49f48d188c483c30ea97ea9d72a60320268ba41dc390a84b49931ede212323
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:184dc07718fbfbd7e91b4451f319e15b3051a760de461a7f0cc2506d0f2355e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273856234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa56e074c40961284b699a46d0ca465f847bdebbe8e2a3a144d58b8482ed1c72`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.version=20241215.0.289170
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Dec 2024 00:07:31 GMT
LABEL org.opencontainers.image.created=2024-12-15T00:07:31+00:00
# Sun, 15 Dec 2024 00:07:31 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241215.0.289170' /etc/os-release # buildkit
# Sun, 15 Dec 2024 00:07:31 GMT
ENV LANG=C.UTF-8
# Sun, 15 Dec 2024 00:07:31 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9a629b563c7867e18ee942f491f3b1671d6bbbc3b986cf5208a6776d910507c5`  
		Last Modified: Mon, 16 Dec 2024 18:29:05 GMT  
		Size: 273.8 MB (273847126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d360bd31154f915de54aadd523646c3c3e6d270b8fbf97c74308104dace7fe`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 9.1 KB (9108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:0ddbc0c3c10c63175620fb884e53936b7fa47bcc83f479e6972b0d54079329b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11914779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe6da1cc9135248b585cc99893a06ff7263a3c21d04410f3559455a3dff4993`

```dockerfile
```

-	Layers:
	-	`sha256:7aedc5df46a740cb695f491deceb7c0fa0e88ae6a8a1b47f81237aa90163e2be`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 11.9 MB (11903025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07602835f1f406328928e1f9024ede80ce4dabf10fb3a57b193c6f6604afb392`  
		Last Modified: Mon, 16 Dec 2024 18:29:01 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json
