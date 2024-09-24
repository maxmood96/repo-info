<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `archlinux`

-	[`archlinux:base`](#archlinuxbase)
-	[`archlinux:base-20240922.0.264758`](#archlinuxbase-202409220264758)
-	[`archlinux:base-devel`](#archlinuxbase-devel)
-	[`archlinux:base-devel-20240922.0.264758`](#archlinuxbase-devel-202409220264758)
-	[`archlinux:latest`](#archlinuxlatest)
-	[`archlinux:multilib-devel`](#archlinuxmultilib-devel)
-	[`archlinux:multilib-devel-20240922.0.264758`](#archlinuxmultilib-devel-202409220264758)

## `archlinux:base`

```console
$ docker pull archlinux@sha256:729afdc31856d0faf2c93c2291f3e81bccd5e75082f45e0f3513f65f83b88973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:9d8002a9a805c88311039f050170eb14869df3b1edb525b72a03071f27769744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151134668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91721497913e579ac4e370dac68221b7800d88a9b3a7958f2ca27b17585f6b7a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240915.0.262934
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-15T00:07:28+00:00
# Sun, 15 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240915.0.262934' /etc/os-release # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 15 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:913facc7a97f31827a37ce293c99494796700c08c8eeeb0248dca1afae3f5c5c`  
		Last Modified: Mon, 16 Sep 2024 17:56:53 GMT  
		Size: 151.1 MB (151126440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9ac91550b6b2fb5cd51322f7c95fc35769726e272cdf1d09ea924b44e0bba`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 8.2 KB (8228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base` - unknown; unknown

```console
$ docker pull archlinux@sha256:f09cbd701b523029c6c1f03c2be671775da8d5c3a6a0cbb7d65d94397c4157fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8113930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daeddc386ac6f6acde612795ed4aca688b3d0eb4fc6c20748cd5fed3aa78eda`

```dockerfile
```

-	Layers:
	-	`sha256:a33233f144321ed1571b8be64f0563f4711ffafddc79af4aeb4c5688be78884c`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 8.1 MB (8102210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa1a7aedb81bb3177773eff83634a4d726ada1e96dec3379cfd00d07e14cd30`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 11.7 KB (11720 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-20240922.0.264758`

**does not exist** (yet?)

## `archlinux:base-devel`

```console
$ docker pull archlinux@sha256:a584d21535afcd833ded9bbd6e0fc0907b203fcfa8b11669f853866bde0c0ed9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:base-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:50021a00197cd7c4d8903987f79f92bc47170becdf7f33c3eb53751ad7802bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272145934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a332277d0673794c29e114d8cf46e21748e498cc3d3aad0c1c1199a99fd0b`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base-devel Image
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240915.0.262934
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-15T00:07:28+00:00
# Sun, 15 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240915.0.262934' /etc/os-release # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 15 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:d23292aad988212b9982631af27846dc7074de944c9c7b732bb709fb1a408bfb`  
		Last Modified: Mon, 16 Sep 2024 17:57:22 GMT  
		Size: 272.1 MB (272136925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f81783a1cbaf12250e3d4b9d6c37907f02e0302f2904a724d5e357c9ade1e9`  
		Last Modified: Mon, 16 Sep 2024 17:57:18 GMT  
		Size: 9.0 KB (9009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:base-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:bef09cc5829cc45485c5455297f6599c56d7c3d4968f375dfd6a80cb1ddc1a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11912073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21d2bd38b0fd06aa514231fca6a73927c72a8e62c64261e834d0a536414b683`

```dockerfile
```

-	Layers:
	-	`sha256:a02d99b8cb3ebcc1af8d3eaabdfe85f71bb3448b5365c682fd24c0c72f92a593`  
		Last Modified: Mon, 16 Sep 2024 17:57:19 GMT  
		Size: 11.9 MB (11900570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50d59023a8f8fd372339b84d5569b2f9ddcea99293100dcd541d147ae0351c0d`  
		Last Modified: Mon, 16 Sep 2024 17:57:18 GMT  
		Size: 11.5 KB (11503 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:base-devel-20240922.0.264758`

**does not exist** (yet?)

## `archlinux:latest`

```console
$ docker pull archlinux@sha256:729afdc31856d0faf2c93c2291f3e81bccd5e75082f45e0f3513f65f83b88973
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:latest` - linux; amd64

```console
$ docker pull archlinux@sha256:9d8002a9a805c88311039f050170eb14869df3b1edb525b72a03071f27769744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151134668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91721497913e579ac4e370dac68221b7800d88a9b3a7958f2ca27b17585f6b7a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux base Image
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240915.0.262934
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-15T00:07:28+00:00
# Sun, 15 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240915.0.262934' /etc/os-release # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 15 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:913facc7a97f31827a37ce293c99494796700c08c8eeeb0248dca1afae3f5c5c`  
		Last Modified: Mon, 16 Sep 2024 17:56:53 GMT  
		Size: 151.1 MB (151126440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9ac91550b6b2fb5cd51322f7c95fc35769726e272cdf1d09ea924b44e0bba`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 8.2 KB (8228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:latest` - unknown; unknown

```console
$ docker pull archlinux@sha256:f09cbd701b523029c6c1f03c2be671775da8d5c3a6a0cbb7d65d94397c4157fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8113930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daeddc386ac6f6acde612795ed4aca688b3d0eb4fc6c20748cd5fed3aa78eda`

```dockerfile
```

-	Layers:
	-	`sha256:a33233f144321ed1571b8be64f0563f4711ffafddc79af4aeb4c5688be78884c`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 8.1 MB (8102210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa1a7aedb81bb3177773eff83634a4d726ada1e96dec3379cfd00d07e14cd30`  
		Last Modified: Mon, 16 Sep 2024 17:56:51 GMT  
		Size: 11.7 KB (11720 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel`

```console
$ docker pull archlinux@sha256:9711b4be47a416b61be5b704e5d0c2151f9433aae0bc0a28605413da314a2835
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `archlinux:multilib-devel` - linux; amd64

```console
$ docker pull archlinux@sha256:fe7de951e3c9afde1c7c9212c1d0243de19a2f049b09d83713d486bf190a9d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321999667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f74b571feb32a8a6fe653d921a42a30124e0bc4969a1faea33a4482b80a05a`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.title=Arch Linux multilib-devel Image
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.description=Official containerd image of Arch Linux, a simple, lightweight Linux distribution aimed for flexibility.
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.authors=Santiago Torres-Arias <santiago@archlinux.org> (@SantiagoTorres), Christian Rebischke <Chris.Rebischke@archlinux.org> (@shibumi), Justin Kromlinger <hashworks@archlinux.org> (@hashworks)
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.url=https://gitlab.archlinux.org/archlinux/archlinux-docker/-/blob/master/README.md
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.documentation=https://wiki.archlinux.org/title/Docker#Arch_Linux
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.source=https://gitlab.archlinux.org/archlinux/archlinux-docker
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.licenses=GPL-3.0-or-later
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.version=20240915.0.262934
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.revision=61cb892bfc251e46f73e716ceb3b903ec4e9e725
# Sun, 15 Sep 2024 00:07:28 GMT
LABEL org.opencontainers.image.created=2024-09-15T00:07:28+00:00
# Sun, 15 Sep 2024 00:07:28 GMT
COPY /rootfs/ / # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=20240915.0.262934' /etc/os-release # buildkit
# Sun, 15 Sep 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Sun, 15 Sep 2024 00:07:28 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:49ede7ca1d036d7b0e613f74870a3c54440fde21de83c98af88d9e67a86bb40a`  
		Last Modified: Mon, 16 Sep 2024 17:57:32 GMT  
		Size: 322.0 MB (321989535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced223c1b6c1510942f6067b949d97fabf7753365280443cf865a0cda1d61162`  
		Last Modified: Mon, 16 Sep 2024 17:57:28 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `archlinux:multilib-devel` - unknown; unknown

```console
$ docker pull archlinux@sha256:05a144ecade139135171171a711654474b17071aa37683bdd1a654e89b1c06e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12179477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc3c2c563084daa3f259763729c8946a517337df80599093de4650790d2bb85`

```dockerfile
```

-	Layers:
	-	`sha256:2cff3358a1d6eb51475f87ba0040ec955100c828ea4e3d0baca2ddb279fce1c6`  
		Last Modified: Mon, 16 Sep 2024 17:57:28 GMT  
		Size: 12.2 MB (12167919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f00322cdee2cfdfbc1c0021a409cbaf4adffac4d445e10e0548065cb4a172c50`  
		Last Modified: Mon, 16 Sep 2024 17:57:28 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json

## `archlinux:multilib-devel-20240922.0.264758`

**does not exist** (yet?)
