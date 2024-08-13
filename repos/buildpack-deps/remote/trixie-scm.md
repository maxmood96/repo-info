## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:b0030545b3c45615fb6677781f05366386d3af32d24be2ab80f866b9e4c708ec
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
$ docker pull buildpack-deps@sha256:1bd5816c21dfd482696112b2f7b1cfe409be46324c34324afd6cd78f8c1e1394
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138640409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b6eb1e8ecebb5addafad2276bb23b14ac9333c39c1fcd6650fec6fcbb3c8ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:11 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
# Tue, 13 Aug 2024 00:22:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:47:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000d3eb244249a76a53e7b3f03c8e999bbac83be7058bc1aa1fe0eebb494baf`  
		Last Modified: Tue, 13 Aug 2024 00:52:48 GMT  
		Size: 20.4 MB (20428585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75784ed4e534b2a8c61e811f3ae902dd7265dcbdd4784c9d0a1e99630fb6e3c8`  
		Last Modified: Tue, 13 Aug 2024 00:53:05 GMT  
		Size: 65.4 MB (65370635 bytes)  
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
$ docker pull buildpack-deps@sha256:79c16aa605ab12c6f1800a914e3ce2aa54e77910c10515151846a8f3fb2a0e60
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138736298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d1ff2e0eb7d674666f5c0ccca985c41be0a9127be3c82797b8c049fe5c350c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:41:11 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
# Tue, 13 Aug 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:07:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc2390559926818fa461fbc23891f666f695df10963c68e66dbcd7d2a33119`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 20.2 MB (20169643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f885d3fa750607fbd2f71e34070f91d1e6ad0cf13800756907e5eeb2a71a2eec`  
		Last Modified: Tue, 13 Aug 2024 01:12:19 GMT  
		Size: 65.4 MB (65414213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:acfc21a933b61a511a40057c2cd17da39e0b250e421dcc7aa725078e2e542d2e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142347395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26dfc06fb060f82a67d251678866e3eff820033e7c7b1d4ef017858d28fb594`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
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
