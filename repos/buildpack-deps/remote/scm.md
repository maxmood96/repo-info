## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:404bd888fabb9bc7fc7ee99eeffe3e8f11208e4e982bea7253e3f612dc8bf141
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d7bab0ce0bb912a82046dc41e3a7bfa7fca599bb1c2cef80dbb93a2d860e8eea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137694206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239cb8644596a3713722d266b6415ed57e494a61dec21b9d10d1333d7f0f7b60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:20:28 GMT
ADD file:98cacc5890a8c0b29d7a2b296774428cb2268b01b4ff97a84deadcd3b513f319 in / 
# Mon, 12 Jun 2023 23:20:29 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 03:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 03:27:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bba7bb10d5baebcaad1d68ab3cbfd37390c646b2a688529b1d118a47991116f4`  
		Last Modified: Mon, 12 Jun 2023 23:25:26 GMT  
		Size: 49.6 MB (49552112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2b820b8e87758dde67c29b25d4cbf88377601a4355cc5d556a9beebc80da00`  
		Last Modified: Tue, 13 Jun 2023 03:36:28 GMT  
		Size: 24.0 MB (24030539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284f2345db055020282f6e80a646f1111fb2d5dfc6f7ee871f89bc50919a51bf`  
		Last Modified: Tue, 13 Jun 2023 03:36:47 GMT  
		Size: 64.1 MB (64111555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e47b720b35ad887b644c94481713f1d2aeab7646224b6b5084d767cea5479613
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.7 MB (131671128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe93bb920dac94f750d11119c6fb44d3e36fe4979b953b01468151f735a7bb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:16 GMT
ADD file:8fc8e3b90ac0435374d713c6b80b23f1db0866a447cf839ea8304d4717982da3 in / 
# Tue, 23 May 2023 00:48:17 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:12:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cd47f968dbd1b839925549bb9a90d021c19486875443123fb77e8cb1367e9745`  
		Last Modified: Tue, 23 May 2023 00:50:22 GMT  
		Size: 47.2 MB (47168971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58dcd7a31d73fae7c8f3da6415b83f56c0b8c1635526741fd0c65632ae15973b`  
		Last Modified: Tue, 23 May 2023 01:20:37 GMT  
		Size: 23.0 MB (22950966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64527cb5109ec935f8bef268d9948c57924a7b5d1bbcda29e980f1bf4a6a37f2`  
		Last Modified: Tue, 23 May 2023 01:20:56 GMT  
		Size: 61.6 MB (61551191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f01d82663638fc6987986560652d11f20c972e1548a53a9b5029cba01a44c873
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126434690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c2ccafb109647b4d25e13c628aefb8e6b0bc38bf9c4bea246e541506d18d9c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:58:10 GMT
ADD file:3af917fd4b956bc618904ef0ee9783c26f07442cfd03eebf92634280dcd2fc44 in / 
# Mon, 12 Jun 2023 23:58:11 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:53:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 04:53:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7bd3ccf07376cd3298bc10edd37d559052da8db8b3a4329639d1f41ad9e69921`  
		Last Modified: Tue, 13 Jun 2023 00:03:22 GMT  
		Size: 45.2 MB (45236172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439a533a0b4799f8a60760a80b337bf9724ded54f0f7facab28b264865a81714`  
		Last Modified: Tue, 13 Jun 2023 05:02:42 GMT  
		Size: 21.9 MB (21936536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942cc1e35dbe7aae8168156a6280c6a0a19a18be2bb0c778e651239f6d8951f4`  
		Last Modified: Tue, 13 Jun 2023 05:03:00 GMT  
		Size: 59.3 MB (59261982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7ba0d1a25006d797d3397f534b1cded1232c7fbe326443abe002ce68b7f5afca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137126490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdf78c43d1787a020bf48e15c509d6228cd39857ffe60e2cf8c08442f4cf1b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:59 GMT
ADD file:0dfaa4beac7b0a95f2b33bc35e08b104057469f46fa35df2af7193451ab3714d in / 
# Mon, 12 Jun 2023 23:40:00 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 02:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 02:59:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a31111d070044ed920abddebc16bfa67a69fb0e0e782b703073c93ec10dedf67`  
		Last Modified: Mon, 12 Jun 2023 23:43:47 GMT  
		Size: 49.6 MB (49573162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2455b35210792787557bbd2b0b976aa27a8bd5931191be95c7291b93b9e38f6c`  
		Last Modified: Tue, 13 Jun 2023 03:07:36 GMT  
		Size: 23.6 MB (23569494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd13397d6ccd754586b475131a51ebeb69394eb49de84b647f4fb6a38703da89`  
		Last Modified: Tue, 13 Jun 2023 03:07:53 GMT  
		Size: 64.0 MB (63983834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5c4936ac3f9de5cc5875791b88e30056a674b389eab9c3d5a32365f4765ff800
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141404377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:478086933ea7cadd122d00ddc1426b1042800b116f0d3dbc1bd4006de053cd84`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jun 2023 23:39:02 GMT
ADD file:a0aeb9b361b31d75c8d96223fac8f3df2807735ed20715b24af45a414ad3965a in / 
# Mon, 12 Jun 2023 23:39:02 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 01:01:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 01:02:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9cf3331eb07181e9e59fdcd7e0dff8a268c9d12151911a49cf687e8007305b4`  
		Last Modified: Mon, 12 Jun 2023 23:45:56 GMT  
		Size: 50.6 MB (50562393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33fc0a6f3d4758dd5dc471507894f4b6b8ac213c61fc008a6c75fc4dc4f56265`  
		Last Modified: Tue, 13 Jun 2023 01:11:16 GMT  
		Size: 24.9 MB (24869788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6b1139f66be902e73f6166c1ce5ace1377a0dcdc4349a092edb6f3c19d6dc4`  
		Last Modified: Tue, 13 Jun 2023 01:11:40 GMT  
		Size: 66.0 MB (65972196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:96cae88d70a5e257946507be52409fcfa7b8ce089ec2aac8d498480eab748c2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136103723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee92b5d400c250be9c84cba11c689ddbdeb640012f654030cc8624058c182e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jun 2023 00:08:08 GMT
ADD file:fbe506fea544eae98a8a13d6b55d001b4327c933053d898d5a19bf9ffd7470f8 in / 
# Tue, 13 Jun 2023 00:08:13 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 01:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 01:56:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fb5fba29e113a7ea4313a026e3a37cd5bc1425850dfd19a63973d48c89e0f266`  
		Last Modified: Tue, 13 Jun 2023 00:21:46 GMT  
		Size: 49.5 MB (49541536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d455436c8b88038e08b0000c9ee013619617a7c7820a0bf065a54b80a660d`  
		Last Modified: Tue, 13 Jun 2023 02:19:52 GMT  
		Size: 23.6 MB (23611740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ac31b2b51452164efc6b46cc660d0ea7af24261706ad3f016de4af1ae4cf65`  
		Last Modified: Tue, 13 Jun 2023 02:20:45 GMT  
		Size: 63.0 MB (62950447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a70fee0093fc78a9ced3f519cb0f01aee68baedc6ac1f6a1afa1cc11103d3ff1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148803187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e212d4fafe68f0c10626374ccb6d62ba1b8d22f76d5b5913300ed6cfe2ba0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:16:38 GMT
ADD file:28e774b3554d274fc742feac48f78a3bf6f120cb729e2824007dd94d5c414156 in / 
# Tue, 23 May 2023 01:16:40 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:45:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:46:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e109feef3fc6307cd9a880958cef6624de9c2c6f054987e479461a1ae51c7503`  
		Last Modified: Tue, 23 May 2023 01:20:49 GMT  
		Size: 53.3 MB (53312324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab84a55cc084469df8b38ab6a01658bfba2b29b7410a970ba6d9d2864846672`  
		Last Modified: Tue, 23 May 2023 01:59:19 GMT  
		Size: 25.9 MB (25923867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfbe0bc6dc85168e7da83a7be20c9913921338417e0c639a93ff1cdc5664403`  
		Last Modified: Tue, 23 May 2023 01:59:46 GMT  
		Size: 69.6 MB (69566996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9e1d58d54da9f531f48f7da4e9eb1ef172f8abfd60275d5e7833ff3b286c5d72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135054673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3c11d4a07fc41d0ed681756a03518e460b192440f51d9e10acefb26e3bfdd50`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:42:04 GMT
ADD file:cc95a0712a6bccebd449eb4ff979eeed054299ca9b7766e545c76d0c23c957ee in / 
# Tue, 23 May 2023 00:42:12 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:32:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ffb123da88ae28227159c41b0f21826f6497089ece0b790a5c14d890cf50771`  
		Last Modified: Tue, 23 May 2023 00:45:12 GMT  
		Size: 47.7 MB (47673474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3541e04aeeb82d496c085951f9619fcdf7bce92b4b7185f684cbb7ef6f65ea32`  
		Last Modified: Tue, 23 May 2023 02:37:57 GMT  
		Size: 24.3 MB (24270889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b984494917df72746bed1d04a989f9f1cf3cbeeef990a9d0a58690373ab6ffaf`  
		Last Modified: Tue, 23 May 2023 02:38:13 GMT  
		Size: 63.1 MB (63110310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
