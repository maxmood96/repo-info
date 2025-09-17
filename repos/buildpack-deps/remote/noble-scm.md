## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:892ea8c7f8e59e209b060faf16fbd54ccf78a05d8a17c4a467fe40cb7e6d68ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5686fc4cc1c02d333a242822bd0f13fa0d9aed4b355732c00f5da9e655f088df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88682000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb24b45ccb4a7a4ca8f19d8397ca39f62b1bac2da63ec127dbf0f01d16703435`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f15f492705b1de8136aa0d2c2d9eb39c00ca05d077cb49934724c4bc48ecf10`  
		Last Modified: Mon, 15 Sep 2025 22:12:09 GMT  
		Size: 13.6 MB (13624812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1313c778bf6a9ff7cc448fb8f14ad32be55019475933c62e3603fc4f25f29f66`  
		Last Modified: Mon, 15 Sep 2025 23:13:58 GMT  
		Size: 45.3 MB (45333738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed95f60f903c8c98199a8d65edd3ac2013e49dace6756374eb892092507c98c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14edc94e400cabefde2b2f6f4ea99d09215bcd3ff4b31d4cbc9c221c64be122b`

```dockerfile
```

-	Layers:
	-	`sha256:221dad3d67aa7924a11bf45ec982ae805d94c829644bce9f0debeb55a8ca4326`  
		Last Modified: Tue, 16 Sep 2025 01:19:54 GMT  
		Size: 5.3 MB (5274574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63cfbbdd2545528f6eeea0bdcaf80a9f3079654b9a7ab28780d59339459c2504`  
		Last Modified: Tue, 16 Sep 2025 01:19:56 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f1a5052212691e2205213fe183499dbf7ad473ce506733cd28af2cb56b4f7a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88501569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7fb33e0f19bc6769ab8865bf6e820e142e55a8bb814aa2be2bd4b0447e92a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:724937f3170b06318ea1d68d111a29f384243a4dcad8729e0deab590d6d690bc in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d7ffb5187e159334b70dbe49cbca848457358d2d2b56fe7072a42dbd9ac9c7cf`  
		Last Modified: Wed, 10 Sep 2025 09:09:41 GMT  
		Size: 26.9 MB (26852474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bb7afdd6f69b5972a86f2f83e308ff30d49b2ee36b8a9c2108e1ad3afc6ae8`  
		Last Modified: Mon, 15 Sep 2025 22:09:53 GMT  
		Size: 12.8 MB (12783833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4b329d0b7d213a4be22f22f475757819ae3aaf1b0d685afb7fa67f4be2c1c0`  
		Last Modified: Mon, 15 Sep 2025 23:14:00 GMT  
		Size: 48.9 MB (48865262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:21d076eef88468616ddf09fb4e986b6639315e0d5f14425185cf4590a252ed46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507e47aa0722f8029a615025eac62798e7c04f8049671d265247eb862a9345ce`

```dockerfile
```

-	Layers:
	-	`sha256:7dbe93ea6b167ec27bfff0e5ffbc8509bcb8d9c77e97eaaeb12df905361fcf01`  
		Last Modified: Tue, 16 Sep 2025 01:20:01 GMT  
		Size: 5.3 MB (5275872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50521c0ef4034111bfc7fda5a14b233c51980732a5ed6beb9b8d4e6b51ce1864`  
		Last Modified: Tue, 16 Sep 2025 01:20:02 GMT  
		Size: 7.4 KB (7368 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4b859c36758e921772518b20bfada5bd3f099e138ece81f8506ce88dcb63c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87629908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32eb70b3db85083f0c62aa288147b7059a449b6b391ebc29a9dba1696f558a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1322a08d432101eaa67d86cf47e2ec84c226aeb9c10d0f3c36d5ae39592c62`  
		Last Modified: Mon, 15 Sep 2025 22:11:37 GMT  
		Size: 13.5 MB (13460309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8945f046ac130c626cefeadeae71f3c749117955f05d96a7f48e52f75a0165`  
		Last Modified: Tue, 16 Sep 2025 00:12:36 GMT  
		Size: 45.3 MB (45308282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06af6a61e97f3905a4659e8219badd3aefa88c84920e104910912278bba0cfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d7b56d7206794b77c546d7b8047bea675af364ddc68d4802971716638feb1b`

```dockerfile
```

-	Layers:
	-	`sha256:5c78a86e8ec804c8c8330d100edbbe4809fb23a3c3651ccc68a165cf8b52e2a4`  
		Last Modified: Tue, 16 Sep 2025 01:20:07 GMT  
		Size: 5.3 MB (5281766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994b74a0cd3aeccfeaa9f8b0399c0547c69a0f4a86050b50bbdf5d6fc0eae192`  
		Last Modified: Tue, 16 Sep 2025 01:20:08 GMT  
		Size: 7.4 KB (7384 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c3d40227c4762687d54a411d947c3ab6b2927f6dfdbcfd292f8574f09777ede6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100595748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2637be7bd75265f15bf3720dbfb53ee8d6277765bec952d7ed5ea6a2b93e25a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c837ddd2ff9840a8084e110a0603180382a7fcc929a7f65af65d4470031ecf`  
		Last Modified: Mon, 15 Sep 2025 22:10:54 GMT  
		Size: 16.0 MB (15953067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d665a438d7ff06d9f0fb03e9b189432d711170c64f06655f88385714c2b57a`  
		Last Modified: Mon, 15 Sep 2025 23:52:56 GMT  
		Size: 50.3 MB (50339554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d965eb64adcbb5c79d06e0f1f5cf1938612819c9e3e2f5b6f3490d10110b1a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c103d631ff5f23f326bbe0e3adde9b69d5f1cf2d1fbb9dd036a5f85674379e3`

```dockerfile
```

-	Layers:
	-	`sha256:62b1caf4ea3091469114cbb64b50bc82595c1f1f466d4c86411d627bcae990be`  
		Last Modified: Tue, 16 Sep 2025 01:20:14 GMT  
		Size: 5.3 MB (5282428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937eff88f4caf584271c01d4deb12ab07508d4f0510ecd12cc113c5bee2c060b`  
		Last Modified: Tue, 16 Sep 2025 01:20:15 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cd2af051fa2f27ce1fe4ebe86b4edf16f36bae36e6aeb1c11b430aaaff21eb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99157059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae51d49d60c7a8e0f79c68df250990133598d346e8dbfe3b4abc28e3d589d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:58fbc6777cd47d1e58396e2c0f70255ae3bd63d0ac2ea2138ed6e5e91fdd70b1 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fc46b4719a7bc0e446bd2b472a339bdca3990f164daf9dde3e710206f93383d0`  
		Last Modified: Tue, 16 Sep 2025 19:54:09 GMT  
		Size: 31.0 MB (30950703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef5352f27f8eaa4912970c5e40c708ff8676d4d3b32b568f91c0697ef0d269`  
		Last Modified: Wed, 17 Sep 2025 10:13:49 GMT  
		Size: 14.3 MB (14330275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c60c4f66e23d52d21fc7f3dc5c91cd17568df06d10b745951ee901f9d3229d`  
		Last Modified: Wed, 17 Sep 2025 13:34:45 GMT  
		Size: 53.9 MB (53876081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ccc77511e60d7ee408ad1522c3ab368f9af1979d4fada6e45c4c9fe707e22077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5187806a83feeff598abe92f20cde5320c30ac60308265f34cbde71e06a51c72`

```dockerfile
```

-	Layers:
	-	`sha256:b93099144546662ddece1659e22623054876482b71477d893edef3e0944fa748`  
		Last Modified: Wed, 17 Sep 2025 16:19:40 GMT  
		Size: 5.3 MB (5264970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee40da18d1723f70b3e0b753ba8e0e783ccbe22031ae7dee77c11b0d38d2adb`  
		Last Modified: Wed, 17 Sep 2025 16:19:41 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:78d4246a9703aa4be9d1157991fac370d356356d639af2382e06496b3a6772bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91625056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f199693dc02ad21aba15ed94847d8b1a203f0a98dda4ae09a4375741b0252236`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:c24f61277b8ba0fc6a9f5e3c821b272fa1878e300fa010e5e8c6bb6b789470a0 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1d6a499251c4e5e59ef209845254eb72c5efde9542271f270cf1a08fa823dfda`  
		Last Modified: Wed, 10 Sep 2025 16:24:53 GMT  
		Size: 29.9 MB (29906591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5addaa29204c79a9906cd7ee74dee50da001c444c82184247c8539ea88b9594`  
		Last Modified: Tue, 16 Sep 2025 04:19:26 GMT  
		Size: 14.9 MB (14938285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf900e5d5f06d96144d0fdbb00fcbb48744678cfe7c416b3dc4001f8491d0`  
		Last Modified: Tue, 16 Sep 2025 04:19:28 GMT  
		Size: 46.8 MB (46780180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b159766b8ed1f7a2b8f0d9dda0134bb76ba9512a828edcaea42d087cf36cfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5284211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eba6425894a57850e576333b520388d2bc49bd35484721c362ef9e232260a7`

```dockerfile
```

-	Layers:
	-	`sha256:508796d75951558dd8642303094655b3c38ef6358380999da66fc995c2d16bca`  
		Last Modified: Tue, 16 Sep 2025 01:20:25 GMT  
		Size: 5.3 MB (5276906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf91f398fb07946865f3ba8d159aa8331980be20dc342a085a3e985e00a69228`  
		Last Modified: Tue, 16 Sep 2025 01:20:26 GMT  
		Size: 7.3 KB (7305 bytes)  
		MIME: application/vnd.in-toto+json
