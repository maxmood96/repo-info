<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241117.0.280007`](#archlinuxbase-202411170280007)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241117.0.280007`](#archlinuxbase-devel-202411170280007)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241117.0.280007`](#archlinuxmultilib-devel-202411170280007)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:ecb9460597467ddf638230a32bb67da0684a389612685e9a8fb23e7f7313b00a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:1e0c18173ffb7db8ce33172877859d2ca46c389eb360d60223149ff05541014d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151325564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1167d898dcca01fee7ad5f79869047ce289554d8cf928710a186e38ca3254d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:15fadeb05ca19b88f7dfdf81f8e4cefc7ab99c44cbc924c48b0bb47f1c7d38e8`  
		Last Modified: Mon, 18 Nov 2024 19:05:53 GMT  
		Size: 151.3 MB (151317267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f586b9bd7bce518d97d0723d1c4125ea1b141ee62172df90c48f5b7f3d6dd3d7`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 8.3 KB (8297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:dfdeb345f89d664ea88e32befeb610d42a99b8cf46a716a07586aaa9f67fa7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d102dae4023c30998fd61dc5e1eee55333295f72c134946fb51ca7d7618e8`

```dockerfile
```

-	Layers:
	-	`sha256:be42b2efa522d11a6e899421577e2b7276ba390869772faeba1d6c75dfeb84ae`  
		Last Modified: Mon, 18 Nov 2024 19:05:49 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fcdae8235ea3b296690ca48b1b2e82fd511804bb22aeb8637a1811dad99091`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241117.0.280007`

```console
$ docker pull archlinux@sha256:ecb9460597467ddf638230a32bb67da0684a389612685e9a8fb23e7f7313b00a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241117.0.280007` - linux; amd64

```console
$ docker pull archlinux@sha256:1e0c18173ffb7db8ce33172877859d2ca46c389eb360d60223149ff05541014d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151325564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1167d898dcca01fee7ad5f79869047ce289554d8cf928710a186e38ca3254d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:15fadeb05ca19b88f7dfdf81f8e4cefc7ab99c44cbc924c48b0bb47f1c7d38e8`  
		Last Modified: Mon, 18 Nov 2024 19:05:53 GMT  
		Size: 151.3 MB (151317267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f586b9bd7bce518d97d0723d1c4125ea1b141ee62172df90c48f5b7f3d6dd3d7`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 8.3 KB (8297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241117.0.280007` - unknown; unknown

```console
$ docker pull archlinux@sha256:dfdeb345f89d664ea88e32befeb610d42a99b8cf46a716a07586aaa9f67fa7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d102dae4023c30998fd61dc5e1eee55333295f72c134946fb51ca7d7618e8`

```dockerfile
```

-	Layers:
	-	`sha256:be42b2efa522d11a6e899421577e2b7276ba390869772faeba1d6c75dfeb84ae`  
		Last Modified: Mon, 18 Nov 2024 19:05:49 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fcdae8235ea3b296690ca48b1b2e82fd511804bb22aeb8637a1811dad99091`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b8906906ba3fc092362810f44a46e2efdd9bea0b86a075cf6d464301fe766fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7c8c5ee4da753afd1a63da937eb1bbb38ce586ef8e76d7838bbf6a5a38a30d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272453880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c71c86b853cfd8c37635aa1c227fefb2bb241a18d7db66b53418aaf16124381`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5b83ed2a07fc5b4755ce19ed6a1ac373d387788e07c69b468c6073cb817f4993`  
		Last Modified: Mon, 18 Nov 2024 19:06:01 GMT  
		Size: 272.4 MB (272444827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed70366604336ab8983a33dc73fff4ad41780e7bcec86e107c0e53987f67808`  
		Last Modified: Mon, 18 Nov 2024 19:05:57 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:74594d43463779a0e9b5064adcb68cb4b481100c6d9d2020720e93928b530493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2a1c23d3a723c92b8a8eee9b0e0ae234701055a81cd3189f487a8945c92225`

```dockerfile
```

-	Layers:
	-	`sha256:20137dc0db65abb533a40bf51f6b78e06af95c80873c342c71f3735fa5f7bbd0`  
		Last Modified: Mon, 18 Nov 2024 19:05:58 GMT  
		Size: 11.9 MB (11895700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6839eff8f9915f011a4f8e08cf641e6dc6de80281d37235b50d7f9b1728446`  
		Last Modified: Mon, 18 Nov 2024 19:05:57 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241117.0.280007`

```console
$ docker pull archlinux@sha256:b8906906ba3fc092362810f44a46e2efdd9bea0b86a075cf6d464301fe766fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241117.0.280007` - linux; amd64

```console
$ docker pull archlinux@sha256:7c8c5ee4da753afd1a63da937eb1bbb38ce586ef8e76d7838bbf6a5a38a30d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272453880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c71c86b853cfd8c37635aa1c227fefb2bb241a18d7db66b53418aaf16124381`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:5b83ed2a07fc5b4755ce19ed6a1ac373d387788e07c69b468c6073cb817f4993`  
		Last Modified: Mon, 18 Nov 2024 19:06:01 GMT  
		Size: 272.4 MB (272444827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed70366604336ab8983a33dc73fff4ad41780e7bcec86e107c0e53987f67808`  
		Last Modified: Mon, 18 Nov 2024 19:05:57 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241117.0.280007` - unknown; unknown

```console
$ docker pull archlinux@sha256:74594d43463779a0e9b5064adcb68cb4b481100c6d9d2020720e93928b530493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2a1c23d3a723c92b8a8eee9b0e0ae234701055a81cd3189f487a8945c92225`

```dockerfile
```

-	Layers:
	-	`sha256:20137dc0db65abb533a40bf51f6b78e06af95c80873c342c71f3735fa5f7bbd0`  
		Last Modified: Mon, 18 Nov 2024 19:05:58 GMT  
		Size: 11.9 MB (11895700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6839eff8f9915f011a4f8e08cf641e6dc6de80281d37235b50d7f9b1728446`  
		Last Modified: Mon, 18 Nov 2024 19:05:57 GMT  
		Size: 11.8 KB (11753 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:ecb9460597467ddf638230a32bb67da0684a389612685e9a8fb23e7f7313b00a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:1e0c18173ffb7db8ce33172877859d2ca46c389eb360d60223149ff05541014d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151325564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1167d898dcca01fee7ad5f79869047ce289554d8cf928710a186e38ca3254d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:15fadeb05ca19b88f7dfdf81f8e4cefc7ab99c44cbc924c48b0bb47f1c7d38e8`  
		Last Modified: Mon, 18 Nov 2024 19:05:53 GMT  
		Size: 151.3 MB (151317267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f586b9bd7bce518d97d0723d1c4125ea1b141ee62172df90c48f5b7f3d6dd3d7`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 8.3 KB (8297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:dfdeb345f89d664ea88e32befeb610d42a99b8cf46a716a07586aaa9f67fa7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8094062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d102dae4023c30998fd61dc5e1eee55333295f72c134946fb51ca7d7618e8`

```dockerfile
```

-	Layers:
	-	`sha256:be42b2efa522d11a6e899421577e2b7276ba390869772faeba1d6c75dfeb84ae`  
		Last Modified: Mon, 18 Nov 2024 19:05:49 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fcdae8235ea3b296690ca48b1b2e82fd511804bb22aeb8637a1811dad99091`  
		Last Modified: Mon, 18 Nov 2024 19:05:48 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:71c9b81ecb343d10bb75aab8daf7deec25372f5f65488adc8481a6543e35432c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:ed22ca153e83fa62a2d20da071e35a466d57712c531a333efffe9066f54833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322304184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238fe4342e6ad0b556c499c57efdce516d709ff060f57f8c76065473cad192b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:bc3a3f8d212d78a51736400db0f99c87929fecb779492a3ab85f465087fee5b1`  
		Last Modified: Mon, 18 Nov 2024 19:06:43 GMT  
		Size: 322.3 MB (322293956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b58bd3f7846a9afc0bb13ac63948cee775ace6dc94031e913c57f13b79eecaa`  
		Last Modified: Mon, 18 Nov 2024 19:06:35 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:3082c9babb0fa9c04d667f7f881babe90fce18e3fada33182b57b54871237c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35db4ac340f9b4d1a12c6c579cecbd8b8a8ed1c0e31920fb267ad05e3bd5a71d`

```dockerfile
```

-	Layers:
	-	`sha256:33d959197b31181beaace8d3e8d66fbc84b8ac82d440cdf01c8a521437739846`  
		Last Modified: Mon, 18 Nov 2024 19:06:36 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff1c36045df7445ea2b09130c539b2cfd0412ed4e49bf7358ab0bbab0c9e86c`  
		Last Modified: Mon, 18 Nov 2024 19:06:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241117.0.280007`

```console
$ docker pull archlinux@sha256:71c9b81ecb343d10bb75aab8daf7deec25372f5f65488adc8481a6543e35432c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241117.0.280007` - linux; amd64

```console
$ docker pull archlinux@sha256:ed22ca153e83fa62a2d20da071e35a466d57712c531a333efffe9066f54833e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322304184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0238fe4342e6ad0b556c499c57efdce516d709ff060f57f8c76065473cad192b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.version=20241117.0.280007
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 17 Nov 2024 00:08:06 GMT
LABEL org.opencontainers.image.created=2024-11-17T00:08:06+00:00
# Sun, 17 Nov 2024 00:08:06 GMT
COPY /rootfs/ / # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241117.0.280007' /etc/os-release # buildkit
# Sun, 17 Nov 2024 00:08:06 GMT
ENV LANG=C.UTF-8
# Sun, 17 Nov 2024 00:08:06 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:bc3a3f8d212d78a51736400db0f99c87929fecb779492a3ab85f465087fee5b1`  
		Last Modified: Mon, 18 Nov 2024 19:06:43 GMT  
		Size: 322.3 MB (322293956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b58bd3f7846a9afc0bb13ac63948cee775ace6dc94031e913c57f13b79eecaa`  
		Last Modified: Mon, 18 Nov 2024 19:06:35 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241117.0.280007` - unknown; unknown

```console
$ docker pull archlinux@sha256:3082c9babb0fa9c04d667f7f881babe90fce18e3fada33182b57b54871237c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35db4ac340f9b4d1a12c6c579cecbd8b8a8ed1c0e31920fb267ad05e3bd5a71d`

```dockerfile
```

-	Layers:
	-	`sha256:33d959197b31181beaace8d3e8d66fbc84b8ac82d440cdf01c8a521437739846`  
		Last Modified: Mon, 18 Nov 2024 19:06:36 GMT  
		Size: 12.2 MB (12164496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff1c36045df7445ea2b09130c539b2cfd0412ed4e49bf7358ab0bbab0c9e86c`  
		Last Modified: Mon, 18 Nov 2024 19:06:35 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json
