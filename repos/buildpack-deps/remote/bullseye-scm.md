## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:db92d660ceea12ef653ba60cef54fd3fb63db56973037c180611382179f7c9e0
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:491f9506339626aae7333f0f58a4e75b9cdc71bcb58d106a3257d0d0afc88ba2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125619430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33be850c6dc5a996da695ff02cb949468aa640a5b643fbe3a7c0c04f7c9b5e3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:20:12 GMT
ADD file:dd3d4b31d7f1d4062ad0eb2d85dba064cea067b1eb4a8b89a0b593ea90001cdf in / 
# Sat, 28 May 2022 01:20:12 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:41:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e756f3fdd6a378aa16205b0f75d178b7532b110e86be7659004fc6a21183226c`  
		Last Modified: Sat, 28 May 2022 01:24:51 GMT  
		Size: 55.0 MB (55009253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf168a6748997eb97b48cc86234b7ff7d8bc907645b9be99013158b3f146b272`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 5.2 MB (5156036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e604223835ccf02d097187b5a58ca73e8598cadbb16a36202ca1943e97f56f1f`  
		Last Modified: Sat, 28 May 2022 02:49:08 GMT  
		Size: 10.9 MB (10875008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5c91c4cd86dde23108ab3af91e9eae838d0059a380ee7dfd4f370b6d985523`  
		Last Modified: Sat, 28 May 2022 02:49:31 GMT  
		Size: 54.6 MB (54579133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8fd7b32c927bb0cdd6b15e11702125f618d95531e492290a62492809db62be0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120494591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff548fd77027c99f7df3d4b735b2c1dad281d9e47d2957a2d31525b10bed01c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:02:30 GMT
ADD file:9d07021c835c5f732ea075ba0041aa31bde8abc22d82e5d63a9bbb657e06c8c8 in / 
# Sat, 28 May 2022 02:02:31 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:06:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:07:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:79c7773dc1de9c078f2f930718c03386e07f9f63af58d616b21cbe73dae47630`  
		Last Modified: Sat, 28 May 2022 02:17:48 GMT  
		Size: 52.5 MB (52540761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8018bc8b592b81a5698df2daaeb0d67e1e6c7f114a990ec56b0a9f1c498468dd`  
		Last Modified: Sat, 28 May 2022 03:30:31 GMT  
		Size: 5.1 MB (5065336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26804cccd3a236a140a0621c20aa221dd0dcc84587297365e0e57b5cd7c21fa3`  
		Last Modified: Sat, 28 May 2022 03:30:34 GMT  
		Size: 10.6 MB (10572975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b1c09ed6ed03cd99b187881b9efc843f582b9e68f00f0ef53d168e86bebc80`  
		Last Modified: Sat, 28 May 2022 03:31:26 GMT  
		Size: 52.3 MB (52315519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8c25aacef0be7dc7a3260339b62b573470437fab81776a048be523c8df28ec35
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115671799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2a971139bb03dcd66fa3deba5840e0391cd66bc0214a0c944c0954aa9f6b2e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:59:10 GMT
ADD file:faa82773e36b14c218e792730b0264c016864613a8d43cfaa33864075b0ef169 in / 
# Sat, 28 May 2022 00:59:11 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:42:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:42:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:43:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8c8b1770c0de8d780b721bb37e9a8b6e5071a83530a584b1aed8ddc9aa12dd00`  
		Last Modified: Sat, 28 May 2022 01:14:50 GMT  
		Size: 50.2 MB (50199379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7380c9813fdc7aac45d249b456f89965b8eee97a56d8cc8d01bf2c09bd344e`  
		Last Modified: Sat, 28 May 2022 03:08:58 GMT  
		Size: 4.9 MB (4924792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed7ad25f71b787f363a804d83f044bdccc37536ae3e8856aecb500db41357a0`  
		Last Modified: Sat, 28 May 2022 03:08:59 GMT  
		Size: 10.2 MB (10217910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927d9aeacff3f0d387cb224277ca6a3173e26fe6f535adcca91aa8b2a5fa35c0`  
		Last Modified: Sat, 28 May 2022 03:09:50 GMT  
		Size: 50.3 MB (50329718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3e69a42c168e5fabc7d234a2e17ebe674f92b321add51ea20c30b2f760d7bfd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (123965222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528872acee213d6070d7599d6c7af83b4bf27aefefff72a7de6d76b62bfdb22e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:40:23 GMT
ADD file:a78273677555ebe8bac187f491203093eec62fa1c4f65f00ba2cf0cc2230992f in / 
# Sat, 28 May 2022 00:40:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:05:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:05:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 11:05:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d794814721d57f8aaec06ab3652e90212cc3beccf5ff5c87f6ecf8375784bcc8`  
		Last Modified: Sat, 28 May 2022 00:47:04 GMT  
		Size: 53.7 MB (53696947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf62ee63325dbbad699d6845f68c2391db3bf158f60373849c2d1cb6bb479788`  
		Last Modified: Sat, 28 May 2022 11:17:05 GMT  
		Size: 4.9 MB (4938744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e37b4c58dd1db7ead6f3c2cdf757f490b4e29c958d2a70559c313e9a03a5ef`  
		Last Modified: Sat, 28 May 2022 11:17:06 GMT  
		Size: 10.7 MB (10657073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb366fec153b3461ef6bedb0d03ddfd52da9b314025abfccb50a3e8e8669fdb`  
		Last Modified: Sat, 28 May 2022 11:17:29 GMT  
		Size: 54.7 MB (54672458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5c35da77158b0e277d91087fa1bf9d278e099a00269d331ffb9327c8dd765aed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128037018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567513c3d81759a2ad0234e6452c65657b455b383b4b05204487b9926c7d688f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:16 GMT
ADD file:2ecdc28ede565866b7302862c5e2a4b70a3afb165b383a4df315957be6dd754c in / 
# Sat, 28 May 2022 00:39:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:10:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:10:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:11:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9460ac70d7d688bab5f76bf5c30d1d8577c1fe0b74778427b0febf82ec246360`  
		Last Modified: Sat, 28 May 2022 00:46:11 GMT  
		Size: 56.0 MB (56008088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8e3a15723f23c48aaec99a47e8db8febb69c63c6c4fb228e79be0e24f60990`  
		Last Modified: Sat, 28 May 2022 01:21:17 GMT  
		Size: 5.1 MB (5080488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957fef8149909e6cd1b5e9ec92e3e9fa99c4f56aa60aeca1fb6d09b707c41357`  
		Last Modified: Sat, 28 May 2022 01:21:19 GMT  
		Size: 11.0 MB (11033704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88acada7e0f75318a771bbda23d86cd3ba06d286bbf27e121de75b94b6bebdc1`  
		Last Modified: Sat, 28 May 2022 01:21:41 GMT  
		Size: 55.9 MB (55914738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:914c9ff8f2341c47586c9e29c741756a9ecb90cc6eb2ac63f189712960828675
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122143249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99de07e655d8dbc229785af6ffdb33c239133f595bc92638376137080abf2fdc`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:10:35 GMT
ADD file:bf0066890c02fe9254ebe22df9f29cfa14ff8023e297cd8ce14c32d423c81099 in / 
# Sat, 28 May 2022 01:10:40 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:54:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:55:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:56:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e3c10d3d838c43f5c37f26af81b379c8e9fd26b58bb2a30e2b137934e2266ef1`  
		Last Modified: Sat, 28 May 2022 01:20:51 GMT  
		Size: 53.3 MB (53272327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0960f5bc3793d07cc0d0910bedc52256987e77a953ca437c6dbc0ad21bbb6b3f`  
		Last Modified: Sat, 28 May 2022 02:24:16 GMT  
		Size: 4.9 MB (4912484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cba3dabc5ac5e0b5c503a658e3366ba3e36e5989ca98f5b3c9993bee50d5cbd`  
		Last Modified: Sat, 28 May 2022 02:24:18 GMT  
		Size: 10.7 MB (10660152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca0affb9d083d5f8df62cc8c4cd9f2b3dcbf363568b23e7e693afdd8cf8fd70`  
		Last Modified: Sat, 28 May 2022 02:25:08 GMT  
		Size: 53.3 MB (53298286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f9f1776ce26ba9418b8a1f9990e28ffa55e173467f09cc2f1711ab559311a15c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134790489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be81a28708c4c889d6dbb1941d1fbe413bc893867c8ac4b234f4cc1a968c0455`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:22:18 GMT
ADD file:0cf54bc63a3f2c0d5652c62456619ccdd983f64f718a89816c151963f108461f in / 
# Sat, 28 May 2022 01:22:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:08:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:09:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a8d10cab014c8bb87d1db1758eacc9d3a16b40994eec1e70e2eef174276708c`  
		Last Modified: Sat, 28 May 2022 01:31:45 GMT  
		Size: 58.9 MB (58902658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334d538bb77542dfc1477efc6f61b979fe29753a36b5d737cc364dc0d9f86efc`  
		Last Modified: Sat, 28 May 2022 03:35:27 GMT  
		Size: 5.4 MB (5405331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906792e5a6009d831898c2831924e9e231cf3a44b49158b5d31fe4443e264c36`  
		Last Modified: Sat, 28 May 2022 03:35:28 GMT  
		Size: 11.6 MB (11627416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cc745f5a7e9f7d0eeee27a7cefc4b0663e9bae7346397e8a30d16c15cd0ccf`  
		Last Modified: Sat, 28 May 2022 03:35:55 GMT  
		Size: 58.9 MB (58855084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c7bab51b29f5d8cb2180be4d864277ebd7f94674e2c91ba64bf7d8e2c8dc1885
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123227364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e20e4c864de20d2c95aa7a612c15cf95933e4d231ac47a4921879a75b15ad23`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:39 GMT
ADD file:2aa6033cc58847736587260ccd8559fcc352cb0c91436fe6bc98ff1c0e457cc2 in / 
# Sat, 28 May 2022 00:42:42 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:23:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:23:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5729889737c79e488091d7133428cefb547531cac87f70671a7a8def5c83b822`  
		Last Modified: Sat, 28 May 2022 00:49:25 GMT  
		Size: 53.3 MB (53276622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8c82464c5aba6b429740f5e491eb99acd73a79a066d32206dece6dddf15135`  
		Last Modified: Sat, 28 May 2022 02:35:04 GMT  
		Size: 5.1 MB (5140603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2def663d7ef6cc773e576712a1ab885d906b1d5fd627ca2bb09120f3366d3140`  
		Last Modified: Sat, 28 May 2022 02:35:05 GMT  
		Size: 10.8 MB (10765425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec40ed3a753730ad01fd413a02ef67b6d923582dbd602a0bf67e6b1d6723c3c`  
		Last Modified: Sat, 28 May 2022 02:35:22 GMT  
		Size: 54.0 MB (54044714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
