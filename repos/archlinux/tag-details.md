<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240825.0.257728`](#archlinuxbase-202408250257728)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240825.0.257728`](#archlinuxbase-devel-202408250257728)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240825.0.257728`](#archlinuxmultilib-devel-202408250257728)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:a750678fba4213b3d4054b88218b314733594e887d44be2a59fdf61cf6a5c641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:649f22ffe44950a2fbdd7b4f3ad7eaf1ae017d60360f857ba1b07902121824d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151193892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd09adc826967eb17f91d1b34e2f25a5bacb786a7d2daa7b42ab8726ce296cd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.version=20240818.0.255804
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.created=2024-08-18T00:07:58+00:00
# Sun, 18 Aug 2024 00:07:58 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240818.0.255804' /etc/os-release # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 18 Aug 2024 00:07:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9ed62a58ff74bd4fb28a245ec0e2ccba3ffe5d464456f8e0deedb4e20501291a`  
		Last Modified: Mon, 19 Aug 2024 17:57:40 GMT  
		Size: 151.2 MB (151185620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00da84d1f8972f5df6c181e1d3fbff6c3f801c27dee24820bec518e802577bc`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 8.3 KB (8272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:d97ca1db468c618434ab7ffe94bbcad8c8a42ac29719b47916d634c9e47ff671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c29c967e415355d4f29d75cc6a91fba3ec01900d2ea620f97c0a895dd364942`

```dockerfile
```

-	Layers:
	-	`sha256:f8a51f688d53dc94414d7de4e91bddd8f54788b4c2aa2fe570b72fe692b759fb`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 8.1 MB (8103931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f853272c82e70efd1417a28fba73b4ed94db1220a8a0e0395802fbb38ecdd3`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240825.0.257728`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:b212ba57dea42f74f3197e5926ec6b9dece07bbc17147afb91db874549b5fd11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:499525353b9944a10f65f1266d08c93fd18bc1dc957d993a93a4a24e174f2c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271745957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdd7b7c6cf0339af07a9d0e072cc511d722117513ec2fb3d010bd46e024ad8b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.version=20240818.0.255804
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.created=2024-08-18T00:07:58+00:00
# Sun, 18 Aug 2024 00:07:58 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240818.0.255804' /etc/os-release # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 18 Aug 2024 00:07:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:24b1c3c45b6ca33f24c75d7f2e4306cd305f51c8872d4f9047898a8c60b6a0b3`  
		Last Modified: Mon, 19 Aug 2024 17:58:28 GMT  
		Size: 271.7 MB (271736915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed4f37407001e5dc344a5c6dd67a4dfec15d9692c6675b174b36fa8cbe85afa`  
		Last Modified: Mon, 19 Aug 2024 17:58:20 GMT  
		Size: 9.0 KB (9042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:9608e74653b13d26c01aa68dd4cc93aa97d41b2e88aacd7c135cbb3d2c6fb1c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11829653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e711d12dec1851e0b37d58b1726bc94c8731ae533b7671ee4d96133dad7ba8`

```dockerfile
```

-	Layers:
	-	`sha256:b628a25d8c672a0297a0cc33637ba042d9379aedf6237272923f767085434ecb`  
		Last Modified: Mon, 19 Aug 2024 17:58:21 GMT  
		Size: 11.8 MB (11818150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4e66114aedecd35b14ceec19f0277ff10b61c3eccdcb51373ad3c3ec9f2332`  
		Last Modified: Mon, 19 Aug 2024 17:58:20 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240825.0.257728`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:a750678fba4213b3d4054b88218b314733594e887d44be2a59fdf61cf6a5c641
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:649f22ffe44950a2fbdd7b4f3ad7eaf1ae017d60360f857ba1b07902121824d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151193892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd09adc826967eb17f91d1b34e2f25a5bacb786a7d2daa7b42ab8726ce296cd`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.version=20240818.0.255804
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.created=2024-08-18T00:07:58+00:00
# Sun, 18 Aug 2024 00:07:58 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240818.0.255804' /etc/os-release # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 18 Aug 2024 00:07:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:9ed62a58ff74bd4fb28a245ec0e2ccba3ffe5d464456f8e0deedb4e20501291a`  
		Last Modified: Mon, 19 Aug 2024 17:57:40 GMT  
		Size: 151.2 MB (151185620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00da84d1f8972f5df6c181e1d3fbff6c3f801c27dee24820bec518e802577bc`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 8.3 KB (8272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:d97ca1db468c618434ab7ffe94bbcad8c8a42ac29719b47916d634c9e47ff671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8115652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c29c967e415355d4f29d75cc6a91fba3ec01900d2ea620f97c0a895dd364942`

```dockerfile
```

-	Layers:
	-	`sha256:f8a51f688d53dc94414d7de4e91bddd8f54788b4c2aa2fe570b72fe692b759fb`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 8.1 MB (8103931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f853272c82e70efd1417a28fba73b4ed94db1220a8a0e0395802fbb38ecdd3`  
		Last Modified: Mon, 19 Aug 2024 17:57:38 GMT  
		Size: 11.7 KB (11721 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:8cc78a4be8187154c85b6b86b31e0d5f32f308c98a1ef5a5f017dcf804aa886c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:04abbe09ca0c911252f652215e2af0158e45e55a8d7121d55091ef9fd284d186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321631214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9964a66ed08b0753a74276dacabc149348c5df2c10b3e5892092d8223631a26f`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.version=20240818.0.255804
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 18 Aug 2024 00:07:58 GMT
LABEL org.opencontainers.image.created=2024-08-18T00:07:58+00:00
# Sun, 18 Aug 2024 00:07:58 GMT
COPY /rootfs/ / # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240818.0.255804' /etc/os-release # buildkit
# Sun, 18 Aug 2024 00:07:58 GMT
ENV LANG=C.UTF-8
# Sun, 18 Aug 2024 00:07:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:461b8e0f36a974d10a4a68614097d8c97bc72bffc076091c4f99f4da2a7c4750`  
		Last Modified: Mon, 19 Aug 2024 17:58:20 GMT  
		Size: 321.6 MB (321621015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b414534c83a12bc64b75c8dc755917109916e743ad43b65dc765b3df2bd058c1`  
		Last Modified: Mon, 19 Aug 2024 17:58:15 GMT  
		Size: 10.2 KB (10199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:d80aa1ce622836554dcf63dd99ee84fb31e5c7c731520a6ee81f8446f7a1f3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.1 MB (12097022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc830055c1405a0292b3aa0a099105a708148c26bfefa335337d005b5ddc5e9`

```dockerfile
```

-	Layers:
	-	`sha256:f3a38db00163f734fbb964073b4a4a7f3d159679230532cf4ade44afa14f18d9`  
		Last Modified: Mon, 19 Aug 2024 17:58:16 GMT  
		Size: 12.1 MB (12085462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edeb1b6ff87f8417bc493bec00e926de21dcfc0ca887dfc560c8c325d06353d0`  
		Last Modified: Mon, 19 Aug 2024 17:58:15 GMT  
		Size: 11.6 KB (11560 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240825.0.257728`

```console
$ docker pull archlinux@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
