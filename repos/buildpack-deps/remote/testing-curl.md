## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:47c2db02e27ea96262bb0a9a602438cdc33c2c644eadf6286f068fa16a8bf27b
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

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:aa729794d8f5acb183cf1a8cdc85376e27acb09dce5d18d415528b22b2bf0bfa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76493238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6818840bd13f8e03216e2d964273cdb62279f530466b2462388196cf6399e4ab`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:53:36 GMT
ADD file:99b2f09b38f37e8fb43da4af7e905a316ef0ae5d1372e182af7a4467ef8d7d73 in / 
# Wed, 10 Apr 2024 01:53:37 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e95c2810bf71ea304ff068100fda778bbde84d0612d720b0cab3e6069e85fa0`  
		Last Modified: Wed, 10 Apr 2024 01:59:53 GMT  
		Size: 52.3 MB (52332312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b66a844a336d24bd3d65fb1c2fa52cd05dba564c7d3c1a7655648d2891df776`  
		Last Modified: Wed, 10 Apr 2024 05:39:03 GMT  
		Size: 24.2 MB (24160926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:48c788d8882dace3838b893835c11bfd59f6a93e624dae3b061ef03626de271c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72463905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b86992eebca3f2cbfd5c138134ab833e08e26dd4d90c43cd804618d6aea2d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:52:01 GMT
ADD file:0476c16083d61e234237e2ef7156b893d991ebc8124b8bc6710b73ef2fe671d0 in / 
# Wed, 10 Apr 2024 00:52:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c8c28d868d5d3991cbf017b63d5fac41114aa7d2eac7b1224fcb86c76b143f4`  
		Last Modified: Wed, 10 Apr 2024 00:58:20 GMT  
		Size: 49.4 MB (49422136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3293a18c8b358e708c54799a531104a9ddde33e702e4608e103d0b33b15cb3a9`  
		Last Modified: Wed, 10 Apr 2024 04:58:50 GMT  
		Size: 23.0 MB (23041769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b5d2234555e7167c8ee99fe2b340e6fd1e6957a9131230b6a632393ec3c3f832
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69275247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ab1a626adb5be1888b4ba197d09814471397ae538b8169167f0542f9930bff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:01:55 GMT
ADD file:656b365d8d9314f1217c95cc1d4d7cfb6bec38e30aea70bfb00983db7de41d64 in / 
# Wed, 10 Apr 2024 01:01:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:55:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2733bd62bd4d649c9ab65374a55302ef287fbb5318c00121743e3223bf33e52`  
		Last Modified: Wed, 10 Apr 2024 01:09:16 GMT  
		Size: 46.9 MB (46920080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02643c0d13132e32e3d948fe0f9e603b1f3bc4e4dab635e89566aabcd733d1d4`  
		Last Modified: Wed, 10 Apr 2024 07:04:59 GMT  
		Size: 22.4 MB (22355167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:237011cb0e8b7cbbaac3052faf5ba301f216bcb4c318db3c384e02e32d1d2fd9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76072974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eecf5b3feff7578bc58f0490e1659c0f395a0f6df1f6480789622be1263bd77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:42:14 GMT
ADD file:d3b8312bf9d9df431c2580a0add351c37786bf532e919d2af2638c2fb93062ff in / 
# Wed, 10 Apr 2024 00:42:15 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:782f2de9bf3353a68116b53b16ae9a2387174b31cc46b4c9b4cf99de0a6e1af4`  
		Last Modified: Wed, 10 Apr 2024 00:48:17 GMT  
		Size: 52.2 MB (52193812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae77305c2bd54ea5f2ca2a76ab1cd96f744878b54d2b45e6edd47242bfa248`  
		Last Modified: Wed, 10 Apr 2024 04:35:41 GMT  
		Size: 23.9 MB (23879162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ade99aca5a25a9ccd47b950d25bce57189ae06309fec207a419bd20d9204481e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78464402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7140bd1b11c3401b355ccc13586f05f2d2fb3e2ec6fbf6f177c608da01b21968`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:363c0c44809b184ca8136ce186fb7b835d52282b57b2a32140cf8abaadb7c521
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76035641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2592a789f614b82ffe8267610de4d3d39c0e9172725f22ab8e5a3624e774be9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e1a174cecd869c3fd8289f4b066d74e54f34f3ff0c9e38a1abd9982699ce78ee
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82506849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95f420a26c17c980839b898bdf759d992457da02aa897aba31ff4e2aab0dea8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:28:55 GMT
ADD file:f2e3cbd5cfb4aff8ec6395d52d929fd664d9648429ab4d9e1153ee9f8459da76 in / 
# Wed, 10 Apr 2024 01:28:58 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c75969f9d1cfa02f8bb4ac9be57d10b36fc89340facd55e8f3ee886024860d42`  
		Last Modified: Wed, 10 Apr 2024 01:34:52 GMT  
		Size: 56.3 MB (56250111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c594ec063ba0274cc2cf2f1cfb2f564c330c348dec7ab928f2424a30b4f1bee`  
		Last Modified: Wed, 10 Apr 2024 07:20:14 GMT  
		Size: 26.3 MB (26256738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4b20bdf8acd620eae1640ec22d6586a86f6971ed08c1c7948614e1367dbd7d90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59d7cb1e7dd8f32dd4f85b2d674391885686d89c4e2b9e47b5eb6dd57c6f2b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:38:00 GMT
ADD file:a05ac36ba0a9e12dfdf53ad56de60918b6f7f530f4b32b570bdbbce0a7bc514d in / 
# Wed, 10 Apr 2024 01:38:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a7403c42a27ad5d5ea9a8c3224d14c269f7cb3da9339e45b20c533dcbe911289`  
		Last Modified: Wed, 10 Apr 2024 01:50:55 GMT  
		Size: 51.8 MB (51761790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c24ff3eb07a21f2639bb7d99f5c6a035571ca068e5457d79f063f14100f020`  
		Last Modified: Wed, 10 Apr 2024 07:33:51 GMT  
		Size: 25.3 MB (25297536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
