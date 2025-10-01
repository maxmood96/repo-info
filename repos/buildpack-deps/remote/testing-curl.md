## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:1e2cd7dc73239c8c71d5fe4d6550872fa633e9d587fe3e1f762ddb7314c01011
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
$ docker pull buildpack-deps@sha256:e0593d850eb9b18f6a49106c47b1826264b30104e5a7f6944dde2d06b254feb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69608006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d446a034d66d0d80f3b6d105737f17f57e2792ff8f5aec795d94af19e73ef07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:37213742d2f58ba09fd9f68c8a57d0aed21f04fbd865207a40734ff3e6e7a8c6`  
		Last Modified: Mon, 08 Sep 2025 21:14:40 GMT  
		Size: 45.9 MB (45943220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86adee590a893d066c841440cd9d1bbc41753c40fc6a723dd85c4ca79b9b96`  
		Last Modified: Tue, 09 Sep 2025 03:20:59 GMT  
		Size: 23.7 MB (23664786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:523ae429277c6dee71206d174405fa89c110cfdba440b914dde9142bc1230718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4124104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2132b5a5c177e7b11957f4a72b5584dddceb4e192016db12e7696989c8cfb5e`

```dockerfile
```

-	Layers:
	-	`sha256:0df8cc22529b2bd0848f1c5afd244d46ef7f28adad2affeb80bb9b9ccfd4427a`  
		Last Modified: Mon, 08 Sep 2025 22:20:42 GMT  
		Size: 4.1 MB (4117224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13d5e73ba4a9d0980081ceae64b162a9dc93a33b11a7a95ebf936d0550f842c`  
		Last Modified: Mon, 08 Sep 2025 22:20:44 GMT  
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
$ docker pull buildpack-deps@sha256:3b8fb394ef56aea0fc0a41e806f6aa5cf8773ab6f2e76ddd6e9c07658dd1b41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80446335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee74d44125d77d18a11c807d2409b503f683c1a1fe255e442b3aa49894ea121`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4e4a2bdd2295cd2a4f3315805533676c7f12dc54b360ff3c285c5614051d45d`  
		Last Modified: Tue, 09 Sep 2025 02:16:14 GMT  
		Size: 53.4 MB (53391698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a918fedc73bd98652f37087b2219a9384ea0986c8affd0a0d0679091c621a`  
		Last Modified: Tue, 09 Sep 2025 02:16:10 GMT  
		Size: 27.1 MB (27054637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8a99a9322b768f8658b97ee5ccee8bae24411236c4d51d98e60f2d5f5901b7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4126407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ada6d5dfd121b0e6151f86a9fc6d808518069072f31be8ee3896a03a3bb02eb`

```dockerfile
```

-	Layers:
	-	`sha256:f7942aaddcbdd846d173518068b6f370c6fde99174a3fe6480599a9db2340563`  
		Last Modified: Tue, 09 Sep 2025 04:20:39 GMT  
		Size: 4.1 MB (4119559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4045a737a20ea7584db190470b8e5858ee8dad6113bb980d72ba289692ee0965`  
		Last Modified: Tue, 09 Sep 2025 04:20:39 GMT  
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
$ docker pull buildpack-deps@sha256:369663a4a86ff7dde775a1d079b3238e49e5387302eb35de52d41c37c326342d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76423478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b82d31bd011477f016d922c3aa233411605019c584520f39592627e9c9c84e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1757289600'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d70c4639b1bb56ca2bfa88a8dedfb6d14d5f6a857613b672fef601229bcd766f`  
		Last Modified: Tue, 09 Sep 2025 10:20:05 GMT  
		Size: 49.6 MB (49583182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23441d4a53386d92d68dfd117aef1e221cdf7c5c29e7c8841eb200ce14f89465`  
		Last Modified: Tue, 09 Sep 2025 10:20:02 GMT  
		Size: 26.8 MB (26840296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ee1dd52099591e1e0a4612e9a94d48b0c476c295aa077b2b2b721f55ebedbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3556799c2c943627d5b7f5590eb261059132dc33cec64bf79467505daad83a6a`

```dockerfile
```

-	Layers:
	-	`sha256:e840a8df0af811cb1f89c5e0fd197a281196065630b27e47a44c166694a055f7`  
		Last Modified: Tue, 09 Sep 2025 01:20:47 GMT  
		Size: 4.1 MB (4117141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a74d2945c6b2ddae9994e7f720b1b9ff74140d80b118f4d2b6a31c0678f9d2a`  
		Last Modified: Tue, 09 Sep 2025 01:20:48 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json
