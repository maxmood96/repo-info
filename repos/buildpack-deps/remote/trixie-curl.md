## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:1437d0e48464912bd72673df80ded4c599c831c633811f1ba6877e7c2426dbdf
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3f50f9a8ec92d7613a2c9e4314890e8fa5fb3f242848fa896996af67bed51ce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76004089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd5b9cda28dfe341c6bfaec8d1d565301d3484e35aa826ec7c2422b55976899`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:23:09 GMT
ADD file:29b09152e341e5171aa28f4c4418697f0618e77dc8ad357953cb4e571071f7ef in / 
# Tue, 19 Dec 2023 01:23:09 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7ff2da0727c582fb559afda4ae37f2ea848c8d7098b1d441c8dd7223abd5ff94`  
		Last Modified: Tue, 19 Dec 2023 01:29:35 GMT  
		Size: 49.6 MB (49583423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59da6f1c57a0d30f89fd7c215ff86fd2807c97e9074d58deb7057cf153949397`  
		Last Modified: Tue, 19 Dec 2023 04:45:23 GMT  
		Size: 26.4 MB (26420666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:54054aae8d2509a606118039eeeee6c1efa28c6bbeb78b90e4812da597c0b30a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72158146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b16c510c0ddc939492d299d77df951dc4daec95385122ea2920a9f278bd749`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:56:48 GMT
ADD file:4525655c4460af6f1eea7b808845971f5115dc53bd3d22e1e5b904174f4a7de3 in / 
# Tue, 19 Dec 2023 01:56:49 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:29:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ef1355a3f40d35583d398e1a76163ce9edc9f474167738235259b9821b4cf763`  
		Last Modified: Tue, 19 Dec 2023 02:02:10 GMT  
		Size: 47.3 MB (47284749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd98b987b22fc6288f62a95eb2ac7f8fdfbdbbdf34f0f8c4bd2bd858a60f4ea`  
		Last Modified: Tue, 19 Dec 2023 05:35:03 GMT  
		Size: 24.9 MB (24873397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:76f97b54998bf37dbda2321e10a822a16b4efe0681560f69c73087df231cedd3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69139857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa32d2383804422278e6e86c011afc781c159888f3d9fa426946748a9708d2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:10:03 GMT
ADD file:3a9b07d7d2dd3958b5dd3f5e10d02d2e2f612023edc0a993b72001585b39fffb in / 
# Tue, 19 Dec 2023 02:10:04 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:03:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fdfd0725abb7810a629f5d363de8fc6e2d9dcb7251dbd35de649c96745cd052`  
		Last Modified: Tue, 19 Dec 2023 02:16:07 GMT  
		Size: 45.1 MB (45080555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc6f8d845eb2d7a99ad733d60426b1890e2dae97e2c100045f2a994f37727dc`  
		Last Modified: Tue, 19 Dec 2023 08:10:31 GMT  
		Size: 24.1 MB (24059302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b8c8fa8fa1b762cb6082830128bcba69fb55d1dce8c7669125b54d28f54a27b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75399200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800fef3e46173a59495d29a44218fa0b3400cfdfc28efd7e0088224f05da0dd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:28:50 GMT
ADD file:b661d22b170c983d1f8f6e1899757b3ea7418ea86f47bc616943149dfde25bbd in / 
# Tue, 21 Nov 2023 06:28:51 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:04:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f05f219707556ec064f3738b8347f22666ebc44f11201375d02acfd29240356`  
		Last Modified: Tue, 21 Nov 2023 06:34:35 GMT  
		Size: 49.6 MB (49571278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48906cee9fa2510e8f3e54f1027f9f1046eb7c9331600c58e2eccc32e1147c20`  
		Last Modified: Tue, 21 Nov 2023 08:09:40 GMT  
		Size: 25.8 MB (25827922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee003c3f905a9cad83790fc2caeae421adf065218be7ae4d9fc6c1cc9f172540
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77964535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b7006dfc2585e037c17696b58061ff5f3e840dff2ddd30d634621ac0b48054`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:50 GMT
ADD file:07e1f2376b64d47d8fc403056f0e46229ed95c88b19adf23f6eef7ed32a4efb4 in / 
# Tue, 19 Dec 2023 01:41:51 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:682156734dfed71ff79e9a6ecfa1d4b20e0cf3af70b52b635e877f84f0ed468d`  
		Last Modified: Tue, 19 Dec 2023 01:48:53 GMT  
		Size: 50.6 MB (50558518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bad710b49474b4b48a9b012369f62bfa589c2c14756ece1be2f50456d7c720`  
		Last Modified: Tue, 19 Dec 2023 03:41:47 GMT  
		Size: 27.4 MB (27406017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8d53552c020d8577a97b4d00b9e69b62db059054744745792dbe36cd56940603
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76039896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395b3db0610d69b3233d02d9a8dff807dc7974d8e92e849268c9aa8a8ac9466b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:20:17 GMT
ADD file:8ea6310c27e7f62f29291d04a24b83af6da2d5e3faa1996293119c2feddc0c07 in / 
# Tue, 19 Dec 2023 02:20:23 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:17:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b33999eae7d9b8d6555148eda58da0cc5207bcf4c08ed630879dc0190791680f`  
		Last Modified: Tue, 19 Dec 2023 02:31:43 GMT  
		Size: 49.1 MB (49068400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbe2cdae3821f18626a3cba0479848ecb8d93b32bc3d454eb52e1fe702148fd`  
		Last Modified: Tue, 19 Dec 2023 03:29:12 GMT  
		Size: 27.0 MB (26971496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:965f912e338611b668babc493a452d7633aada0b922596c5ef12cc6e50e27a3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82252709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bdba459863fec3e91bd7c853b0ea34383073b319aa7a132424943ec736438d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 04:26:49 GMT
ADD file:dc6f1d4d555ba3f35237b7e67b320c18ac6e1c8d12a95eedb8a5230f42402844 in / 
# Tue, 21 Nov 2023 04:26:52 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2c7e2ccd81c8e1fab8cf4a7e3dcfcc9c9057946f10830bacc66f9e35e00b25e3`  
		Last Modified: Tue, 21 Nov 2023 04:32:41 GMT  
		Size: 53.4 MB (53437879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3da93de48b4e366a300fc98f49a68981fa34793ac393d57b3adda3769aff47f`  
		Last Modified: Tue, 21 Nov 2023 07:10:36 GMT  
		Size: 28.8 MB (28814830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0f139df5ef4591e2c04f2e13de5dd226700837a29cd58118757b71f8a1af6332
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76060979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d02d58b5644aea5831d2ac9d8aed49d828461a7aade8a89dad2d9b0907b4c6d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:45:30 GMT
ADD file:b16365f9cf7d013b9f58428c1e63b824b4c10cd69e7e4899e47af1a279108581 in / 
# Tue, 19 Dec 2023 01:45:33 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b824578a72fec7523b71b452ffd659ecf374f66d41368945e63eaefb55285ad8`  
		Last Modified: Tue, 19 Dec 2023 01:49:59 GMT  
		Size: 49.0 MB (49047729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3918e3f5a21f3ff19f3099110f7748b164e79403be43cfceef60cb243c54219e`  
		Last Modified: Tue, 19 Dec 2023 07:56:10 GMT  
		Size: 27.0 MB (27013250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
