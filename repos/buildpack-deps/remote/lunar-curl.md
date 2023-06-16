## `buildpack-deps:lunar-curl`

```console
$ docker pull buildpack-deps@sha256:e6183b1efd217a959d23a96d43bb01c372883bb93f675d0f78fbe3ec56fc9c5e
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
$ docker pull buildpack-deps@sha256:61f8165c03b66199f977555fafe08162a630a16f065e0ceed29a208e80246d0b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40349017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203b76f8605ab7f37098a6b727a70b5b955f76e48db136ac819d1892587e8968`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:33:45 GMT
ARG RELEASE
# Tue, 23 May 2023 08:33:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:33:45 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:33:47 GMT
ADD file:b2902a85ba60d642b00f2d7d7e4f56825749dca527e2d8d5e64d854c76ed28f0 in / 
# Tue, 23 May 2023 08:33:47 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:799351a2e050dcbccac2616755ae9631d97278ecebbd4db013e40b3a849439c5`  
		Last Modified: Fri, 02 Jun 2023 00:05:52 GMT  
		Size: 27.0 MB (27017966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f53223904f9116e3fca0e8c45abe0ddd4a8c43584afe7ad09b9406e2d26a91`  
		Last Modified: Fri, 02 Jun 2023 00:05:49 GMT  
		Size: 13.3 MB (13331051 bytes)  
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
$ docker pull buildpack-deps@sha256:5a68259ff06e05d5bccf8c96bb8b1c4eb8de8d6673792dd842a95a870ab003e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40240481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15dddaabda002a74052772df33f7a797814d634decc6f724a177f4bdce84c84`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 May 2023 08:34:39 GMT
ARG RELEASE
# Tue, 23 May 2023 08:34:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 May 2023 08:34:39 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 23 May 2023 08:34:41 GMT
ADD file:390d5b6c76bd6ae4f2901362d9a308f7dc4fa9a83574ec3952e867bc951c1552 in / 
# Tue, 23 May 2023 08:34:41 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd80ecb7763a9e3fbf3b7c2b815d337acc04e6d1a42898eee903ca05160f9419`  
		Last Modified: Thu, 01 Jun 2023 23:19:54 GMT  
		Size: 26.2 MB (26236512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05916a9cc39edfb88d065692b72105e6d80b81387a04f196cce1b55eabc17c66`  
		Last Modified: Thu, 01 Jun 2023 23:19:53 GMT  
		Size: 14.0 MB (14003969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
