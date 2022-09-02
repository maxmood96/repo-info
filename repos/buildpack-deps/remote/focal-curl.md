## `buildpack-deps:focal-curl`

```console
$ docker pull buildpack-deps@sha256:a8824640956e33928bc5c6fd25b9fb2e95b006073a97ef29853482118ee74014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:focal-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:859a87863b458751a541038d05e5569e5f62dc78e39091b7b6225a3ea9745a8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39944615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71654a9ae5f8958dcaa319be61ebc69326d6eb070e287963d83a169357468b2c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceaa9f66a60a3695a6348be449df629aed61f57a9cbd55a388bdcfa40cb27b7`  
		Last Modified: Fri, 02 Sep 2022 02:37:25 GMT  
		Size: 7.7 MB (7747479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d69e69900ca0c9eb8762e001879c1e84e29d94a2397e389440b1d8689445e5`  
		Last Modified: Fri, 02 Sep 2022 02:37:24 GMT  
		Size: 3.6 MB (3624451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:906ed436fe65f8c2c684d883d3da1561827838dd0bc17e144d188a281fdfc753
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34449771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18ab99087c24b628efd9e394f93e2e04ea1b5e24f38fbc08e4f517e0ed66ce9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:56:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c939440c1bd88d1d1d434d3aa1ea94785fdbde5a1afb6314202876a124622a25`  
		Last Modified: Tue, 02 Aug 2022 02:15:15 GMT  
		Size: 6.8 MB (6756450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945d9dd06ca6053a40015193ee5c594f3eb35191a1cb14f2256dfa9a0c2cc08c`  
		Last Modified: Tue, 02 Aug 2022 02:15:14 GMT  
		Size: 3.1 MB (3104048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:196e4aebc99648365b96cdf49675a7565f1a2f51b7cbf9d53ab2589bb900f2c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38210796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b04598a2bdb0b055d6b09084c3b5a6dd5733efe3908208649fca71e2667f89d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 01:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 01:32:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c444542145972df20962fba6d4329459e66f2f686af24d63dafc2c5a1b6efe52`  
		Last Modified: Tue, 02 Aug 2022 01:49:44 GMT  
		Size: 7.6 MB (7631155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9924b49b3caa4a90a845795499c127cec28b1a834dea8b2af26a4a464f5cdfed`  
		Last Modified: Tue, 02 Aug 2022 01:49:43 GMT  
		Size: 3.4 MB (3387837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d47e1f12d9061d2873d9c60f1a8994a2c6caad46a876f0770ecf8e0e76d2f6c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46456575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046ee271c995217b16c2b683d8ebb2fd39ceafee110313d8835f9d7e5a71539f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:54 GMT
ADD file:eb82827919ea73f9595d7b0b70fe9aa5ff23e16ea6a87f7f9ef4e1905857b789 in / 
# Thu, 01 Sep 2022 23:49:56 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:35:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:891f6400ce611ee5975f04ad6d2c68305c76a8628b846df1b1f9ac7c45b1311c`  
		Last Modified: Thu, 01 Sep 2022 23:52:11 GMT  
		Size: 33.3 MB (33295624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c38e8344eceb4e722b9d2cc7cf0d2cdca38bb2870c652f545c8ea652efa4f6`  
		Last Modified: Fri, 02 Sep 2022 03:55:42 GMT  
		Size: 8.7 MB (8704791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059cb2841292be0e2908a7c8f78a0db3f136154b78b70a9881535c8c1080dc3f`  
		Last Modified: Fri, 02 Sep 2022 03:55:41 GMT  
		Size: 4.5 MB (4456160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ab0b4e710273e638ba716aedb8a727f3b67f94ddaa5ad6f5a9d494cf30423b20
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.1 MB (34132358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbe2f4f13bcb67f1b8b3ba8c4b939fab6dd3106951388314174f8343a01c67f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:09:50 GMT
ADD file:3f3a2d77633db008f6d929f63880dab6bd20eab1e346e715331cc1b32a9d9821 in / 
# Fri, 02 Sep 2022 00:09:51 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 00:59:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 01:00:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6cbb7395a087ad86b87360ff9e4682ac013d19b01b368e0d658aa360440c9e0f`  
		Last Modified: Fri, 02 Sep 2022 00:26:57 GMT  
		Size: 24.2 MB (24243281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da12dcd490d59114c83ba58a7ebb7af8cd20209af19b95285772857279ba9bb3`  
		Last Modified: Fri, 02 Sep 2022 01:48:06 GMT  
		Size: 6.7 MB (6744222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33395e6e037105cb40bc74d80f9d435cd4770ecc1fbeedd173dd4422aaacc2ee`  
		Last Modified: Fri, 02 Sep 2022 01:48:00 GMT  
		Size: 3.1 MB (3144855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:60896cc7f8a1ca84de78ac668cbd48eae132398b8df15d631a211d02450910a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37985463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f45ed43266896cb111d1ed39d77f6d9b84486fac419d2a02bc39d1cd023139`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:13 GMT
ADD file:75a78d9ec31ac5486bdde3e48ebfc534089c5f38f14850243c2ab2e632f0bbe5 in / 
# Fri, 02 Sep 2022 01:03:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:03:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:04:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b87ab7b8bb5c2a1f34d9a2e9887fde669c33cea7428fdb048362dfa81eccaa75`  
		Last Modified: Fri, 02 Sep 2022 01:04:49 GMT  
		Size: 27.0 MB (27045282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f81ff7514526202dbe703eab1c9f1a8c08e2fdc2c2d56b949c8d1f90825e908`  
		Last Modified: Fri, 02 Sep 2022 02:15:30 GMT  
		Size: 7.4 MB (7397526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf575bc155da8ebabf970fa2716a48bb3789c6a3967d83d0f7583991658942`  
		Last Modified: Fri, 02 Sep 2022 02:15:30 GMT  
		Size: 3.5 MB (3542655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
