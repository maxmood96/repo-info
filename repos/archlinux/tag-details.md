<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20241110.0.278197`](#archlinuxbase-202411100278197)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20241110.0.278197`](#archlinuxbase-devel-202411100278197)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20241110.0.278197`](#archlinuxmultilib-devel-202411100278197)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:3c9c1b4058255ab69853cec0f04e12505fb6a25ffa5a2d3baf91032cb93b1525
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:098a55eaa21d67f4fac315702eea994316b7425c7da7947bfdc4a7d46d9edde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151295122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6161c1a4982fa9c04c584160b298e1f0578f25f2d229ac1e5d1d240201487b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2facfc8e7394aecded27d459bdc7e393d42a5694c20c8355bb630acf3cfcc63d`  
		Last Modified: Mon, 11 Nov 2024 18:58:14 GMT  
		Size: 151.3 MB (151286801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ba553329ad01d47c421f02a99b69b6a61b1e4f5db14017b3b538c2f15732aa`  
		Last Modified: Mon, 11 Nov 2024 18:58:12 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:2f82d894985e9b6e0ecc9d1b5849738006d81515aea89373f3bfaef06d80ce19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8093845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ceda43db7c7c10503ce58f5adb0b2aff5a939be342d2ae7491f275f8b9bdf4`

```dockerfile
```

-	Layers:
	-	`sha256:845d02b3a0664ac7fad2313c074fec2da6f09b9f6cdec20f7c35e3beb73eb652`  
		Last Modified: Mon, 11 Nov 2024 18:58:13 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a899e579497bb51652521013ff3c829a4607c0aa2f8b4fdbf89ae02a5969386`  
		Last Modified: Mon, 11 Nov 2024 18:58:12 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20241110.0.278197`

```console
$ docker pull archlinux@sha256:3c9c1b4058255ab69853cec0f04e12505fb6a25ffa5a2d3baf91032cb93b1525
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-20241110.0.278197` - linux; amd64

```console
$ docker pull archlinux@sha256:098a55eaa21d67f4fac315702eea994316b7425c7da7947bfdc4a7d46d9edde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151295122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6161c1a4982fa9c04c584160b298e1f0578f25f2d229ac1e5d1d240201487b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2facfc8e7394aecded27d459bdc7e393d42a5694c20c8355bb630acf3cfcc63d`  
		Last Modified: Mon, 11 Nov 2024 18:58:14 GMT  
		Size: 151.3 MB (151286801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ba553329ad01d47c421f02a99b69b6a61b1e4f5db14017b3b538c2f15732aa`  
		Last Modified: Mon, 11 Nov 2024 18:58:12 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-20241110.0.278197` - unknown; unknown

```console
$ docker pull archlinux@sha256:2f82d894985e9b6e0ecc9d1b5849738006d81515aea89373f3bfaef06d80ce19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8093845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ceda43db7c7c10503ce58f5adb0b2aff5a939be342d2ae7491f275f8b9bdf4`

```dockerfile
```

-	Layers:
	-	`sha256:845d02b3a0664ac7fad2313c074fec2da6f09b9f6cdec20f7c35e3beb73eb652`  
		Last Modified: Mon, 11 Nov 2024 18:58:13 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a899e579497bb51652521013ff3c829a4607c0aa2f8b4fdbf89ae02a5969386`  
		Last Modified: Mon, 11 Nov 2024 18:58:12 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b2769eb9f333a0af56944cf6aeccaa59011c1a0516ef49ebb4f409e6df9215a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:f795a0b7bcae2aed78ff75c160e432f29f5022318ed775c9ebe7239c6e980e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272433307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb3c70ba41ba6d5e07cac213fe57b5469ba2763f3ea33a57f635f0e7b65a127`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f216b571f44a239d4f4c6d69a1dda566c45a9a44e799822dafdc9b32f5d6668`  
		Last Modified: Mon, 11 Nov 2024 18:58:44 GMT  
		Size: 272.4 MB (272424247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe5621576a3df3ebb05652537b68049fb9e3f436e27e360164a66aa89b43e7`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 9.1 KB (9060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d1feb1e3b4b3eaf4ad5b1b9c2baebca7a76f6113f9a0c0ee74d8de63f1caec1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969240571d7bd07eb46191fb9a61d4f9079b5101ede5e258f939e9c403c478d0`

```dockerfile
```

-	Layers:
	-	`sha256:274f4ca6bd6fba43e6f82acb2a725d3182c8de0f487cfbc1f1612179524c4598`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 11.9 MB (11895685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f1c4d2ba147e6ed43b078f92e41fb934c58b58168f43baf1af72ed6fd07c65`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20241110.0.278197`

```console
$ docker pull archlinux@sha256:b2769eb9f333a0af56944cf6aeccaa59011c1a0516ef49ebb4f409e6df9215a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel-20241110.0.278197` - linux; amd64

```console
$ docker pull archlinux@sha256:f795a0b7bcae2aed78ff75c160e432f29f5022318ed775c9ebe7239c6e980e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272433307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb3c70ba41ba6d5e07cac213fe57b5469ba2763f3ea33a57f635f0e7b65a127`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:6f216b571f44a239d4f4c6d69a1dda566c45a9a44e799822dafdc9b32f5d6668`  
		Last Modified: Mon, 11 Nov 2024 18:58:44 GMT  
		Size: 272.4 MB (272424247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afe5621576a3df3ebb05652537b68049fb9e3f436e27e360164a66aa89b43e7`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 9.1 KB (9060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel-20241110.0.278197` - unknown; unknown

```console
$ docker pull archlinux@sha256:d1feb1e3b4b3eaf4ad5b1b9c2baebca7a76f6113f9a0c0ee74d8de63f1caec1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11907222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:969240571d7bd07eb46191fb9a61d4f9079b5101ede5e258f939e9c403c478d0`

```dockerfile
```

-	Layers:
	-	`sha256:274f4ca6bd6fba43e6f82acb2a725d3182c8de0f487cfbc1f1612179524c4598`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 11.9 MB (11895685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f1c4d2ba147e6ed43b078f92e41fb934c58b58168f43baf1af72ed6fd07c65`  
		Last Modified: Mon, 11 Nov 2024 18:58:41 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:3c9c1b4058255ab69853cec0f04e12505fb6a25ffa5a2d3baf91032cb93b1525
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:098a55eaa21d67f4fac315702eea994316b7425c7da7947bfdc4a7d46d9edde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151295122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6161c1a4982fa9c04c584160b298e1f0578f25f2d229ac1e5d1d240201487b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2facfc8e7394aecded27d459bdc7e393d42a5694c20c8355bb630acf3cfcc63d`  
		Last Modified: Mon, 11 Nov 2024 18:58:14 GMT  
		Size: 151.3 MB (151286801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ba553329ad01d47c421f02a99b69b6a61b1e4f5db14017b3b538c2f15732aa`  
		Last Modified: Mon, 11 Nov 2024 18:58:12 GMT  
		Size: 8.3 KB (8321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:2f82d894985e9b6e0ecc9d1b5849738006d81515aea89373f3bfaef06d80ce19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8093845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ceda43db7c7c10503ce58f5adb0b2aff5a939be342d2ae7491f275f8b9bdf4`

```dockerfile
```

-	Layers:
	-	`sha256:845d02b3a0664ac7fad2313c074fec2da6f09b9f6cdec20f7c35e3beb73eb652`  
		Last Modified: Mon, 11 Nov 2024 18:58:13 GMT  
		Size: 8.1 MB (8082090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a899e579497bb51652521013ff3c829a4607c0aa2f8b4fdbf89ae02a5969386`  
		Last Modified: Mon, 11 Nov 2024 18:58:12 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:25f4d79c05832a338c8a05921364a93d1736e49eb6dbce9fb5d7a77b33730dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:7bdccad0d730d937cf13c0da67b52e9ab65113fcd7f7f6bcf92547934ff61da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c1ba506b1d4ded9900724a22b6c45c9a2b3fc1730b414ad8465bfe25a81d4f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3ab97c08b12194b39487459a35c6eae1338779f256278f9827959dea61a640bd`  
		Last Modified: Mon, 11 Nov 2024 18:58:58 GMT  
		Size: 322.3 MB (322278597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dffb47154ea1ce0649d809746d4f3756a12af61fe14ab6064dd05a811eaccf`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:8e5cf1acd9ba98bf4960b9ba1ae87525c03ec97c316703a4ad73e35aa7f2ee0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e3f9da20e701b50e519a2525d8e34c28a1b249fb2a95edd813f38552e216a4`

```dockerfile
```

-	Layers:
	-	`sha256:cd86b9436854dc6687c33dee316859237c3e1d9a846a2eca2a9616eaaba253e4`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 12.2 MB (12164481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415bf24fdb2d6674ad2ca5785ae568c336d36ec9e303b16a1cd660be5102e334`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20241110.0.278197`

```console
$ docker pull archlinux@sha256:25f4d79c05832a338c8a05921364a93d1736e49eb6dbce9fb5d7a77b33730dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel-20241110.0.278197` - linux; amd64

```console
$ docker pull archlinux@sha256:7bdccad0d730d937cf13c0da67b52e9ab65113fcd7f7f6bcf92547934ff61da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322288826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c1ba506b1d4ded9900724a22b6c45c9a2b3fc1730b414ad8465bfe25a81d4f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.version=20241110.0.278197
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 10 Nov 2024 00:07:43 GMT
LABEL org.opencontainers.image.created=2024-11-10T00:07:43+00:00
# Sun, 10 Nov 2024 00:07:43 GMT
COPY /rootfs/ / # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20241110.0.278197' /etc/os-release # buildkit
# Sun, 10 Nov 2024 00:07:43 GMT
ENV LANG=C.UTF-8
# Sun, 10 Nov 2024 00:07:43 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:3ab97c08b12194b39487459a35c6eae1338779f256278f9827959dea61a640bd`  
		Last Modified: Mon, 11 Nov 2024 18:58:58 GMT  
		Size: 322.3 MB (322278597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06dffb47154ea1ce0649d809746d4f3756a12af61fe14ab6064dd05a811eaccf`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel-20241110.0.278197` - unknown; unknown

```console
$ docker pull archlinux@sha256:8e5cf1acd9ba98bf4960b9ba1ae87525c03ec97c316703a4ad73e35aa7f2ee0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12176075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e3f9da20e701b50e519a2525d8e34c28a1b249fb2a95edd813f38552e216a4`

```dockerfile
```

-	Layers:
	-	`sha256:cd86b9436854dc6687c33dee316859237c3e1d9a846a2eca2a9616eaaba253e4`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 12.2 MB (12164481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415bf24fdb2d6674ad2ca5785ae568c336d36ec9e303b16a1cd660be5102e334`  
		Last Modified: Mon, 11 Nov 2024 18:58:54 GMT  
		Size: 11.6 KB (11594 bytes)  
		MIME: application/vnd.in-toto+json
