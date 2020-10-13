## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:3a9d7ea963b572f0462ec40d7e451b6a077d0492c5eda7969beade7fe351ec46
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:557e408b13e9e176ea6899ebf4cac90b543cb268bb61072c95fb627ff6487510
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71077922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a011dd3d5bdc20bc84350adb940dbd9308198125815a345e88f05e8242f3b39`
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

### `buildpack-deps:bullseye-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9cffad62f2a3e6d69211e8f8f2cfc27f21ab5ffbc24604840960e1d9ff5ee018
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68262070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e756594c06ab0e4499b0face1a5fb7cf87a7911eed913a0aa9e88f2997fe4d7e`
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

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:977efd5e0ec8bf1cde16d93ca9cedb6f637f3a49b8bd11576c3990a756e16928
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65379632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097fe12498826376d9f165523da7e7e61157ab9f4b0bd1ed8e0b359fd94c941`
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

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0bbda45cf1eea59c664061d14d5af72a0e34929fd2833710a6afc6fa96554d57
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69863070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4970961ae9c1844c0b81e5a737543b10f138848bb6d027f11638823a568c69d8`
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

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:06457e99fd0f7835727787f3a0cf188359915be97d836369707240235b63482c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72688895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9811489ec68750dcfd959c2a598e6ddafa6957ed834e3ccb8101fec1d79136`
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

### `buildpack-deps:bullseye-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c06d4651dde40c13629f4c02c3df2b32e63037030c685b0f75a641f2285e7fd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69315429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729bc95ce3f69ecd010276403ded62e7ad6b24dc775b8f3ed89f08144ccedc22`
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

### `buildpack-deps:bullseye-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c5cf3189687056927cbe4595c765bf7d07921ebc09c49aff670075b462e10ceb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76185814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615d79004b8e9de67dc274cce692bed4e750940b5383b59f639bbc953bcdbd59`
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

### `buildpack-deps:bullseye-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3deed9c0932d2541051c0493e89221a76052199169c4119d21ace541a7b0a74e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69164816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bad1744099e7aa469e747eaaab8cd7c0ef508fdc5e0c12d9781eeb778dd4a9`
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
