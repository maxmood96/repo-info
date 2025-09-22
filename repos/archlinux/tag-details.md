<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20250921.0.423275`](#archlinuxbase-202509210423275)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20250921.0.423275`](#archlinuxbase-devel-202509210423275)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20250921.0.423275`](#archlinuxmultilib-devel-202509210423275)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:8fe9851fcd8bd23ea0e6bfa99483d8778e40b45e0fd7bb8188c94cbdd8c25a38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:7b7bba26926c8bae835082a400fc0b5615a91fa3cfa56183ffede8ab69d3f8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164323307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b444b8a5550863744f1d1c07cef8a7137a9ed15c80631234658a74765e55eca9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250914.0.420821
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-14T00:07:14+00:00
# Sun, 14 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250914.0.420821' /etc/os-release # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 14 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9ed1b528ba03ff7a3bb0ffaccb1317530ae62b73bc0294667d34c927515d4136`  
		Last Modified: Mon, 15 Sep 2025 17:47:17 GMT  
		Size: 164.3 MB (164314969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e711ed963937def6a325b6ec32aca2cf29018e0d5e6d9f8b0d4cdab61791cf0`  
		Last Modified: Mon, 15 Sep 2025 17:00:09 GMT  
		Size: 8.3 KB (8338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:a5ec181549203664e58112d11d192d26785c36b7c1004aff1aae4bed2ea94042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96c8eeba9a9e8631242ea6723ce107c17819f95172e82fdd54ab3e75e8b4df2`

```dockerfile
```

-	Layers:
	-	`sha256:3900cebcc0b1edb531d3da51fd836f7a1e11c925e71fd88b1eccffbda043cad2`  
		Last Modified: Mon, 15 Sep 2025 19:48:17 GMT  
		Size: 8.2 MB (8182745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6119ef2b478ab0b116046a9bec2dffc49acfeaca24e0b6c9a90489537cecd2`  
		Last Modified: Mon, 15 Sep 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20250921.0.423275`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:9019fd8b026064ee6bbbe3fe38686b058752a14b1a9960fd9048509ebd72b5f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c9d775751f4db6799ba3ea8dc5145bc55cc1a5a704668865a98a581889fa44ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289424783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1ccfc6dc51b6f9e681e0af0d775d9c1d407ae4722ec29aec5e23b6ef013d7d`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250914.0.420821
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-14T00:07:14+00:00
# Sun, 14 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250914.0.420821' /etc/os-release # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 14 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:2c5033a95e457971d4d5938e5a753faa2114aabd3ffe3947ff3bfed3170b552f`  
		Last Modified: Mon, 15 Sep 2025 19:49:43 GMT  
		Size: 289.4 MB (289415608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e20e2a0f08d7d3640a21ce42ca13b73e7490729c837acae9fdd9cb2dad0c64c`  
		Last Modified: Mon, 15 Sep 2025 17:00:53 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:b411f2009b4dd0c9ede0afb7d91e56017c166feaf733b065445d2016e73e6d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12095909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c384adb2cf9337d34b130328723db5d2fcc1d4cba90f930eac73da1c7545edc6`

```dockerfile
```

-	Layers:
	-	`sha256:ac1519a6eca3b70b3d74866947aaf32063c01ab711c12551e1b42a6b77c7ed1c`  
		Last Modified: Mon, 15 Sep 2025 19:48:22 GMT  
		Size: 12.1 MB (12084155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed1f723b393e89ea25368da7bf228dd63e870edffdc24c2a339e05f1cc901d0`  
		Last Modified: Mon, 15 Sep 2025 19:48:23 GMT  
		Size: 11.8 KB (11754 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20250921.0.423275`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:8fe9851fcd8bd23ea0e6bfa99483d8778e40b45e0fd7bb8188c94cbdd8c25a38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:7b7bba26926c8bae835082a400fc0b5615a91fa3cfa56183ffede8ab69d3f8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164323307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b444b8a5550863744f1d1c07cef8a7137a9ed15c80631234658a74765e55eca9`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250914.0.420821
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-14T00:07:14+00:00
# Sun, 14 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250914.0.420821' /etc/os-release # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 14 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9ed1b528ba03ff7a3bb0ffaccb1317530ae62b73bc0294667d34c927515d4136`  
		Last Modified: Mon, 15 Sep 2025 17:47:17 GMT  
		Size: 164.3 MB (164314969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e711ed963937def6a325b6ec32aca2cf29018e0d5e6d9f8b0d4cdab61791cf0`  
		Last Modified: Mon, 15 Sep 2025 17:00:09 GMT  
		Size: 8.3 KB (8338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:a5ec181549203664e58112d11d192d26785c36b7c1004aff1aae4bed2ea94042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8194717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96c8eeba9a9e8631242ea6723ce107c17819f95172e82fdd54ab3e75e8b4df2`

```dockerfile
```

-	Layers:
	-	`sha256:3900cebcc0b1edb531d3da51fd836f7a1e11c925e71fd88b1eccffbda043cad2`  
		Last Modified: Mon, 15 Sep 2025 19:48:17 GMT  
		Size: 8.2 MB (8182745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6119ef2b478ab0b116046a9bec2dffc49acfeaca24e0b6c9a90489537cecd2`  
		Last Modified: Mon, 15 Sep 2025 19:48:18 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:31c2103de5109437b8d9f48accfaf526a3191c6b1f92ba87371331f7d4ff99bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:c2dc5ad75555575d940a924c65b276f7183cf1d3cebe60cdefd5f08bfa66e94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340729932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6826e30ceeb7b4bce3fead594bfa2ae3e21daf9b55d3bdd3bdf4aa18771d3b0f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.version=20250914.0.420821
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.revision=744b1c5c6a7f999c9a8b3daa5897c922e86563ee
# Sun, 14 Sep 2025 00:07:14 GMT
LABEL org.opencontainers.image.created=2025-09-14T00:07:14+00:00
# Sun, 14 Sep 2025 00:07:14 GMT
COPY /rootfs/ / # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20250914.0.420821' /etc/os-release # buildkit
# Sun, 14 Sep 2025 00:07:14 GMT
ENV LANG=C.UTF-8
# Sun, 14 Sep 2025 00:07:14 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9f25f03a61659fe88c998948478e8e8f4a78af4baae6861c412264c76cefc2b6`  
		Last Modified: Mon, 15 Sep 2025 17:06:59 GMT  
		Size: 340.7 MB (340719665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfafbbd681a837939cadf718167f2af172360fd711bb567305c2b211eeeb494`  
		Last Modified: Mon, 15 Sep 2025 17:01:06 GMT  
		Size: 10.3 KB (10267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:24083930c4b61846e3f755875a11552711957c6077032fe49372655b16076255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 MB (12364860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cf0ae21e4fe36e3c456e424fd048d968ef00a9c7141f2cc8a6c8911b12190a`

```dockerfile
```

-	Layers:
	-	`sha256:08b76a7a61d4cb877dc88025799a71acbacfdae595c647e7929ad213895d1e37`  
		Last Modified: Mon, 15 Sep 2025 19:48:36 GMT  
		Size: 12.4 MB (12353049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a8a116e8ead8b781f97da6ea87d3fb5f8a3a8449fc8ef7f0a56c5ab3676f42`  
		Last Modified: Mon, 15 Sep 2025 19:48:37 GMT  
		Size: 11.8 KB (11811 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20250921.0.423275`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
