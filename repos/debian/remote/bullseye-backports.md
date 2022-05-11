## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:aefed68df20ecfe2a39b8d5bbf7ebad3074cb71153af8bdf73b0ad2dbe7583c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:f648a0c55eb9d4fd641ecc99d15abb4f0bc015fb27e2ad2a420c006b168c623b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54945845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51cfe562feb956d8b99448a87fdff1347370638d6d99b097d8f5ef7c9b4af937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:20:05 GMT
ADD file:68a5d7d0db592625159865110c1b7dcb15cf70ecf71b5fd541ef89584cd734ba in / 
# Wed, 11 May 2022 01:20:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:20:08 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:67e8aa6c8bbc76b1f2bccb3864b0887671833b8667dc1f6c965fcb0eac7e6402`  
		Last Modified: Wed, 11 May 2022 01:24:45 GMT  
		Size: 54.9 MB (54945622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d23b60a02c634028eaec370b83e7d3745882275f7a3337705e729c024004ca4`  
		Last Modified: Wed, 11 May 2022 01:25:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5ac485b588bc028c0c69e3e39750cf7eb0e5e89a250a1946a6a619744d23df86
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52476916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b090dbffd51e5f3ad904264a913616936f4661da704612770b0940654b832bc8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:59 GMT
ADD file:b4fea5a360c5cca5abc5866da48126a30eeaf4e976d09c479958fe445dae8021 in / 
# Wed, 11 May 2022 00:49:59 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:50:16 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0ca4fabca59ca0d617061b776745ff41fdc3968ce90dd2b9198717e0bae91d98`  
		Last Modified: Wed, 11 May 2022 01:05:03 GMT  
		Size: 52.5 MB (52476689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a0e22799d830428109d08dacdcac932130ffb23a4797141403570088ddc1ad`  
		Last Modified: Wed, 11 May 2022 01:05:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f009cd3f06ae1f9be72f96c330e26f87d8c0479ae2f77cb8b3645691b3928d56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50134296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a754c579ac9701e23b5e1946c59d22fe24d6604e3bd4295546fe6018b497c321`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:48:30 GMT
ADD file:d6545064ea0f75166d59e4d4a2df1e41a3477ae468e558e31f29857336978c0e in / 
# Wed, 11 May 2022 01:48:31 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:48:47 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ba38f9a6c66968e207a7ada348a2110e3be0ff117e621d9e10ddd7c4becc0d2a`  
		Last Modified: Wed, 11 May 2022 02:03:49 GMT  
		Size: 50.1 MB (50134069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267f5442067fb0e5fc19f11434b11c72d331f0ffc68565f89c12761f83deb0aa`  
		Last Modified: Wed, 11 May 2022 02:04:12 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8c6155d0993698cbc4b36721e3e323870b49ce57ad023f171d63e2c51846fb89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53634561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32257ff300e1a156929b6ee2771df345e029713ba5c7332ff0f95072de14d996`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:44 GMT
ADD file:239aa42118877a929b2fbfc0d5793fee7815289280affa5286de2459385c0679 in / 
# Wed, 11 May 2022 00:46:44 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:46:52 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3a36574378e6cece2dd3a839e1c0220eaccc4063b61d7481d1a19d3990c1f2c2`  
		Last Modified: Wed, 11 May 2022 00:53:15 GMT  
		Size: 53.6 MB (53634337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cfc29c29380e005e7cbd7c201dca43686086b4b253f069bf6f1a4b1c8922f7`  
		Last Modified: Wed, 11 May 2022 00:53:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:cdbd022451400b303fe27d87c9c6c75412b01e16d55a30db0976ed0ca1390890
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55943058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fef1a21b770d51bd1fbdb7eaa94cb0b56403a346f6b81c8fe2bdaa7774f41b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:38:57 GMT
ADD file:dae3dc662d1327f461e95b84f6f9282f3c4fb51f16ac8f20a5f141951d8436a9 in / 
# Wed, 11 May 2022 01:38:58 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:39:05 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5ad4f92623738998bc77103ff64344255f842f6e5fe4a846df656351b3c4852f`  
		Last Modified: Wed, 11 May 2022 01:45:53 GMT  
		Size: 55.9 MB (55942833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2bbf9fef6f3176980f60c2a36740e044181cfb0bc6ebe83f85eefee106c759`  
		Last Modified: Wed, 11 May 2022 01:46:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:9a995b1c25e7c084432dd07c951e013fb582beaca6a246042b59cc67a410af06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53205767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9ae758ad55e8cc960b1e3e0991d23323a9381b8b7c4007944f338ef8c80e16e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 02:22:56 GMT
ADD file:eb055eefa53e1ab6b7358bc8e543f3b7e2016eb48a65d6930cc4b4367b380cfd in / 
# Wed, 11 May 2022 02:23:02 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:23:15 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0723f7ee145d9214b27021d88822f2da789ed74e757924ae6c8074085507c2dd`  
		Last Modified: Wed, 11 May 2022 02:33:00 GMT  
		Size: 53.2 MB (53205540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f5f4128694b9c22a03e86af67b8992cff33e54e1a88faee3c5cda6a001f7d6`  
		Last Modified: Wed, 11 May 2022 02:33:17 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ea4114cdd96d0295f10b2ad746302c2d7bec5d4af3401b318b356d92d437f6bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58836753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:601ea6a790f4e830de0248e29607c70ecaf6edd8f15c2f1e93f842f263aaccef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:31:46 GMT
ADD file:6d7393a3491f45287b6b9a4c97432db92f762fc320e7b4527fa0969250c7cda6 in / 
# Wed, 11 May 2022 01:31:53 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:32:14 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8ad85695cd2aa86dcc7fc175edbdd1c94dbfa061000f3770d4e6f795df7d74c9`  
		Last Modified: Wed, 11 May 2022 01:42:22 GMT  
		Size: 58.8 MB (58836524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9061cabaf9773189e70b4e71e0890bde5007eaad2b6f09bf883ad9fa1c45f3dd`  
		Last Modified: Wed, 11 May 2022 01:42:47 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:6810d8ddbe534405322ed601945ababb85dd5fd73ebf14f06f8cce43860b338f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53208921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3103c6d34bca2898807a9d730397b8d076531454cf8e4caa0fd52239b3d7a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:43:58 GMT
ADD file:8b9cfb1e16e1c11cdc1f936ccd3dfdd2104ab85b0b9078b1fe3bca89f53e0682 in / 
# Wed, 11 May 2022 00:44:00 GMT
CMD ["bash"]
# Wed, 11 May 2022 00:44:09 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f8313f715dc1cdd9f8a3da73eafca06dcb30dff4c078bee35a162247cae99c4d`  
		Last Modified: Wed, 11 May 2022 00:49:41 GMT  
		Size: 53.2 MB (53208696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bb88e8aa94d2043f0c4149d6fcc8c33b0634815d05315a3d03ba1f8cf35cfc`  
		Last Modified: Wed, 11 May 2022 00:49:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
