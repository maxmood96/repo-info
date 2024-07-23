## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:904a02d4c9629b3b793dfb50db6adfeec1c6f6bcf4bc3064492190378c1645a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:992c7760458aabf9e0318cfdf78f8213afbd4d4c1e65ac47b78447a93c614246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271452604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2682e2187c9d3e15f79346917a5c6fe08ae2251e8bedddd61cdf48b2ab7df4b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20240721.0.248532
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 21 Jul 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-07-21T00:07:43+00:00
# Sun, 21 Jul 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240721.0.248532' /etc/os-release # buildkit
# Sun, 21 Jul 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 21 Jul 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:68f76d89052db3b531b4590cccff8643757330318ed8f33f844421089f752f3e`  
		Last Modified: Mon, 22 Jul 2024 19:59:19 GMT  
		Size: 271.4 MB (271443577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fe652d6bc95c7768c93c69e6f102853e0cfe50b99b8cec7d467df6cd7c8acf`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:475bd249c3845413fc736cc474fe88b28c407aef6042defc5b3e3c2c3717f6dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11800120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ce15d15e18d0fb6e333fde5aa2071c1f2579d64576eab5327ebcfd6576beb8`

```dockerfile
```

-	Layers:
	-	`sha256:6d96c50ff5225eab7385c54e249a93045fbd5cb95cc354d58f506c06d289f708`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 11.8 MB (11788617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fefc2fee115f99e9851ca75e46ec703d0c2def6ebab097d680912c7eb4f285`  
		Last Modified: Mon, 22 Jul 2024 19:59:16 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json
