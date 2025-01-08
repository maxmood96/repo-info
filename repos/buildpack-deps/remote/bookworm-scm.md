## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:875c2b6ab66031533c3532954046ace8b8c52755f8f3696e94020aee34721a66
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

### `buildpack-deps:bookworm-scm` - linux; amd64

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
		Last Modified: Wed, 08 Jan 2025 03:47:00 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 24 Dec 2024 23:16:06 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:98095e8b5d2f4dca3c50e681ce344fa3135fd30c701685dcfa883d81e322ad32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125606171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e8575d3c1f9bc1e33c35b81411a60f424ac02f05bd3687961c3d1759619095`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6cc3f398148ba6c47b31ca021b4ca1cab97e08caaec9726b1d3f81e4f7d95f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe08cc8869d9be28e277619d09cfaa9af4f599e262ae90ac1cb0131e8f45738`

```dockerfile
```

-	Layers:
	-	`sha256:fe666d48440ffce9fdaa7d58c623c4fd4f2cfcbae6ab76a3e1686d1340e49d49`  
		Last Modified: Wed, 25 Dec 2024 13:00:54 GMT  
		Size: 7.8 MB (7754013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72bd160636ad220ab2e9d9e2e37f5c0e29e4add5b551dd4104ae69159b217ea7`  
		Last Modified: Wed, 25 Dec 2024 13:00:54 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c2632ad6c1c90478a2b81e4dc20b3cfe89afe56b81f69d9b78741e354e0e522f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136078704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e1021537b35dfc28ebe4fdf49198c5fb0f07aeb49b7133a8c9ec31e458fe1e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be39e84784ce31ac7484757b7cc69e1ebc4e1ae905d60789bd2b6076100e32d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c98498ccf5c2730766e368dd9fe7474d9a565b5e1913a59076d878d071e99a5`

```dockerfile
```

-	Layers:
	-	`sha256:8e2370faeb7e1aaf57fce2b10f69b06dece93441215a4dd960604be27b9657ac`  
		Last Modified: Wed, 25 Dec 2024 08:11:49 GMT  
		Size: 7.8 MB (7759133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6647341dfa43255571377a7b311aaa5b87cc9300d3c0f53053065745b474c361`  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13ca5071ec13ff460953798daad666106c46ca2b2eb3dc82c41682d9220b121f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135512750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c330b4cb04586912db66a6e8c539ea43706561671df5d25bd4e9fd1b2b540a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6cdb193561d8db1e02ebdca6d4fd5bba968cf0d7acefa02489879d47cc42af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a2fa930db5487c1c9ba556acfcb71b70adaa00d244a4c6a4b1e2d165897e59`

```dockerfile
```

-	Layers:
	-	`sha256:12f1d48387ad7f8a6179c3861c94ffeba6a882d0d84c44a1bd6f3bde5a79f2e4`  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b1a91d6ec665e4042c64fec10ad5b46d2bc7985760f26d9dfb991f540c0a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147663993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4666cd492c6b6a9a1133dd7af1deb44a6d85416c321c809da3871cedc139cd5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b41cdc05f2fb617f664e6d5882b807537d969779bd93c4ef287503be5ae5cc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7863ccf15fffaba3ac88d09d0688d4d86023ac09db7befe5bb38afcc68fc21`

```dockerfile
```

-	Layers:
	-	`sha256:70996268e7bd5b6a00da22119cc9fb810a57b94358226b6d2e05d6abe464edeb`  
		Last Modified: Wed, 25 Dec 2024 13:15:14 GMT  
		Size: 7.8 MB (7760435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eda429325959d8fc1a00cca7b163a3d4718f4a51a3721994eda88196cc43b500`  
		Last Modified: Wed, 25 Dec 2024 13:15:13 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

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

### `buildpack-deps:bookworm-scm` - unknown; unknown

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
