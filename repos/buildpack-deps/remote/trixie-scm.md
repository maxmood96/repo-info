## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:afce682b0dfdddd28f22ec909cc95d35b20900acdf75f7bd20ca6afc213d64c8
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
$ docker pull buildpack-deps@sha256:4c42ecb88b3ec59ba808db443ec01f74f1564bfaa4bd090b6a3b203c3f5a5230
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137632404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6115d13d01ce8f5aeec86478625284c0f4440c8d246b6766e25e4d057ec88d30`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:26:59 GMT
ADD file:90c4ad8b280b16131f305780a1f2721616642bd4d5b4a26256c760cd8ae98f27 in / 
# Tue, 02 Jul 2024 01:27:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ca828e2fa86974a7bad5159e89a3c4f34921c624322a7fa71026f2a3933ab620`  
		Last Modified: Tue, 02 Jul 2024 01:31:45 GMT  
		Size: 52.5 MB (52458214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687f3d296dd0e92cd772395160b84eeaffb55fa2ffce846bc61595e5e164a5e3`  
		Last Modified: Tue, 02 Jul 2024 02:03:19 GMT  
		Size: 19.0 MB (19021831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb04f2f4343d6b362ed3e5d55a9e7736eacbe6aaa43d185b2b3e8af75e33528`  
		Last Modified: Tue, 02 Jul 2024 02:03:35 GMT  
		Size: 66.2 MB (66152359 bytes)  
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
$ docker pull buildpack-deps@sha256:879cf292ca55f2dac3f60d1ae87c900d99a880b17f984e3cea0f803942fb91a8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137810832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a97ec39812e39e1c687955dc4e4357d504033c6bc4b60b658da73fc4fb46db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:56 GMT
ADD file:231a92f6a31914243d9c6358dbd08017ac703b3270465f6d231f3d178f7e783f in / 
# Tue, 02 Jul 2024 00:40:57 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 03:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5bed35cfcfc0ac7f84b7a2c93f738e00119f31c9a82999f6fc0e8493ceff3010`  
		Last Modified: Tue, 02 Jul 2024 00:45:19 GMT  
		Size: 52.7 MB (52693320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9751e3702568b536545773c8a831b25db2876eb1b4d0823a3cfa663395793f96`  
		Last Modified: Tue, 02 Jul 2024 04:04:20 GMT  
		Size: 18.8 MB (18763001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b302bfdc7cbaed0a8ebc1a14e878b03d086764643d49d881cf50b66a5a851fc0`  
		Last Modified: Tue, 02 Jul 2024 04:04:35 GMT  
		Size: 66.4 MB (66354511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:14d77bec735b0db701c7b9e0db46afd5a4ce074230807fcd268fa53372e61370
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141269892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56bedaaf854248b902da5dcd667e0b11fbfe42d0d418c0b22d4336e795486f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:40:52 GMT
ADD file:2c79a29515e7dc495de2293d9b08d4b2ecee86e61c2d0adf1658f7b939d57c1c in / 
# Tue, 02 Jul 2024 00:40:53 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 02 Jul 2024 01:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:86c6de18cd170a5e610d31625f09596aeecc408fed7171fc8922ae0196331108`  
		Last Modified: Tue, 02 Jul 2024 00:46:09 GMT  
		Size: 53.3 MB (53333176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ed3a89daa70bb513739a2ade83fc5f0a43a784f37749e2584d3c335224ae6e7`  
		Last Modified: Tue, 02 Jul 2024 01:17:53 GMT  
		Size: 20.0 MB (20029610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3099c8c1942a3e6f5ac57d77a04b1e727414a9f58f935b9f5458db57884654a`  
		Last Modified: Tue, 02 Jul 2024 01:18:14 GMT  
		Size: 67.9 MB (67907106 bytes)  
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
