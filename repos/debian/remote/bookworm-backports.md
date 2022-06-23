## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:aded31316315d7081f99d09be07448616bfce72916dc08975fb6349e8967df81
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:02730bed17106a177ea16ce7bba1224e3fd1be3bce085ff790133380683250e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52994206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e550058ac1a5f1b412dd543173df88a84365855436e38bc34e122d69ab82a686`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:19:54 GMT
ADD file:7e968e6ae38ede120a52f1d2e734b4fee4fd4ffd6e5f747edc8190d2a8bc6a52 in / 
# Thu, 23 Jun 2022 00:19:56 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:20:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8849e73adf621df4a443e9ac4eec9b698476e4f14f8ed894806f302d5b33156b`  
		Last Modified: Thu, 23 Jun 2022 00:24:12 GMT  
		Size: 53.0 MB (52993983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baec0e933ef4d12c74562b25bc861ca80dc538738f2a719dceaf4f2b6dfca53b`  
		Last Modified: Thu, 23 Jun 2022 00:24:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:70464b58e32c951bd97575096efb9e81268651e2685e77bb5c55c3c76d288ca0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50768070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c40192147d7cef8f29fbe266936b7445968765742090e0c652ef74942f0a8f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:49:07 GMT
ADD file:d8a58d5f4d1c34aefbf2ca6b2eeab0bbf20b8cb6400548926c6a16cce570dc9d in / 
# Thu, 23 Jun 2022 00:49:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:49:20 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5248fb4f18035bd1257a3136675241430095c1cdf250910c001999b7f421381c`  
		Last Modified: Thu, 23 Jun 2022 01:03:30 GMT  
		Size: 50.8 MB (50767843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa0a3772da58dcdf05008179cc22c13802ccc1b97d0bcfe57c3d2e383f97699`  
		Last Modified: Thu, 23 Jun 2022 01:03:43 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:ba7a016efa438945e34a02a865f1428d4753c86d466d3f4cda86f49eef86394b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d55f321d3ac76325f63487d897e21a0f2d88ccc5825e2456b76994f2afd4b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:58:08 GMT
ADD file:485670bbc3d21c74d06e079229d1c74d05970c4bdf8c5d25692ab1464f0acfce in / 
# Thu, 23 Jun 2022 00:58:09 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:58:22 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:da5c76d2fa54760a1e859c83968ea6d7dfee1c43064fb6f34c27f8d639859b07`  
		Last Modified: Thu, 23 Jun 2022 01:13:19 GMT  
		Size: 48.5 MB (48506514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870a33a2f42343a2de22de16d5edc8f176e731f29a2c0d55d03d845765fd715`  
		Last Modified: Thu, 23 Jun 2022 01:13:31 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:9ed333d4d109ae360733d0ec4f457e10b5e25bcca673659ffe17d46e4b058544
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52074830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7201f5fa5d79d2f16ac530f5d94923e86cffe3266276bf7b0eb7694651718f6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:05 GMT
ADD file:149d923f098f33a347aa57ca673aae5cc103628b202337e4ff2ea5ac278e5c18 in / 
# Thu, 23 Jun 2022 00:40:05 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:40:11 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e34000263ac838bb9254930c5e34d9fa4b486f544707ae0aa508bb7ded624d59`  
		Last Modified: Thu, 23 Jun 2022 00:46:09 GMT  
		Size: 52.1 MB (52074605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d3cbf0dded20994dcb3a7105cd8f82dd6e6a376e6fe5d816a61a5901473f3d`  
		Last Modified: Thu, 23 Jun 2022 00:46:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:3b658f649d6999d958ca8280c855c197567321d423f3aa24bbeb5eb8645a77cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53963860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6dbff8f592b5e1b6ce1cfb9a1e07b655b8abe1f377a92d551d388802216d13`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:38:52 GMT
ADD file:d8108af9af2f3fb7f3dd905a9b4dd8391d568ba8dd590a9ca2bbeecd44354e03 in / 
# Thu, 23 Jun 2022 00:38:54 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:38:59 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0120d80f9ec3d96114e34087bd467cf9989c9c723cf7622bb16fb3675443565c`  
		Last Modified: Thu, 23 Jun 2022 00:45:18 GMT  
		Size: 54.0 MB (53963635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea902b39321f03e5af5ae2293ede5941e1d847a6c0dca983a1b9d5197632785a`  
		Last Modified: Thu, 23 Jun 2022 00:45:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:8d9f579874f1d6d1d7b1e3687e9421c1547385ad95f00aea4bbe8a45a2b637e4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52061859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19d9a4a679994d3e3c1323ac52b20ca7485951e880316dd160e6c86e082e869`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:09:18 GMT
ADD file:0db9365eff38bea353e789709159951d557685e098127d950e467c83468aadd7 in / 
# Sat, 28 May 2022 01:09:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:09:42 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:409912beaa99ac80f6ec57bce7ac6621f4659f5f43cdaf3152de94639a634798`  
		Last Modified: Sat, 28 May 2022 01:19:34 GMT  
		Size: 52.1 MB (52061634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d3a40fdbecff63c4beb672509e324b6a505607c4dfdf02dd1916814675e701`  
		Last Modified: Sat, 28 May 2022 01:19:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8b279a994ab0ce058b3fe8b97ed989bc6468e8d861cc9131181eb5ef6b3f6148
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57161813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ed173d89a2ba648d5d53a9fa1058dc2a873413062a25808a408c4db502bd78`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:21:20 GMT
ADD file:af4ab80f98b1cc5089a94e2932d676aad92fb52c2f59476cc64955602ea3d330 in / 
# Sat, 28 May 2022 01:21:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:21:48 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b80d749a1cbc85d39c24118acb8615cd7c0ba93c2cb7561974f0473b9863a264`  
		Last Modified: Sat, 28 May 2022 01:30:55 GMT  
		Size: 57.2 MB (57161586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee69cb413e115137616d0f02a36cd1a645ab9e964d6fd148bbf1110c153836f3`  
		Last Modified: Sat, 28 May 2022 01:31:08 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:d77b292cf294f1d4ec825ce447d7b20899892e9ebc6d57705a8e658d9e5cedc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51530798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225fa13806a6d7a64cd1d366908263a89c006761da73f05b94826cdcd1fa69a8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:41:51 GMT
ADD file:b7c920f3965a4e47e7a0f42e020e195f493babee2f175c563676dd0d45c0b27b in / 
# Thu, 23 Jun 2022 00:41:58 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:42:08 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bb926b744d748e9437f2a0a451eea25192350981dae9cf0d8effd239dd22e761`  
		Last Modified: Thu, 23 Jun 2022 00:51:01 GMT  
		Size: 51.5 MB (51530571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e6d64aeab99a4a0c99290e5d483c79f00d4f313057a28c50be02e5cea819c`  
		Last Modified: Thu, 23 Jun 2022 00:51:09 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
