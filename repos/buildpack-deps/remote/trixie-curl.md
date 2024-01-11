## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:d3f499f4ecbe6f1c7929b6fcc1782da32c79a632c778a9d3cc2cb2f0eecb1419
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
$ docker pull buildpack-deps@sha256:6bad5091144d0e3d37b9958559cf68f0f90d1a84e22439cc8e8c0b1c911b7761
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76026283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8febe876a5942a8eda15c9e8f1c3a4729913f45784db20162e41a95574ea0de0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:38 GMT
ADD file:221c5996f1ff4dd71764ca719f363e27bb329a807e397f6654cbb3c478c54c9e in / 
# Thu, 11 Jan 2024 02:40:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5c06b5f92f5d425b6a1eca65d06813d5da1bf325255b6cdab64db03a7ee0d47`  
		Last Modified: Thu, 11 Jan 2024 02:47:11 GMT  
		Size: 49.6 MB (49562052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b14ab6cee5b8a008ac52067ba895976219bd813b8d4aa739a74ba5ce9121594`  
		Last Modified: Thu, 11 Jan 2024 04:48:48 GMT  
		Size: 26.5 MB (26464231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:380da98df673454f90aa80a5dcd0c7beb69e5d9ab848a45d50993b84a7aa1437
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72203867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f2fafbe478353678f8358c8daec31f58792b98944f84c3cbf1f161a9130e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:51:35 GMT
ADD file:406477db7977cf7bae3dd986446192c7a9c9187721f800f6414add12009ed4fd in / 
# Thu, 11 Jan 2024 01:51:35 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:02:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2ffe09ad7d6788d69349e61610eec99edf75d529a8f29e51e982f323dd5b39a9`  
		Last Modified: Thu, 11 Jan 2024 01:57:42 GMT  
		Size: 47.3 MB (47275273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbe43ce8740ef7b4c0109654d60ec4abac22aef1e893ddf0a49dc137bd8ece`  
		Last Modified: Thu, 11 Jan 2024 07:09:58 GMT  
		Size: 24.9 MB (24928594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:93b651595e2f60da0d3719b391dbfbcc48e323e5d3ab05a9ee82584bbf879b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69166681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e161c2fd80f021232959d9b8eca8f6d8326eed584e9a39d452e3d983cbc3e3e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:45:43 GMT
ADD file:2578bbd6242f569b630ed2a8dbbe60a6317a1fd910aebe4814313b4c0eb7a482 in / 
# Thu, 11 Jan 2024 02:45:44 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d77eb11f48fd53e8f4a4cad655e31f2fb5f91177fb35abe347a055a3352eff1b`  
		Last Modified: Thu, 11 Jan 2024 02:53:33 GMT  
		Size: 45.1 MB (45063448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37916331c99d3b698aae6553fb6c2a2c76d2cdb8dea2d3cc6e825c690f03420`  
		Last Modified: Thu, 11 Jan 2024 03:34:33 GMT  
		Size: 24.1 MB (24103233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:97fd699a16bff4f4bd43aea65a65c9c5daa93af27dcde89a694a28865c0e5b60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75566215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac371db66dfde3c88f7ad1f260fd03c0f692c3408f008d07bfd3f8e42b48bec2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:55 GMT
ADD file:3a7cff48546e976afb3192375ccd816fa228a2a86ca359ad2d25968d89736a30 in / 
# Tue, 19 Dec 2023 01:42:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:54db10be8b28565099ed8931d6e2048335ac2a2e8633f5ee9961d35950099935`  
		Last Modified: Tue, 19 Dec 2023 01:48:52 GMT  
		Size: 49.6 MB (49615103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3258514d2e2ba8de515d7376cc008e3df15536a3972bbc964930061817df14e1`  
		Last Modified: Tue, 19 Dec 2023 11:45:54 GMT  
		Size: 26.0 MB (25951112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e0fa21d18c633a8bdcfe78d55cc3fcbdd347b44f7d11a71931963afcda5892c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77980950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd5e0cc77f1bbc7e2e30b4228724f5bf145f8b10deed217cb1e2689c691bc5c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:24 GMT
ADD file:5564e4ab4c2aca360aa2b99bcb8c9c77e6d97554833ae3cc9bb2f49ed35e25b2 in / 
# Thu, 11 Jan 2024 02:41:24 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:39:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a827afb392949e39b5beea804bcbbd7be98a07848f45ead6a59e020bce5836dc`  
		Last Modified: Thu, 11 Jan 2024 02:48:52 GMT  
		Size: 50.5 MB (50527068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181d3088fd6488ff4296a6d76024c5ceabebb089069d60b6dcbf62cc62624985`  
		Last Modified: Thu, 11 Jan 2024 04:47:28 GMT  
		Size: 27.5 MB (27453882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8d8f8572554c24a4a5140ef38ba287518427e5385eb62996695b85aed096bad7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75538201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca7f9fefa124774b1983005ef3a10453f3f34b181db0d117219bad2773bf343`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:18:24 GMT
ADD file:f8968c17bd3825e4f058fd68c683a3c699e06368b69577a14d575a0c3ac70e6c in / 
# Thu, 11 Jan 2024 02:18:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:15:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc5cc64b8a2f7c7d0c78917ac707955e566c39f9c62003870eb7cd32f7b23a5f`  
		Last Modified: Thu, 11 Jan 2024 02:30:01 GMT  
		Size: 49.3 MB (49333270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136a6eeb1b81bae44e0e846833442693a689a375fce576961be0a2c167f5f861`  
		Last Modified: Thu, 11 Jan 2024 03:34:44 GMT  
		Size: 26.2 MB (26204931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a087888fa02c27645d206a502362a4d1d09290b3068c0116b5791488dd2c2f8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82401008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acb12899776a5c70469b1736c4c8ac851f0d355eb2634e5afa3fb2160035b71`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:16 GMT
ADD file:d68448f447d4318f3f9fad32f62806e0a419160a92848f345b24ec3a1aa68cf9 in / 
# Thu, 11 Jan 2024 02:37:19 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:18:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:451fd7c87652550c3d81b74039588f9cc1098943015d72618adc689c50a31de3`  
		Last Modified: Thu, 11 Jan 2024 02:43:06 GMT  
		Size: 53.4 MB (53435762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0721dab59d6faf980a2731617cf00ce4d4f5118003d8d0c3dad0ce0ff7844f94`  
		Last Modified: Thu, 11 Jan 2024 07:27:03 GMT  
		Size: 29.0 MB (28965246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3398a38e8165291e04adf7d360035cf102c95a23b69e951e1268c9ae228e0500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76291680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514e2d2dca99e46bc3c8b4c1792e00a3006331ee6944d40330830ca21526cf78`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:48:25 GMT
ADD file:3ce2a6c625c267468f6ecc7899fd855c1705b7efb767d466e8b5e859b1047897 in / 
# Thu, 11 Jan 2024 01:48:31 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:15:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:14c1c69c5e90f50e1791d192ea58f134dbc8ecc231a5b815d4c7ee99ef3a1ff7`  
		Last Modified: Thu, 11 Jan 2024 01:53:03 GMT  
		Size: 49.1 MB (49091863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f3694e83d440b396cbb77938e6510f4437f21e56dc3bfaed630e6caab9214d`  
		Last Modified: Thu, 11 Jan 2024 02:23:52 GMT  
		Size: 27.2 MB (27199817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
