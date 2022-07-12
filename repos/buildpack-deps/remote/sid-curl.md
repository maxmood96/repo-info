## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:59faf5fbfc0905f18ae0f20e2819a19a00142674735f8f7e1856aae9a9dcf1ab
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d34c812f68b7964a89e7850a891757b7c471ea95398ef2d7e27df1cb0d274450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73793751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63bd1a814d6810f02fe1200b850c86355c0102c19a7823ec67fc2d457b29c34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:21:07 GMT
ADD file:0aaeb8a0c7fde9f030dc2ab67a03f21f44e9eecad9e4cf1f360dc5f768292460 in / 
# Tue, 12 Jul 2022 01:21:07 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:50:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:51:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:4a81bc091a3ce5ccc3c89ef56e710ee1854c5ff9fd3d7f148e87cb956b5b78c7`  
		Last Modified: Tue, 12 Jul 2022 01:26:19 GMT  
		Size: 53.2 MB (53226349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b567a2d645b715cf7eced5f75816db7c980c3416be39e599e6e4b0bbc82f9eb8`  
		Last Modified: Tue, 12 Jul 2022 02:57:17 GMT  
		Size: 9.3 MB (9295637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303c4db152401668239f15446f8107b320fcfdc241030fd93f94783340b469ca`  
		Last Modified: Tue, 12 Jul 2022 02:57:17 GMT  
		Size: 11.3 MB (11271765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9def20650247b2230980ebd69d23330d0a1a30340ee1bcd273342676d3094df9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70694157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68f962fcf1e5b4ab1e32d6070c47a265008661972cb1e41602cd155ff2f9d07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:53:06 GMT
ADD file:d09e1e4b772f7be41e6f5adcb5a71d86548e6099876e8d5d1bf8eb816a2d8cf9 in / 
# Tue, 12 Jul 2022 00:53:07 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 01:47:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 01:47:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:c8fedff5488db39c94b1a6e628f1dd8a8718a76f0b9f0a65f57e06652448e9f4`  
		Last Modified: Tue, 12 Jul 2022 01:06:36 GMT  
		Size: 51.0 MB (51027952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fdb9c4c566afe6ee79f348756dbd9b7b7752109285ecc12936279d515cc71f`  
		Last Modified: Tue, 12 Jul 2022 02:03:57 GMT  
		Size: 8.7 MB (8725449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece2169f6168d0cd57063262293e9a5e841d140a27a657883596ac7fb3cafeaf`  
		Last Modified: Tue, 12 Jul 2022 02:03:58 GMT  
		Size: 10.9 MB (10940756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4c66d10d2d7da5aa68a29db4d78562becc926db2133c316bfca39c9782b286fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67713014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:431c791598b945c7599ba7b616b5f660bec9cf5b25aa3a940b61289dae7f25fb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:03:16 GMT
ADD file:51a321e16e02701a4130fcd4804ef7e14f5facfab8a82cdef3c2fd228a4ba034 in / 
# Thu, 23 Jun 2022 01:03:17 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:54:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:54:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2391a5c3a80e9c0555d4b398df748ee8be95db129c7c16e82cb7755d493118a7`  
		Last Modified: Thu, 23 Jun 2022 01:19:50 GMT  
		Size: 48.7 MB (48734709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d1193f1a87016b7e352fd620d9d5e616526a8c1d9ac8cad6c77aeb6559fd09`  
		Last Modified: Thu, 23 Jun 2022 02:18:45 GMT  
		Size: 8.4 MB (8405462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59543246561323586b73771e4cfd176cd7d73ca9c0e20cceba57a93111ba12c`  
		Last Modified: Thu, 23 Jun 2022 02:18:45 GMT  
		Size: 10.6 MB (10572843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b938bc2c9abf52f196477963146f37d259cead2e226d80950483167e4bd66497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72528212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c932177d42941c6fda777d16de5930c0f4d5b5a24eb40c0c2d3b27344ed189b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:40 GMT
ADD file:0f18dcfe7e502abae9dd7f72911dda640e4675306760d63f467092f962228ad1 in / 
# Tue, 12 Jul 2022 00:41:41 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:36:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:36:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d3ef27d3c918a6321957a64c33268d09a01ec18590cce79a144625d9c0c8599a`  
		Last Modified: Tue, 12 Jul 2022 00:48:17 GMT  
		Size: 52.3 MB (52331756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f3b169736466d16aa015562be48cd38804707291d997ad0a77f69293eb28a6`  
		Last Modified: Tue, 12 Jul 2022 02:44:53 GMT  
		Size: 9.1 MB (9139825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fef5554fb71c819accf1cb6b60a439cb9c6a8da7ad329ecdfa59582ef1f116b`  
		Last Modified: Tue, 12 Jul 2022 02:44:53 GMT  
		Size: 11.1 MB (11056631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ffbcf2722ef04e82df0329e8c4a891c3cd9e6eb1a91910e955e91e3c81b784d2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75111099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86852b4e5c4a5363fed719d25e53dc3df0d92192ebbb94112ed4952fbe449a49`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:59 GMT
ADD file:8e587a340c6b6c6dfa097954552e77cf8a794c99a1462d0c2062dd4f3b905687 in / 
# Thu, 23 Jun 2022 00:41:00 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:15:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:15:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:82252cde47e9fb82645e6353c13b39594115b4ab4b96e5a602245359036bb69f`  
		Last Modified: Thu, 23 Jun 2022 00:49:29 GMT  
		Size: 54.2 MB (54181034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a804107ac0ac6b959662ec593acb07f7f7900f2753d01cc321b3f498797ff54`  
		Last Modified: Thu, 23 Jun 2022 01:24:44 GMT  
		Size: 9.5 MB (9465816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3278139543c9edfb79cec19d272bb6af19642454308507ba2015c252c4b5462`  
		Last Modified: Thu, 23 Jun 2022 01:24:43 GMT  
		Size: 11.5 MB (11464249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0ff4a74532f3523ffb2e37cb870db09a06593b35773de23f95c05f5df910f311
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71980014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f332c9f7710c0dbcca7ca00fc8c1cfb9d05fa74b0d47e3a03e3a58125961dc52`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:13:03 GMT
ADD file:ee6af73e7954397e332676cdf91fcc81e58c7039ee0e6b28c76a45bbcd35f878 in / 
# Thu, 23 Jun 2022 01:13:08 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:08:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 02:09:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1122351c74d1f54ed8c97871bc43b5e9e533e877516d1335d49d0b35a135e12a`  
		Last Modified: Thu, 23 Jun 2022 01:23:42 GMT  
		Size: 52.3 MB (52302602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b60fb601ee8b9ce8fdf454454bc04959e78f2245d78fb79c1fd28d74c735fe`  
		Last Modified: Thu, 23 Jun 2022 02:26:28 GMT  
		Size: 8.7 MB (8657901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a790127ad374d0d7dce1e83718b6927775398eff00185730060dfa660ee1c63`  
		Last Modified: Thu, 23 Jun 2022 02:26:28 GMT  
		Size: 11.0 MB (11019511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:70bf422e9a395c4b0a8197af72fba614ef40e2d75ed0608a4fa349126c4d2725
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79362837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08e778d8f74f1ee130c5b7e78d15d7e4fff1768e8b3753a91d0cfe2e9ab8946`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 02:04:45 GMT
ADD file:c9757ca75462d85dc4d76c948caf7c9441b1f94311712aed484424049dfa236b in / 
# Thu, 23 Jun 2022 02:04:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:36:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:36:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e03a908039ec9067867d0cfb4e2137913335e7055a4de7caa5a17b06fdcfc936`  
		Last Modified: Thu, 23 Jun 2022 02:21:32 GMT  
		Size: 57.4 MB (57413710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012e0f9d40f6756a17c2a26c1540b57aef08309d861a58ee201ce546d8e16f89`  
		Last Modified: Thu, 23 Jun 2022 04:59:07 GMT  
		Size: 9.9 MB (9883975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26df9fd6cda08db21eda8015d4fac544f2e705c64a73aa93ac154c59b04ee95f`  
		Last Modified: Thu, 23 Jun 2022 04:59:07 GMT  
		Size: 12.1 MB (12065152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f3001e6db8ff5ae74e465a953fb9a1d3dd64846bbb31f0d42fe5493b1b59f92b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68491637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7648e9385ddf020464c24f07cef291a6853a4552ca65a6b8e8253e26708443a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 01:10:39 GMT
ADD file:bd8475470f5c6f95d31c06b918cd7725db4098699597cddbe66f7d30cecdebf6 in / 
# Tue, 12 Jul 2022 01:10:42 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:16:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:18:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:e08ecdb135d5f5e0335332e1597ae44e5c8eb292461b299517cd917fed413256`  
		Last Modified: Tue, 12 Jul 2022 01:28:55 GMT  
		Size: 49.4 MB (49440738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb7bba79828c7c077abda404edadc49cf674ae2d2268ef7749779a9b29a75ce`  
		Last Modified: Tue, 12 Jul 2022 02:59:04 GMT  
		Size: 8.4 MB (8394915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e028c389ce83680914e57b7f8fa251005e8f6822edcc336e7d10417e63e80fbe`  
		Last Modified: Tue, 12 Jul 2022 02:59:04 GMT  
		Size: 10.7 MB (10655984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:62699f36e296ebf4c43cbb6b2af63874698e02388c914239c012320b78470bdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71859543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2355d79e2f3fc2f5009bf9c18c05bf8b2f8ecf2e2b0078c1fd7b711ca9e13132`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jul 2022 00:46:07 GMT
ADD file:160fd6ac1dd96abed2e1719ac95e75e8a8eeaeef9e04a353e0ba4a23cbd1c1e4 in / 
# Tue, 12 Jul 2022 00:46:14 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 02:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 02:45:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a4ac3f896d9c36c21fdbee9a7ab2637136d4d09ef6db30c3b2b4ab10c48abbe7`  
		Last Modified: Tue, 12 Jul 2022 00:55:11 GMT  
		Size: 51.8 MB (51757401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7d0c4835633a8b04da06d28abb8af4b5557ef25b136337b6872fd92b710b70`  
		Last Modified: Tue, 12 Jul 2022 02:55:25 GMT  
		Size: 8.9 MB (8939218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deabdcf7f5d4d109945eb55d7a1fda36ddcf55c65eaff794d0456ee0e0e2e30f`  
		Last Modified: Tue, 12 Jul 2022 02:55:25 GMT  
		Size: 11.2 MB (11162924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
