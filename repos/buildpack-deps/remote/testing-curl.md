## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:8130f4d8d0e56847773ebbe6877ca682d7c627524d44d073b994adb3fa3a0660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1e3f2c1cc5a22cb3a741d697018cda56c9378c0ef6ea8f8efc710ac8fefb9e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75588657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e431997ca64e3aa1057e63456ee76b7ff798a76535c3bbf7e5646b7c82c126db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075219ece41f099ca8ada652efeda87c6ef755098af129d14764aea953222807`  
		Last Modified: Tue, 30 Sep 2025 03:17:10 GMT  
		Size: 25.9 MB (25851839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28708a4c5ccc0aa1f288a1445bb0e1f3688afb3f16e2c0c6ed981a4f5b2a19b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bed7fa224421ef95b3d928e2c95e57b4edf097434604cd02e59e22747e9f49`

```dockerfile
```

-	Layers:
	-	`sha256:5f9289cb52afd2f183b91e9c0a7e801755120a6118713c9eaf07693f0f3828c0`  
		Last Modified: Tue, 30 Sep 2025 22:35:28 GMT  
		Size: 4.1 MB (4108640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97a9cec3b2c7100495ecf60d80e50fdeb5655778f988e5f51f05abfb2900b1a3`  
		Last Modified: Tue, 30 Sep 2025 22:35:28 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0004003dfd299b8e10b916032781eb750cbdc1800d16bff4802a029a3731245c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69774683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff5c395ff601a8fe1159c9a6a1b2bf2bc5b2372b09f15bfc26aeda0df4f1c38`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43934bcb3ccabc44fd5dd6a6383f81957a551493c079cc1ab7f71f687b26a8cb`  
		Last Modified: Mon, 29 Sep 2025 23:34:21 GMT  
		Size: 46.0 MB (46020847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c128e1aa14ec2c1ed27b97b88786e99053986c4d3e241f522a65c9ca20a3c3`  
		Last Modified: Tue, 30 Sep 2025 01:07:25 GMT  
		Size: 23.8 MB (23753836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:53b6f2c1c104a00a95c3fe164535f7f70a2e19b2bd87113436bdf404263efe0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dcd229b2cb11a7f74affc0d55c1d522b181421478cda82809170efdc9d52ca`

```dockerfile
```

-	Layers:
	-	`sha256:cfa4fe3c9989a073f61c26cebc5cde589386776413b11d412ee7480ad083ef2a`  
		Last Modified: Wed, 01 Oct 2025 22:22:17 GMT  
		Size: 4.1 MB (4110133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3eed0c7c68b6db751cb688e5d71e22a511d214a767e2203abd02cfdb38194ac`  
		Last Modified: Wed, 01 Oct 2025 22:22:18 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee8c7a2bf20ab885826029b7070677f6d71a93a77f1e143021da90d62005897e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75089238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55baf19c754f0d901fa9079c5f77e9db0d0e4d5d8cd8154237ebf7569c57627`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed417fd581c20c18b8c6cfc58498c59128dd74498d5d6a89f9217103a4fbf9d4`  
		Last Modified: Mon, 29 Sep 2025 23:35:24 GMT  
		Size: 49.9 MB (49879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009e42d3323422f2397c63e68313d31e460dfa892d093803cd931e5199733e2`  
		Last Modified: Tue, 30 Sep 2025 01:18:56 GMT  
		Size: 25.2 MB (25209361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:01fa46658e7d109fd48fc45182c257a2ce33fefd88fc980b5ef5b5d7d3b15bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73d6652462ec97979d7bf6b258ec7a635db62c1ad67fcbc7a688b473a0f9895`

```dockerfile
```

-	Layers:
	-	`sha256:64d1c017e8c1d2d0a27b59bcc8baedd98a2a7b2d6580ca6b616dcc77c24afdfe`  
		Last Modified: Tue, 30 Sep 2025 13:23:44 GMT  
		Size: 4.1 MB (4110170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6883879cf67323ce477f91afa1bd7e0aa73f4108e5aee837690959a0cd3bd52`  
		Last Modified: Tue, 30 Sep 2025 13:23:45 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:83d3fd2fb2469a6818480930c26f371c3bd0dcd9de23a90f60a7ff31b9499c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78015856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d3525a9f6fefed373050e73609b49398e3f77f0c73248fb623db182b524789`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccf114b881a561e278525714169b788115fe512463f3cf36ea76912c59a87cb`  
		Last Modified: Tue, 30 Sep 2025 01:18:44 GMT  
		Size: 26.9 MB (26896436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30590b965c948e94a4b0bcdac791d52e9f8ef2b27e81ff2dabfee33c5863e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be51f2450625b1dffaca6d4815e47d0290a7813b880cca1b6ebdcc16ac8a415e`

```dockerfile
```

-	Layers:
	-	`sha256:c89c9190d4cb327738e9a052349d4b8c89c0505324c203c0185e60cbf228ce11`  
		Last Modified: Tue, 30 Sep 2025 16:36:49 GMT  
		Size: 4.1 MB (4105761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc520e0ad8f3cb827296679038fe01c50b01cdc9402345f26bb34c9039ed74f5`  
		Last Modified: Tue, 30 Sep 2025 16:36:50 GMT  
		Size: 6.8 KB (6794 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:86e4ae38abe8160767f6f4f60217328e08c08bf575f4963e65eb8b641f7726a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81946076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c84b84e9172bdbfbf8b2575ba67be830357edd89d5e501279d70bc68cbabec7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c998caf3e9e3602596b17377df87ed145d1ff51c75338d4bead32fdc1773c859`  
		Last Modified: Mon, 29 Sep 2025 23:35:22 GMT  
		Size: 54.8 MB (54750879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9457c9822c8c6d2c9e044696c2965d09ada732a8ed5c4fd9aae6bb4d5485465f`  
		Last Modified: Tue, 30 Sep 2025 02:26:32 GMT  
		Size: 27.2 MB (27195197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e781b023bc9a42d2d18f33fcea446b62874d0a137ea4efba17c85b9e368fd193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6eca9bec51c5378958860976d1dfaf97207c301001664e04c34af890e41ce77`

```dockerfile
```

-	Layers:
	-	`sha256:374df6aac6f6e5f80eacfdd4d5747141f716a26f48bbdbba8a4063fba83364f3`  
		Last Modified: Wed, 01 Oct 2025 22:22:01 GMT  
		Size: 4.1 MB (4112464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:730feadb90a0ad52c50695f26571473fc84e52a4d51a514804f6c81f73e1fd30`  
		Last Modified: Wed, 01 Oct 2025 22:22:02 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c6c890a28cfbf6bb141a7d3b7767297fa2569751e95259fd977f0960f7536d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73079370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e547bd59735276ba70b974a538af6576b02153ebfc9032a152f139e2df7f3936`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:db7be57cb42d3da83b1f69e7698442aa575eac43cfb6c579690c32c4f1cc1c22`  
		Last Modified: Tue, 30 Sep 2025 00:49:36 GMT  
		Size: 48.0 MB (47970093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d1cecefcb8fd1e3777e94b0c79bf25f44457085d008c5a4fee32d8fdc9d9af`  
		Last Modified: Wed, 01 Oct 2025 10:49:03 GMT  
		Size: 25.1 MB (25109277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0caf99240ecb8511816c0cb8ba2505124729315f27c52f93b60f8f7d41a3bf2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef5c2ab2c2189a1d6d3ef3022ae21ce50b37acc394aa16f984bac648d8a8e13`

```dockerfile
```

-	Layers:
	-	`sha256:0519aeb0c3afb7b1f3d2f206bb004df062b7bcd8fcc26d651b1594bbdbd0a7fb`  
		Last Modified: Wed, 01 Oct 2025 19:20:09 GMT  
		Size: 4.1 MB (4101118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1c905aabb2b922ae5c4df741725b9350a0d891b4d3678815f51e836689e99f`  
		Last Modified: Wed, 01 Oct 2025 19:20:09 GMT  
		Size: 6.8 KB (6848 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d8d366e9147e1e5a0c8ad0f6285b47f1270055e6d74e4aaf0d0e187cc9f55dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76563145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbd3dcb821082c569edf61798e02d2181a36e8641edee9e13ff57a362f5603a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1759104000'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f12f0b09af6c73f5ac02ec4057426f99780ba4cc2b7ffa5da8754ce19dc3c40d`  
		Last Modified: Mon, 29 Sep 2025 23:35:21 GMT  
		Size: 49.6 MB (49576014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cd2fa0437cfacaf00281ef1e68d7f757d4929c7cd7fef87c86f4fd3b95f9df`  
		Last Modified: Thu, 02 Oct 2025 00:43:13 GMT  
		Size: 27.0 MB (26987131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1b86fdd2eb8a4748e51b9520347ac0424fd204897fa4ea9636d87c23f45ced5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681fd987bbf59eb0a36b130e2869a34725b484873519b84fb0fa4721876acb50`

```dockerfile
```

-	Layers:
	-	`sha256:fc7c5ab5a99ea7c681f955bdf56a9f3e72d2e91f66209941474d41afb9825627`  
		Last Modified: Wed, 01 Oct 2025 01:29:32 GMT  
		Size: 4.1 MB (4110050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97f9a40f0dcde98a2bee11676195c0712c840fd4f1517f38006fd81cb4b794f`  
		Last Modified: Wed, 01 Oct 2025 01:29:33 GMT  
		Size: 6.8 KB (6815 bytes)  
		MIME: application/vnd.in-toto+json
