## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:dca89fc87671a1560985b886bcc7f60567226b411706d662a2bcf74e3422f0aa
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:079424468f0eb509ef049deee98b5cef0b9ebdcea733b003cd7395bde02700b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137527693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f4fd31e466aae2585a1c45186ec7693e0f6c4d2da23cf32fd7488f304f3715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 05:26:17 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
# Tue, 23 Jul 2024 05:26:17 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 06:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 06:11:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d0f848dd15a13c8823fd99e5306acaecabecb24a04e2148715831928b219f3`  
		Last Modified: Tue, 23 Jul 2024 06:16:13 GMT  
		Size: 19.3 MB (19295644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb2782ec0c8f6a51d6d35106ecb2c6dc20884f4733b1236af9de7260944277`  
		Last Modified: Tue, 23 Jul 2024 06:16:29 GMT  
		Size: 65.4 MB (65410843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d0191a2b3eb5bbc58aeab05f297127fa46c0883320291916434150c83e955d23
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138741834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23a8db2f6fadafad6db8d02d01b62dc2151f0380773c96f655321756d8446a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3995f67f100684b8a4349bea104130c9a88c087b6156a290542809abaf92fee`  
		Last Modified: Tue, 23 Jul 2024 03:56:39 GMT  
		Size: 65.5 MB (65524112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:63f39701455c7b52b5afc3a4dbe8b79d58a527e2f7b96be64eb0eefb2c93942a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132659149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbccdac0e820af648947deaeceb9fc4085258cd537072d2a68ed494ce72573eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90386b6142530b1ede165d6dd3a0cd162bcd3ddd68e43f48c8f76f8ada03618`  
		Last Modified: Tue, 23 Jul 2024 03:51:24 GMT  
		Size: 62.9 MB (62860451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a34d3ccf7480596852a7a82bd609a5133b84f03a589075cf4467bdc6edcf5a2b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137486678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f90529babea4756000108a806d6b6ca8949541c4897fdb847ef2ed483be0945`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 04:19:11 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
# Tue, 23 Jul 2024 04:19:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 08:08:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 08:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1a0ede68aa727c607d43ae4be3b7578d31d87709092b02d36e3b7e4a0fdbbb`  
		Last Modified: Tue, 23 Jul 2024 08:12:40 GMT  
		Size: 19.0 MB (19033702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e785485c52ea269ecbc49c8c92334b4b4c5c2197c256111f09c3158120f7939`  
		Last Modified: Tue, 23 Jul 2024 08:12:54 GMT  
		Size: 65.4 MB (65426655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d923d1db8297e4b85a34a97bc7d75b03fe29b101ddb7138fecd879a6ebb4a9b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141205493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6af04ff871c1be2747f0f54793aed4b11296e5872e9eecd576d860f486361a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:56:12 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
# Tue, 23 Jul 2024 03:56:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:46:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 04:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a03acf0ea95beaeb6fc7c7cfac20f5747058cc54deb10ec36249d791cf845b7`  
		Last Modified: Tue, 23 Jul 2024 04:52:34 GMT  
		Size: 20.4 MB (20354365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908527b139d9269245a4259635b1caf76393575aba5a1f4650d84a199883a1b1`  
		Last Modified: Tue, 23 Jul 2024 04:52:56 GMT  
		Size: 67.2 MB (67169878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6228088f3891510ab445efe6f056342d9a805dc01b753b8872d499908cf34828
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135629170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75ea010fd80caa8f1bb20778ef586a1688bfe15b745ebc58f17bbcb5ed3702c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee36f9299929b13c64e8d1dcbbecffbc23ec614ec5279d3468b3cc790fe0439`  
		Last Modified: Tue, 23 Jul 2024 02:09:30 GMT  
		Size: 64.2 MB (64222016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b9c22c11ce24f944e5ab6db7b108c9dc0d66620bc8a8b16ac2b1992ae0c11f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148700726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a6cd597306f829d3ed16e8c3b4fd9ca4cd5a55945dec1e4c5840820b52036c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432aca4b63ee1a3a6c2c0c85f637c9ff06323c852e1a5363d3eaf9b36ec6bafd`  
		Last Modified: Tue, 23 Jul 2024 02:45:39 GMT  
		Size: 70.7 MB (70683207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c6329d78700cf3032add31025f8c1fc5a855f016d94dab2742cf438bc93f333e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139376987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb065e2e54ebbee952f3f504e0aec0e591fb660cb8dd576307932ab4d75b050`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13abee5c4577fc2e5e5ccd45eb4abcc067e815317edd4eb7fb89c6b9ff137b4`  
		Last Modified: Tue, 23 Jul 2024 03:17:12 GMT  
		Size: 66.5 MB (66483586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
