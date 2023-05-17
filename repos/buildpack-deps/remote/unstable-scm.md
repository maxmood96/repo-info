## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:b53de7d7789217c25bcbc01ae0168f5db9488c344a9f49d19bee48b8c0e0eef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7aebc9182763ef511d6bc922ffb55f553b3a91dc811e818d6b81fddfb53925a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139163095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d802647ec07569e8933cae43dfa5671e2d62a40d01c78d7934fdfd5ddbfaf5d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:42 GMT
ADD file:6261ecb921e04d2b3f6fd44e5dcb5683154bc0beee4f26913c2be9395a060489 in / 
# Tue, 02 May 2023 23:47:43 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:22:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:23:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae396e350f30e1defad1bfa67a84b97389d42cf3442551e39a0e2bab6b53a50c`  
		Last Modified: Tue, 02 May 2023 23:51:56 GMT  
		Size: 49.3 MB (49299270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5394399a653714edce416717c938e83945318e2f603216d0c47c5ede1fbf955`  
		Last Modified: Wed, 17 May 2023 00:40:35 GMT  
		Size: 25.3 MB (25348503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23532021f28c576117b0fe9afd17d131baf6f97947ae4c8cc69f35313c0d6a09`  
		Last Modified: Wed, 17 May 2023 00:40:51 GMT  
		Size: 64.5 MB (64515322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ccc0e4f6692a9c88a3959463d318035e6f460aa5d17095b1609f4c0e8e9f46cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133317467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002f5bc9dccb1a887d9b0e8ad6392c81540bc5cc6686525e8ac72079e1cad603`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:49:00 GMT
ADD file:2228a07c6ec82db1e0719684d77cecf448c3be947c2b1b48347ba5de9e5b57f8 in / 
# Tue, 02 May 2023 22:49:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:52:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90d5a5fdc15637fce928afc279fecd9adb82fe3c476f174458fc6bdd7fb4b57e`  
		Last Modified: Tue, 02 May 2023 22:51:47 GMT  
		Size: 47.2 MB (47167062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3aabdf1b5f4fe267ba781854e71260b46210e5625adf002fe5ff5e24865561`  
		Last Modified: Tue, 16 May 2023 23:55:08 GMT  
		Size: 24.0 MB (24009742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5c70d2aaf967c21be93aee1715376be9d7e6080ca3b20e1fce409cbb398017`  
		Last Modified: Tue, 16 May 2023 23:55:27 GMT  
		Size: 62.1 MB (62140663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ab0243a521c1c7f1594786e9740b3ea4af0957543c76a2154250e16896e0138d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127981149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93cb3edb35101b92d8d4bb39ff8037c1209fcdfba20441be54d9a44ded27bb7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:42 GMT
ADD file:17739fc730ad8febc64f53eec61cbf10f8d2c5184cfda5466e89ab423a88f9d6 in / 
# Tue, 02 May 2023 23:48:42 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b827c534260a55126ac3b18c14ea9160a3a3a03448b5c2b4462f9f3f4cf0ab`  
		Last Modified: Tue, 02 May 2023 23:53:05 GMT  
		Size: 45.0 MB (44988077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858686fb647755cfaf9d97846212a8b1056f291d77f962bb8bf7be5d16a5ff60`  
		Last Modified: Wed, 17 May 2023 00:24:35 GMT  
		Size: 23.2 MB (23219225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fdb017446b11706119bca2906a6b8fa79ccf636d08457981e54be450413bf`  
		Last Modified: Wed, 17 May 2023 00:24:55 GMT  
		Size: 59.8 MB (59773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b4092b6c55943924df5c41d7c192457b2383f9bf1df7a88784b1d139f6498fd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138739471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8543a16b79610649af1d8aa2b6403f15f545d458f63ae31d0af59feb3360caee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:23:28 GMT
ADD file:cb107aa90220a9fc72fe1e3aa26878752691d6e9eb04696738920b5834c6d9e2 in / 
# Wed, 03 May 2023 00:23:29 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:42:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:77a3c1a83d83f65ef8fd579d19879f09a4018e384f42cfa55f82d426f32ff840`  
		Last Modified: Wed, 03 May 2023 00:27:15 GMT  
		Size: 49.3 MB (49345262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f52781deab323ab07663419dcbd3af52651bfaf9895ae88fa6160c7a78b5c7c0`  
		Last Modified: Tue, 16 May 2023 23:57:13 GMT  
		Size: 24.9 MB (24896432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c9f3ed5b90a971a7d8c99f95aa99252f2fcd3a7fadddd62e9c1b012f89b3b6`  
		Last Modified: Tue, 16 May 2023 23:57:29 GMT  
		Size: 64.5 MB (64497777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:467b5a43e4ac6ff9c76c3bdc74adbe5064159cbb5821488e0d0b45e18fd14b9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142854740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418a41a125e0d5997240bd579f6ec8daeeed23a126fa49e09aa20f24a94fd32a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:01:59 GMT
ADD file:4abf127b0d4037b2d94457a8ef168165ed6946fec0635fdaa845ed4ee8f74681 in / 
# Wed, 03 May 2023 00:02:00 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:44:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:125509149936f5c9fc010cb99811f5cb23108af74e034fcf0903d3f2cc08d893`  
		Last Modified: Wed, 03 May 2023 00:06:56 GMT  
		Size: 50.3 MB (50321774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4a96d98aebd4e76698b47d9e1a7e5c5b576c22314cb670e159aa6548a7e385`  
		Last Modified: Tue, 16 May 2023 23:47:11 GMT  
		Size: 26.2 MB (26192711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce172b2251db3844f41f864eda3f64f8d4c0141d0557af09d03c8a0725ebd47`  
		Last Modified: Tue, 16 May 2023 23:47:32 GMT  
		Size: 66.3 MB (66340255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:bd6b80bbc9740cd6610054b1e33f8cf3c689fee2f7aaa7180e1ca95ef4ad4973
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136930349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe12618afaf4a0ba94828ecb52cbeba92cf0b7b7ddb9aff772424cd6048e9126`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:50:24 GMT
ADD file:3eff171361a4eb801d0fe38f81ca109a46285fd25a23f84aa338364d49c0591d in / 
# Tue, 02 May 2023 23:50:30 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:54:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:56:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ad09064fad2597f74f486eca3ca74c1f51072bf61093439cd70c0d5735689aa`  
		Last Modified: Tue, 02 May 2023 23:58:51 GMT  
		Size: 49.3 MB (49301428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c533f052cb6f9d390977495e5045e622d198eff3064421eab4a0476cb44dc6`  
		Last Modified: Wed, 17 May 2023 00:06:07 GMT  
		Size: 24.2 MB (24206980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b8dcf757e238ec443e11e6688d2932c5b7fcdd1a6033170446c15b90305e01`  
		Last Modified: Wed, 17 May 2023 00:06:56 GMT  
		Size: 63.4 MB (63421941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:67426e75c2842c61693d298f97015ce79dcdb9411895fafa4621cd8ddad0749f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150313773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23eb836f20cd85f69d407058d0ef581c2c4972371d9555ab7dfdb4abfb42c1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:32:10 GMT
ADD file:c9bb656a5f751ff13849f6ca569f657cfc8dbe757b270dfa6e9fe2181e699494 in / 
# Wed, 03 May 2023 00:32:13 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:21:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:22:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71d18ac463268aeb15f1776de10a379de577489dfb1022fc92adf6187695aeeb`  
		Last Modified: Wed, 03 May 2023 00:37:22 GMT  
		Size: 53.3 MB (53307234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7506675c561fa99ba9e7606e22d38016062b4e3ff52b88e0ce9cefa5899e7d5`  
		Last Modified: Wed, 17 May 2023 00:49:28 GMT  
		Size: 27.0 MB (27049441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b369e6e1d1b485a054117c340502c5479238b3ec97ae5f82a828bc5e2befd09`  
		Last Modified: Wed, 17 May 2023 00:49:56 GMT  
		Size: 70.0 MB (69957098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3542223d714626afcf4e085f34de0360e8465a64d0913f7eae3b16c71dd899de
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (129003875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a60d54a46af640013222658abe762a71e2b568ad4da41e5661df37801c12016`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:29:17 GMT
ADD file:4e365b380d9cfb77573624c399d3376d19fa5c7028c44b681071b426fb1c6db0 in / 
# Tue, 02 May 2023 23:29:19 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:10:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:12:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29b183cb384ba20db9a991d4213be72a43fcec3d5fc87f259bd5719d35027d1b`  
		Last Modified: Tue, 02 May 2023 23:32:35 GMT  
		Size: 45.5 MB (45510102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4bc7d7e7f388c0265540f089e7c67a7aa86c6f5bfac0e5c45d897f3d99df03`  
		Last Modified: Wed, 17 May 2023 00:21:16 GMT  
		Size: 23.5 MB (23533638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b83e6666e154117a476dc174b5fa1480d093e8947f87c61a0738916e1edb89`  
		Last Modified: Wed, 17 May 2023 00:22:38 GMT  
		Size: 60.0 MB (59960135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e046ec9cded061a5b59e552f8a7d71ea7d25430a1dd8d795594c1daa79d017e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136634108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35394c98b44287f15a02362a5d740ef8003f15408dc1def9f0ffe8dd492eeba3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 03:42:08 GMT
ADD file:f714218b704bfe42a591f19c2fc0360b178732edfcd6b12687ea572c74b84171 in / 
# Wed, 03 May 2023 03:42:11 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:43:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:43:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cad3c2eaf2133414000bf2d83ce6816eb4031d5b81288493af8102df33f2e4c`  
		Last Modified: Wed, 03 May 2023 03:45:13 GMT  
		Size: 47.7 MB (47675884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bab5e47182cd759c84de89b674a6e02b13aef910e9d07d034d7b802c36c2c9`  
		Last Modified: Tue, 16 May 2023 23:55:48 GMT  
		Size: 25.4 MB (25352347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79c5309e9a86c28868504dbce3cd42aab010a6909a28eee8682f5a41cf684d5`  
		Last Modified: Tue, 16 May 2023 23:56:03 GMT  
		Size: 63.6 MB (63605877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
