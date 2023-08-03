## `buildpack-deps:lunar-curl`

```console
$ docker pull buildpack-deps@sha256:95ff4ba5a3d7ac6e6923fbd8956a8fabc7f5913cb0a2f01e33110fb95e2fe6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b4a7037ab529927d19c652a98edece16c14a141220bb94b2ae137372a910662
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41357035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb02a4320e2d201d51f16cac15f0e1a4bd615b6d5f6294bf6e3c45f3d864710`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:28:38 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:28:38 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:28:39 GMT
ADD file:708314051e878a0c6071fb2c8d4458a04ce058f47f2cfaa58c1b5a42e837ca0f in / 
# Thu, 15 Jun 2023 08:28:40 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ccc37bca66e7c29e0d65a4279511fe9a93932a4bb80e79e95144f3812632b61a`  
		Last Modified: Fri, 16 Jun 2023 01:56:54 GMT  
		Size: 27.6 MB (27612943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7beeb5a79f9bd13c90ee4c9f68636fc642df773adb1bd04e27e2115f6c12a6d`  
		Last Modified: Fri, 16 Jun 2023 01:56:52 GMT  
		Size: 13.7 MB (13744092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:61de8a1c369fb750af225159ced6e4c45df3ad711c10ad9598b6764df05f9f06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38095712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217162e2f73ec8805a9bcc072434a36250aaff6d65a445fba2cc1fc08f1ed000`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:10:50 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:10:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:10:51 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:10:53 GMT
ADD file:8484efc06b5f22d170eef374f45df452d8e36f4cbef702f7ee4d1f130dd28093 in / 
# Thu, 15 Jun 2023 08:10:53 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 00:49:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ca5128fe76949cc104af7f40ce0f7213fe093079077d47dd525fa0189090c57e`  
		Last Modified: Fri, 16 Jun 2023 00:59:51 GMT  
		Size: 25.4 MB (25432780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d8ca764d56bdf14c46fabd5c4e2e988ce166d01c8c0631d7c345802ace7bf1`  
		Last Modified: Fri, 16 Jun 2023 00:59:50 GMT  
		Size: 12.7 MB (12662932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:15e1b21e95f850df357ce2723b32b5ccf5191bcc1ab7476ec7bda4eec7b2dc98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40365279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d91090cdeb11e3d5f2aa2be50867a5582c1cf78e454986031a529673b37e45`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:24:02 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:24:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:24:02 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:24:11 GMT
ADD file:8af4f6767fc5b6665bedd4600c0601ee7d7f803de51e979a40bd3d6ebcd25f95 in / 
# Mon, 31 Jul 2023 17:24:12 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:38:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc3ebe95800c7b88cce17a04cb6a4e51211ef73656bd15c0885a6f96b173aeef`  
		Last Modified: Thu, 03 Aug 2023 00:50:53 GMT  
		Size: 27.0 MB (27031709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c53b82c57224a6aeb0716a4227436ebcf006fbd33ca9346c8875243d0ba942`  
		Last Modified: Thu, 03 Aug 2023 00:50:50 GMT  
		Size: 13.3 MB (13333570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dc5e0428f7f0c3135af8d7fee001e103cea834d13b0ec934142f1415dd644071
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47852374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6d6cf91b670992b73799b26277cc6486e785cb084948d3c1fa3bb5d0d71f89`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jun 2023 08:29:14 GMT
ARG RELEASE
# Thu, 15 Jun 2023 08:29:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 15 Jun 2023 08:29:15 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 15 Jun 2023 08:29:17 GMT
ADD file:5ebdf4bd4bc2b27019f20fb1964a395fa504d4f20e208c54237e363895b492d7 in / 
# Thu, 15 Jun 2023 08:29:18 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:11:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a58a0b662b0d4d5e271c7c17f35795b5782a33c69a079e473f7c2303bee50024`  
		Last Modified: Fri, 16 Jun 2023 01:28:52 GMT  
		Size: 32.0 MB (32010412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6f165de89ef5a3a93777200dd180f02a8fc30051f7eb6267300a3e6f27ae1e`  
		Last Modified: Fri, 16 Jun 2023 01:28:48 GMT  
		Size: 15.8 MB (15841962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2d8abebd9d4b6cc7fe03f5e7a5a9ef302dbd29def81c6e0f8041ef083e161e87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40249694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81083bbb06be2b6c5b21c6531f4a63810a49fefb639db3d8523c3c75bba5b77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 31 Jul 2023 17:25:09 GMT
ARG RELEASE
# Mon, 31 Jul 2023 17:25:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 31 Jul 2023 17:25:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 31 Jul 2023 17:25:10 GMT
LABEL org.opencontainers.image.version=23.04
# Mon, 31 Jul 2023 17:25:11 GMT
ADD file:02e6a6123ef99d36f86e3e53231b3ba93c90b4ac9fc0bdebe8f01f2a6c2efb4e in / 
# Mon, 31 Jul 2023 17:25:11 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:12:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec64faa69090fa13dbf3419726044381d0c7137866daa46daa6a85f785a5389a`  
		Last Modified: Thu, 03 Aug 2023 00:21:59 GMT  
		Size: 26.2 MB (26244138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6910656a90f2717882b9ec910b9f54fd6d237915853a5ffd4b160913158408a2`  
		Last Modified: Thu, 03 Aug 2023 00:21:57 GMT  
		Size: 14.0 MB (14005556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
