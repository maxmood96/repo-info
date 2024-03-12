## `buildpack-deps:curl`

```console
$ docker pull buildpack-deps@sha256:da13a0b5c77dc3e752cc9d9e185b9c09f2e2064d8e11218ffca5a57406a10bfc
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

### `buildpack-deps:curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cc05c08ca39e926630564a43219ac19163c7e528389960d2fe9e639025638618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73598930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15c215ffce5e7490aba71d8dabf58ef741bced74521af2c5f27869e888e3d95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0240b8998a2b49677c6ca0a32e10689d5c0117ba74d967e8a6d98fe7a4ae3fa4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70037013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca62b11afe7a8431a7e12380500c7c2eb46286dde03a2bf7cf121cb6e7d10708`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b872e7fd396a6833da36a5ef61e35ffddcffce622e76d99cd704ed9bc2bb9c56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67104123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff330e85d6b2d9a434a86e0c5df03f2fc83d2d5fd31e47532edcdd9512873898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:48cec1cd7e892dc51c4f2d7516b2ed8f391e116929b5460e3ae0c976ed050693
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73173860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ea96e7d1339ff33f942f8cc1315e0731121520bcbfac53669df4bb05c253fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7bfebc01b0982fb9874fe5bc61cb62bf8dba226d5fa3477f593bdad7502621f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75466713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7410bad07bb558d5fe093b6a01893c3a2b26334e114a68a3644836299bf37f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:47 GMT
ADD file:4cc8d7cc52399e70fff26562034447d71192cc79b9dac9551bce3f3046ba905a in / 
# Tue, 12 Mar 2024 00:57:48 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76c347d52f9093273e46a420ef3def7fbe603accb8533dbef53629d661d7d464`  
		Last Modified: Tue, 12 Mar 2024 01:02:18 GMT  
		Size: 50.6 MB (50581859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58451b255cbefff55ab1d06e4d8396e373e8deb00528e5b8f44a5575cb35e8a7`  
		Last Modified: Tue, 12 Mar 2024 07:53:20 GMT  
		Size: 24.9 MB (24884854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b18588551c4d881828aa5f3317b0536cc51d3663c096fa4d1ff409b1a7837e4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73193761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a9c2db66277195f38df723d4eaf40817c0a38943d94badc968e39f17f98be7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a9d2e59a230a9d4a04808ae004745f51e0e596953a2770503084886a3fb23f2e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79253819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5a24d3eb15d8f3b9ef6a936bb7a9d5b7a210c0779c7b2bbfc59ae6e0e14774`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:95b1f86365edd875e362c6d47e79763e1f3b7504f29992ff6abf68cefbf731c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71960165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d6b776a30a72031edeaea3d61789f2250d8181bfb7503c9857a93cb931e569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
