## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:b8812ba17cdd9fd75d56c9e3fbbd218c1c14100e255e7eeb73329c41caafe29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5c1827e50e583a398cd7306ea1db41842cfed7560e49c00fe82b8bf8553f086e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130124780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02204df23e3a57c40fdbcc8c771e0b7bc347f784258360a7d18a619e1497abcc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:37:11 GMT
ADD file:96a5f24c28b0ba6960064c54e4643bc56eb6890db2c214c7d54bff6a00f9f049 in / 
# Tue, 13 Oct 2020 01:37:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:12:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:12:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:13:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:831751213a615bc3a20e0080e123bd3a2f1f1eef137b680b3101f3127cdff08e`  
		Last Modified: Tue, 13 Oct 2020 01:47:33 GMT  
		Size: 52.6 MB (52579873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0865ee0fc4d919fc9d8f50091271f48b9d93d23451b3b03fac42f42c4e96fa1f`  
		Last Modified: Tue, 13 Oct 2020 02:27:31 GMT  
		Size: 7.9 MB (7870921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bd8b5719c34db0bfc0bc2bf3ed420adc1b98d9bd7b52a7210a5b240141fcfa`  
		Last Modified: Tue, 13 Oct 2020 02:27:31 GMT  
		Size: 10.6 MB (10627128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795dd20b363a5e86e17eef25246cf865107b7b53efddf0728732147795d47037`  
		Last Modified: Tue, 13 Oct 2020 02:27:48 GMT  
		Size: 59.0 MB (59046858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:31624aca6f32b7f547d825b349e25c77e44340d1f139c3d5f6313c3dca3496e0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124675472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6597381d68581cbea31a509b8d4117b0a1a907ac5938ba0dcc81ab1ef1e22f71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:50:20 GMT
ADD file:1aac38d903afb61492480cd4bdcc33919b418ac4dc88e3fb01b1d0a1589769db in / 
# Tue, 13 Oct 2020 01:50:23 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 03:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:37:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 03:38:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17a424b21d91218fba0e197ed7ceea9ae2ea4b949acb3e096cdb220f324853f9`  
		Last Modified: Tue, 13 Oct 2020 02:00:22 GMT  
		Size: 50.5 MB (50502115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbc82abbf9107f3acf2d4b2788cd9581852a883fe44f4875b8f32d23b2b04c7`  
		Last Modified: Tue, 13 Oct 2020 04:05:43 GMT  
		Size: 7.4 MB (7444491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185e98d64e9c93a1facb94fa0c79188ed1d0c02d5280e1db1841f8df929613c3`  
		Last Modified: Tue, 13 Oct 2020 04:05:44 GMT  
		Size: 10.3 MB (10315464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a9ff5754c6d1ea4ba2619fea44db11263cf5996571e57b4e70c83924137a6`  
		Last Modified: Tue, 13 Oct 2020 04:06:12 GMT  
		Size: 56.4 MB (56413402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:56b5c51e7d5c732061b99fef9693e3a3ce68aab30557bc2c07ee866373720139
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119324978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6ccc5d0415bca5e56209d56e702e1b10b4485a8544a5d0d135028024fcd1f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:58:08 GMT
ADD file:fb1050c1c18a08781bda11a75976f0483098ae971141de440f987df6c3da5eb3 in / 
# Tue, 13 Oct 2020 00:58:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:30:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 01:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1cc4a9f93bac620cf7887911c999122564026a7a9c2ca50766b3df4909c806f`  
		Last Modified: Tue, 13 Oct 2020 01:07:26 GMT  
		Size: 48.2 MB (48236859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517c91bf44a59eaea16877bae5d96e8e3739abbb8f93ededbe1a6edd9132e278`  
		Last Modified: Tue, 13 Oct 2020 01:54:44 GMT  
		Size: 7.2 MB (7184130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df823445c24dabde93145f0baf428b813928d6b636054a35a13293faaf42511`  
		Last Modified: Tue, 13 Oct 2020 01:54:45 GMT  
		Size: 10.0 MB (9958643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb060b2a6181fd285876f2f88e84e4bedbabc6cdcada618897d7e19b8202827`  
		Last Modified: Tue, 13 Oct 2020 01:55:13 GMT  
		Size: 53.9 MB (53945346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5a25bc19edfaf7190d56d0754d290dc6808ec35c02e651f0d235d644086c6de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129154068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ff143dddb3798fcaa421c07f4a0c2e367d311ad429da577ba7785a3135a76d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:49 GMT
ADD file:78d9e0b86c707d2f2153d35cccb88e56434830b20463e2114857178cd2c28ed1 in / 
# Tue, 13 Oct 2020 01:39:52 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:29:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:29:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:30:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45ba759b265011063551ebfd452fd79c0d477ff10d2fc0261e7edc8e46a5d3d`  
		Last Modified: Tue, 13 Oct 2020 01:47:12 GMT  
		Size: 51.5 MB (51484292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96906616e2d4ce424db1417d034acc953ef44b819f5866e2e98cde19ec79e22e`  
		Last Modified: Tue, 13 Oct 2020 02:46:01 GMT  
		Size: 7.7 MB (7742559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abfcbcfc78d61faca659b2499d9df1584faa1fbc6589b71e7faa4bf3b8f6e9c`  
		Last Modified: Tue, 13 Oct 2020 02:46:01 GMT  
		Size: 10.6 MB (10636219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f8a88f2319e4196ea3383a53797f7b79f7da093c44c6f0d17d2ab0c9c93299`  
		Last Modified: Tue, 13 Oct 2020 02:46:26 GMT  
		Size: 59.3 MB (59290998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e4be63b3e296d6f4ee8f3d26b5112b01c232a7e875e818b285c4a2995966fc99
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133666226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c008254e675e885b031944e5306298e20cdc3cb23a70c445f00abddcda306b8e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:42 GMT
ADD file:ddac7d3208f9bb85ea4273acbe09812b15d0635131191fc86bbb4bc2b6872873 in / 
# Tue, 13 Oct 2020 01:39:42 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:17:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:17:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:18:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a47de09075d002c62b36280b2b99d0486d6cd50266e6d6601b5c88535d032924`  
		Last Modified: Tue, 13 Oct 2020 01:48:03 GMT  
		Size: 53.6 MB (53627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb79e160247595d474a4be5625892d5f99dae5a6432f72dfe50f479d8f1bd29`  
		Last Modified: Tue, 13 Oct 2020 02:36:48 GMT  
		Size: 8.0 MB (8046137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a31e3ced4c61ebf0b93021ede8fd74be48dc6b994fb61e0e99f0031dfa6bf3d`  
		Last Modified: Tue, 13 Oct 2020 02:36:49 GMT  
		Size: 11.0 MB (11015021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd42e0300ac0fec8fb6393766d3e7f40cc0ccaeb0188c68ace8079c1db610d26`  
		Last Modified: Tue, 13 Oct 2020 02:37:11 GMT  
		Size: 61.0 MB (60977331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3f6bb5e6b2229ec3244e9f85ea0b3a5167ad71c344702fedb2b4156cf2a92ef3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127218593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc7c336db6997f2380f4c0108b8f7fec0681ed51a5dbe95f95655dd8765d940`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:08:29 GMT
ADD file:ca35129fd2f6a5420278e6a1790ba92b4afcb01f474e67f950b277b7d75db37e in / 
# Tue, 13 Oct 2020 01:08:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:06:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:06:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:07:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:abe3595453fb68f277799325ac06eb70b1ca68c849710051325993f2f22b051f`  
		Last Modified: Tue, 13 Oct 2020 01:14:37 GMT  
		Size: 51.3 MB (51279779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290cae23b8ebfb371a811642ffb256d3e23ca0ff6150be76966ec0283d83125`  
		Last Modified: Tue, 13 Oct 2020 02:19:43 GMT  
		Size: 7.4 MB (7396581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef5dab7e9de3f6b935b8bb68d316252a7ad220b1cabcd3f4a3a27344fecdfb`  
		Last Modified: Tue, 13 Oct 2020 02:19:44 GMT  
		Size: 10.6 MB (10639069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a13a51d0114bb5c79dec589b9cd66342d75d46442b19d37ecb4d4aea0903864`  
		Last Modified: Tue, 13 Oct 2020 02:20:38 GMT  
		Size: 57.9 MB (57903164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1984964e17e3ef966ed20d15d138d40fdd47262a7998ca5385f31015be67ef1d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140915006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6317753d08034742ca5a4e5bb9fdf084dde48dfe95332aa141e4fe15a8dfbe06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:36:17 GMT
ADD file:29c9502df00306ab143f7a4895ecbd5188710e18fa501d1931dfffe0d2281c6f in / 
# Tue, 13 Oct 2020 01:36:23 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 08:44:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 08:45:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 08:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e449e1f1ecdd90acbe5e4ea9a9f941aa8dcee06a83eb2eff72fe4dd55cc20576`  
		Last Modified: Tue, 13 Oct 2020 01:47:12 GMT  
		Size: 56.5 MB (56486527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b868bd306c5ff6ba6bbe52fb1cc3deaa47fed5a1362d135d89cfca87a684e4a4`  
		Last Modified: Tue, 13 Oct 2020 09:29:49 GMT  
		Size: 8.3 MB (8307201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5bd324b7e56f3121bd85c3a06132da98d95654678c2a01b4439cab8adc5b5`  
		Last Modified: Tue, 13 Oct 2020 09:29:49 GMT  
		Size: 11.4 MB (11392086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26769c811da7971c25f9fab265e60dd509f2c8522ff89eea05deda913a34b33`  
		Last Modified: Tue, 13 Oct 2020 09:31:06 GMT  
		Size: 64.7 MB (64729192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:242434967d0e11b5460e3c125441a3326fd480bc365ff36988731fd3ab848d0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127380883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84bcb2639be6c29dc810033e18a9dc0c467a0468edf5109caefc471e3355277d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:35 GMT
ADD file:1952263a13d56f052b56241e876c31bad8764b58e4a2c516a99d4f39950caf39 in / 
# Tue, 13 Oct 2020 01:41:37 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:03:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:03:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf0128f5938d0a765169c542feff60f3c439d59fb9c4be101b86202a01e6f72d`  
		Last Modified: Tue, 13 Oct 2020 01:45:00 GMT  
		Size: 51.1 MB (51118723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b959444d9f887602c790b9d941e7fb570dcef590dc48846b621da06e4ceba2e2`  
		Last Modified: Tue, 13 Oct 2020 02:10:25 GMT  
		Size: 7.5 MB (7541005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524b8fa445700c4082be482549c0d7902ce50a93b37e1f7fc5d14c927285c3c`  
		Last Modified: Tue, 13 Oct 2020 02:10:25 GMT  
		Size: 10.5 MB (10505088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cb425e964f6a35cefee9f35323651b0036432a1ca4440bbc4126036b16886`  
		Last Modified: Tue, 13 Oct 2020 02:10:40 GMT  
		Size: 58.2 MB (58216067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
