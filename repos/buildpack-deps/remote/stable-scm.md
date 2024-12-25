## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:e690833d6567b90529badb344deb5a0002ef8ae65f4947560968b400e9cb89ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0f068fa160711293677e37179e0091d4748cd57d8da9cdaca11c55575916829d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136753957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40918210b0470acb4fd3682a5c397ca266b168e2c1ee0a763fa28b9f0513e2f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 24 Dec 2024 23:16:06 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e3cf530c9fe3bf8c558e7f5f6f8a6adb27958153a528f0fc4343e738a0b068c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a362e0d27ae0499b6332637e5887073efd6a58badfdcc7b4a9f16c32ab11ef98`

```dockerfile
```

-	Layers:
	-	`sha256:71cc5b65f206bc784bef080dcb5737f58720be5b8457c1df040f9f8648ee2d26`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 7.8 MB (7752728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:507b41af85883987fe1b3539a98407ed17e9be395b1e1492c295196c2abf3c6f`  
		Last Modified: Tue, 24 Dec 2024 23:16:05 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fa12fde642f33e751373953c1431190e3220371e2fddd8aa5d003bdbc661742c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130561444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1f5e2de97e15ddbf006b13a62791296051ede62f7426af9b00f5edb37d4f84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e29fd2ce2ac1a28218c54bef4d2c9d159f2a524d7e4bb45b04701439ef9a71`  
		Last Modified: Wed, 25 Dec 2024 04:48:58 GMT  
		Size: 62.0 MB (61996736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb8e2398c7248300a97e9aee7662056aa768da8ed4761e61237530566c6c7a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97337b665c7e9e89c7b5fea73d578cf8a80fb40137f94677c3e7eb0ef10d6b20`

```dockerfile
```

-	Layers:
	-	`sha256:2b41460584356ee5b7e84e766760ad79ea1bde8e690e32d46064e1c968b87bca`  
		Last Modified: Wed, 25 Dec 2024 04:48:57 GMT  
		Size: 7.8 MB (7754286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b06e81b9bb005ac036f537faa2d0a5b93090aaf29694e463fd8bc1be5c8d9a9`  
		Last Modified: Wed, 25 Dec 2024 04:48:56 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:390b0a015b9c6bd4a91717ab50b2da649b0e953291c1f6f179ac799ef34e25dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125608396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e6c420c1f7fb64fa485887316c939461f82ec6dbdf0ccd26e9a5970807dbee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4d43724a324f138c88a78ca6df0a39ab6868bf1f121eb974439c5a51284e1ac2`  
		Last Modified: Tue, 03 Dec 2024 01:27:59 GMT  
		Size: 44.2 MB (44200109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff0e53b92c3d0f5c370d71aeac1be1d23e475f1afba41d896ace0ff6eeefc90`  
		Last Modified: Tue, 03 Dec 2024 07:36:14 GMT  
		Size: 21.8 MB (21767161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9625bef464ab08848044651374e04f75d37ada02fe71387c3f9f83d0c9376c59`  
		Last Modified: Tue, 03 Dec 2024 17:15:53 GMT  
		Size: 59.6 MB (59641126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97cad46bffd054d5464b24f3898b89857a83b9327bd544db3f756fe68e8e5eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7772198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a53c50a14cb4d17416ad8c2b9f6ae29f07e4a2b9360068459000d153cbfa28`

```dockerfile
```

-	Layers:
	-	`sha256:98bbc215633288506c1cd937a4043acf7e3f2d79ced4e6d1b78fb36f63f12c90`  
		Last Modified: Tue, 03 Dec 2024 17:15:52 GMT  
		Size: 7.8 MB (7764475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4b268dda7212f4c955489072ec118680aa47218128cabc0b36f57ab7211081a`  
		Last Modified: Tue, 03 Dec 2024 17:15:51 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4b4fd9f631b9294a9c2600d58e03ea6aabe8064c9023517e3c004147a248c706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136079345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294a87bc6560e0bb4acbf480b18930ca99a2863c50d4817579003ad59c8dcf5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac722d9cf93b238dec2480278a2df5f8ccb672c97ec39f191191fd39f6721a8`  
		Last Modified: Tue, 03 Dec 2024 05:38:46 GMT  
		Size: 23.4 MB (23405813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261351ed796deb9fdad22dc734919eaf6726dd79a8dea99327d9e1376ecdcbce`  
		Last Modified: Tue, 03 Dec 2024 11:50:22 GMT  
		Size: 64.3 MB (64347852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:296b38d3b5682f620d8d350576747bedddd836671036ca931158e5fcc0abeba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6feeb02a68d010871c1233be105b538ae59e9b1d4fc972aaf364445fbcb678bd`

```dockerfile
```

-	Layers:
	-	`sha256:52070a7e355cffc4a9d0da8f0dc19e32ab40a808d402a964b8802456ba6e889f`  
		Last Modified: Tue, 03 Dec 2024 11:50:20 GMT  
		Size: 7.8 MB (7769605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:559dec8b2f1952ab63dd3ad11af3f0cab12b2904ee9ac16805ff6743224ac486`  
		Last Modified: Tue, 03 Dec 2024 11:50:19 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:816bf5fbb0c7ff341b5d1058c02c378e91bb1b9c97ba448acb65ec064b4a9c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140394482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ef30957e5bfb3b55fafee6f15d8ef8ce37aded72bcd0b3f995e21f870bb5c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cbd1da18c5356dd3d385be4259ac3747e8813e3aa4d63384ad199ec8994a0923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2564416595e7e49ca43db258d3019760ef6919c66eef1cbecc2b9d5465cde266`

```dockerfile
```

-	Layers:
	-	`sha256:dc333f3c380ffc7b37cf8328922462d456b4de176bd87ea4ccade8fad5f11fd5`  
		Last Modified: Tue, 24 Dec 2024 23:16:07 GMT  
		Size: 7.7 MB (7748805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a80d8775e1ef93448fdc01acb544ab2674962dca0a4c8c1ca03f7f7795f6b63`  
		Last Modified: Tue, 24 Dec 2024 23:16:07 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8915c51839fedacb07adb7002f8c190c948a12fcb503b7696ffc03b6a1b61ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135513047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbc8ce69146cef10089880f0995e0f8904567b5f315696d227d654aea381c65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f7c3140f4f3af477253c748b229283137cca4214e1c3df21109b821f9227620`  
		Last Modified: Tue, 03 Dec 2024 01:27:53 GMT  
		Size: 48.8 MB (48771844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa54d74c5fddb1e648e0a4d95fcc8338f5800ff817646baaa9e6e65596d80c5a`  
		Last Modified: Tue, 03 Dec 2024 15:45:04 GMT  
		Size: 23.5 MB (23458105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279e7254de3fa3935af4b6008753d14fcd8db605c58b83903cf8c5f880324cd`  
		Last Modified: Tue, 03 Dec 2024 23:22:12 GMT  
		Size: 63.3 MB (63283098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c84b11a183c60766b72298df7807d4c7092c9c2f73f1d21017e277fc9ab23ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a1f59aac2c22a1238dc51a66bd9dce102857527b4849511e58dc50dac965a0`

```dockerfile
```

-	Layers:
	-	`sha256:20ab0e5caa843ee96726eb9c38d13c80976c82e15ba6ba6202d3e1ba959cd413`  
		Last Modified: Tue, 03 Dec 2024 23:22:05 GMT  
		Size: 7.5 KB (7496 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f41ac76702c18986d7791e88468e69b4dc78c623d28e1a490e6c0cbbfc6b1082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147664451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514cb07cf8569c7b8531ad437622c499eedef341c3f377fe235d298f7e8ac991`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c84d784fe3c6c2bd95dea1c0d6eeba7c981bfb75bd53f81e83bcaadd87bba6f9`  
		Last Modified: Tue, 03 Dec 2024 01:28:03 GMT  
		Size: 52.3 MB (52328222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f0cfea13db30ebc69124696ada25182d1141398cd301a47a2cbf3c10d7fa9b`  
		Last Modified: Tue, 03 Dec 2024 04:36:57 GMT  
		Size: 25.5 MB (25523892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac73bc765d61ec6125ff5203c6c3d44543e6c3030684bfed0cb8f169640ae757`  
		Last Modified: Tue, 03 Dec 2024 09:41:44 GMT  
		Size: 69.8 MB (69812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a89a02d7b0a3fc01937338322a3adbfec4f8acf6ca3ccbf611a6bfea596fec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a47c62b0745a03c2b02e5a3f2df0ebe6f985dc10f4132e1e9b9ea44ffc350`

```dockerfile
```

-	Layers:
	-	`sha256:4b033dd73e35183deec51e3e2b0975d4838f1627c9589d8d0a263fdb61430e94`  
		Last Modified: Tue, 03 Dec 2024 09:41:42 GMT  
		Size: 7.8 MB (7770901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1815558343ccce9363e7d65977e06bb87d6b20878e7dfbcffc07133ed7dee487`  
		Last Modified: Tue, 03 Dec 2024 09:41:41 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d11eb20b2cb62ef240e664bd435e87591cd97ef7c119a1c9c6540b0efad1d43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134488352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0ea6c85f11c5639e4215760c9c7ab63b2d68c7dced18355671f82e71e42880`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:533af391433b185f75b5fbedbf1a23f9114ea5795edee6e36166d6f7157eaddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d399031b4f4c884a462114d13b01f419f5d7087ed82c0ed69d516c1d8c332bd`

```dockerfile
```

-	Layers:
	-	`sha256:942a39e169ce5152360dc856728687ca7cb4d7fce9ff1284e4beb95edda34024`  
		Last Modified: Wed, 25 Dec 2024 03:29:05 GMT  
		Size: 7.8 MB (7751933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6172b9b6aa5db8566911ee909486fe3b4d4067ec0a5c1b409cd4350397b4a9`  
		Last Modified: Wed, 25 Dec 2024 03:29:05 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.in-toto+json
