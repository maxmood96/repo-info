## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:b10feba565a68fc7d2863ff9acc507eb86dfff4a6da5596c5507fc043faf6718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b573b727c0125b679c50be70ed58e1bfe94c98d6dddea27b6c35ece7fea7ab56
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81855751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6133721c378e481baeba1a494929723d504263f7566707d1af6628b052688066`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 08:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 08:59:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 08:59:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50a59d24ef6d2e742c7f4bec2d2cd67d4d3012b8ac371691c1ffcf145fc1bcf`  
		Last Modified: Wed, 02 Feb 2022 09:35:55 GMT  
		Size: 6.6 MB (6641573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e6ad46ecf02ceb26104e64689b6c2e7de98034201f9acf9694587c4e77faf5`  
		Last Modified: Wed, 02 Feb 2022 09:35:55 GMT  
		Size: 3.0 MB (3022225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a086a1ddb3b39165491203d2d198f5f2d23dab656a16a1d360ef2db139e11`  
		Last Modified: Wed, 02 Feb 2022 09:36:11 GMT  
		Size: 45.5 MB (45483887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7d5940e1432cdf7ddd439031fc7d67cbae945f1099297c3722329479e33700c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71281384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8137e5710dcd959656d9dba1da1a22d654dee5f3bc7dfe3568956400f1ac75b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:24:47 GMT
ADD file:f5678be7a8216c2848b16665194b944ad8bdf7696d2925a432437feb730cf587 in / 
# Wed, 02 Feb 2022 02:24:48 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:52:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:52:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 03:54:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3ddd1f986797e6622f6e3810028291b19248347b52709a52a74e6dea7ccee961`  
		Last Modified: Wed, 02 Feb 2022 02:29:12 GMT  
		Size: 22.3 MB (22306998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da1b8bb83e9f084a4b63a32178c403213a14c0e1087853ca2b524d7f4f948eb`  
		Last Modified: Wed, 02 Feb 2022 04:41:23 GMT  
		Size: 5.7 MB (5712132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9d2b667f1e938366a3c39c8de13e8ffe1c11351051d4e27affa22d801f593b`  
		Last Modified: Wed, 02 Feb 2022 04:41:20 GMT  
		Size: 2.6 MB (2584548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1c97954aecd75d04deee982c28e4519c8c8e3bfcd2b2852707224d19068530`  
		Last Modified: Wed, 02 Feb 2022 04:42:03 GMT  
		Size: 40.7 MB (40677706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4da7fc288b71943eeffa18555098b11bb5c03564956043b2d6800bcdee596ea9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75657773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b857ee99c7e082678cf018d807fd45b1ddd2bd5d7781e23394d14389e450fcc6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:53:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:54:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 03:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413d438e227e1c03388d3842a3be7b274f23879daa376a88bbf2c93e51abc689`  
		Last Modified: Wed, 02 Feb 2022 04:33:41 GMT  
		Size: 6.1 MB (6082497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d51076ec9b173d8ad6edeedb81b332a5b8e3c73284d7934a59fb7303080c411`  
		Last Modified: Wed, 02 Feb 2022 04:33:40 GMT  
		Size: 2.6 MB (2570141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa4135db6703ebe16fbb7cfba7d59caec297db7e2b134760e01e603da451b0c`  
		Last Modified: Wed, 02 Feb 2022 04:33:58 GMT  
		Size: 43.3 MB (43275399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ceb3794868a61251592b8600387a0ba1031137b6738df1567b6b1b39879a98c8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84411419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804299197c5d9c14418af66350253c54ad1e472f98d1d46b98be324a9af78af7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 01:39:15 GMT
ADD file:41a670fdf6e067377f3e555206d80e9dddb0d180cd7493802d3989acb2c1b573 in / 
# Wed, 02 Feb 2022 01:39:16 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:01:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:01:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 02:02:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:783703cdc79d2cd178a6be62b27388915bbc0dabf13db414d7ee577514c92adf`  
		Last Modified: Wed, 02 Feb 2022 01:40:03 GMT  
		Size: 27.2 MB (27161586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955bdbde56db8b7cf718ba13de6b2e3354372b33fd274f32b990991a6255b20c`  
		Last Modified: Wed, 02 Feb 2022 02:09:16 GMT  
		Size: 6.9 MB (6930162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bb1b4b1a4c21aa296f0b94f42e206f779faaed569656d1c932690e15e848b4`  
		Last Modified: Wed, 02 Feb 2022 02:09:16 GMT  
		Size: 3.3 MB (3252082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3552c3ecd906992c3be580d7e11f30dc30daabc300794aea7a8db5d39343249`  
		Last Modified: Wed, 02 Feb 2022 02:09:38 GMT  
		Size: 47.1 MB (47067589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b1967e37aaeea468fecb2f0c6b8a5097d7f7c0053697c3462bad516a2378d615
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94935719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8dd9ecc5ce4fb8ceb3947e6ff5e14bc5c74a005110a22d38073b64f53e0d6b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:27:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:29:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 04:32:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7210dcc578c99b7590d84a4243882e58ec2ea51343819c40ff812f74ee175021`  
		Last Modified: Wed, 02 Feb 2022 05:22:07 GMT  
		Size: 7.1 MB (7056530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c820be59b07fc722116e095ddec2185a758c88e620b4c7d730b25add4608201`  
		Last Modified: Wed, 02 Feb 2022 05:22:05 GMT  
		Size: 3.7 MB (3719326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e676423e248f9373dcee868feb9e0c4db75884f0d5ba44252102f60502f087e`  
		Last Modified: Wed, 02 Feb 2022 05:22:44 GMT  
		Size: 53.7 MB (53722178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fcd314b0e6d3ddf76463dbcf44e16e95a11dbfec3e5a86e712d974f8a17de810
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79689204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515e51bde50dda6fadaaeabfb252d3d1136b6c64f79a58ef6898ac2fd3586a2a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:03 GMT
ADD file:3fe2ce9d5d8932ed39dc2c73abff4b15e244fb1e7eb456de0a05df07ede3bf39 in / 
# Wed, 02 Feb 2022 01:42:07 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:07:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 02:07:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf002da3924024b39105dcc613288421b394e45e04d7a3c245ce5dcaf544dd98`  
		Last Modified: Wed, 02 Feb 2022 01:43:50 GMT  
		Size: 25.4 MB (25364307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7508a37076812ed770b47904d4d7e9640f569e6446e5fcf9db1740dbbb9cbf22`  
		Last Modified: Wed, 02 Feb 2022 02:18:32 GMT  
		Size: 6.3 MB (6332517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c9029e49a1cfb9781afa2319f21b8ab1731c998bace902c4aeb9fda33aa153`  
		Last Modified: Wed, 02 Feb 2022 02:18:32 GMT  
		Size: 3.0 MB (2974993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779ff0ea5a07fa5bfec1430d49a0e97296c7d3959cf4042040308a9ddcc22e83`  
		Last Modified: Wed, 02 Feb 2022 02:18:46 GMT  
		Size: 45.0 MB (45017387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
