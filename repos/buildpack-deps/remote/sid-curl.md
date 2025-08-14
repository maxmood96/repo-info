## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:4a84b3cfef18f312f1a154218eb104ef76430994b842ab414d5cbef4275548dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4322206bb7360279efbcfc57da75a1cb672b25c2ceb220d2a573e7996935aaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74982769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c84e584780be633ac2625d9dfe74f9197196b84e0bab3aadd19ea96d8dcfa1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:91617643e569834fa54ae3c641bfe51cb7c336b5d4c84459fe06ad34797a9b56`  
		Last Modified: Tue, 12 Aug 2025 20:45:04 GMT  
		Size: 49.3 MB (49311006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6147febc7eaaf987437ba1cec086fc417009e9ea749cf4a8e05425f6ae2ecd`  
		Last Modified: Tue, 12 Aug 2025 21:22:06 GMT  
		Size: 25.7 MB (25671763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ec334cd8db1978f446fc34f0e404b45f9a260a487a3732c514639e7d6cea318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1b283d2cd460c99cb502be8736fae5ea7d410301ccb617bcbef79fc8b4d3c6`

```dockerfile
```

-	Layers:
	-	`sha256:d5686fc1761a3a1e378ffb5e4ac7b5984e9ed7c728c5d9effa33d6913e56108d`  
		Last Modified: Wed, 13 Aug 2025 01:22:17 GMT  
		Size: 4.1 MB (4112392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b252d2cc1fb5699c91cc59e5a61258d8987e298e03977dc5aeebcfb9b56e7291`  
		Last Modified: Wed, 13 Aug 2025 01:22:18 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1e29440fab312d6f0935441fae3375f2975d8f21ebded5079f04dfb78f59433e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71890434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595f04fd3abbe54493f750de44795573fcdf8c84bf92408ec88fea3eb9b977c9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5748e2c98ab94a513cbe6704d8aa158304698c52babb6c14538afdc0d2da4d79`  
		Last Modified: Tue, 12 Aug 2025 20:46:52 GMT  
		Size: 47.5 MB (47481153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8674f20f211a0a5df7e43fa4413500efffe4f69e9a5f53119c86c35ab3bfc85a`  
		Last Modified: Wed, 13 Aug 2025 00:00:46 GMT  
		Size: 24.4 MB (24409281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c5b4c3be95a0d187cf3db7613b4e578fb477afc8ec95ea7e9fedbda3599fc127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffb67654efe0019f10f56d2797001e10841b483268c0f50fdcf4bf141973441`

```dockerfile
```

-	Layers:
	-	`sha256:3d17510b4caa8af88175d21ac1eb88c8aea87b9b927f30886f0f7e25d8f11792`  
		Last Modified: Wed, 13 Aug 2025 01:22:23 GMT  
		Size: 4.1 MB (4115391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f9653c1dac2ee2fd469d12cdb0604d682d8ee41c80ad8366740b9a32f7e136f`  
		Last Modified: Wed, 13 Aug 2025 01:22:24 GMT  
		Size: 6.9 KB (6863 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1a9fc59ee9e00c351be838e9aed89550188c9b3729a1996d7c0be41dce084d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69425485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d78e03c86ac0e8f870aeae773088c03e2d4b68b8268078105037550eaa245a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51c05ed00e703a3cf5143ee59e5e4f274a1b80aa10078d7b24eafce226544dde`  
		Last Modified: Tue, 12 Aug 2025 20:49:45 GMT  
		Size: 45.7 MB (45743292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f4c6e871209c22d9147d58afa57aceed37d2c4246961ef6f33220a727e664c`  
		Last Modified: Wed, 13 Aug 2025 00:16:33 GMT  
		Size: 23.7 MB (23682193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b972a3d0b9f5fe6e68038b316fcaf81311d79586c2f1731a701ececbcc7b257e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa414e20b446dc4cd8f4e4e4f7303c9f64ccaa4ef1ad808cb1c9af65e4c4f40`

```dockerfile
```

-	Layers:
	-	`sha256:f3a06805eb1747131d2c714b99a08387c15099afb245e18774ed9f7ef58e5ff9`  
		Last Modified: Wed, 13 Aug 2025 01:22:29 GMT  
		Size: 4.1 MB (4113885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbab2347605ff2ff9f88ce8b9d5377546823747b8326f2d943da185d6a4898f6`  
		Last Modified: Wed, 13 Aug 2025 01:22:30 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76f7c18fc09ab9bee95758959ac3afadc6c5534acaa724b89854eec024f663af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7d6f9d0af6c9fd9f8de01cf64951aecdc6c41c9b84daaa308986ae8ecc0a4f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:406c75c505cd140952825ea55560dd596c3ac81bd28e8acd75409de77c63efed`  
		Last Modified: Tue, 12 Aug 2025 22:10:46 GMT  
		Size: 49.7 MB (49665758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42948f27bd259c3af4df8bb9642f9b13a961850fc18b0d0d704e4d8bd4184ce`  
		Last Modified: Wed, 13 Aug 2025 06:44:51 GMT  
		Size: 25.1 MB (25094159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ea29ec4516a414694edece1b6c12b0ba385623f1bd25080bf18cda8279bae09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a9c309453cb10ecf86c6a1a5eb3ff6eb3cb4fd5e52aac5a5c2913e7ed88645`

```dockerfile
```

-	Layers:
	-	`sha256:813ce8c337e2667e4f0e8dc190720f005d092f9fac5d7ec646ad4e92c3be5fb1`  
		Last Modified: Wed, 13 Aug 2025 07:21:16 GMT  
		Size: 4.1 MB (4113922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6d09493031c47ef20f1d15e9ca5254c7059dac9ce119e461a17dc2f6d3e13ae`  
		Last Modified: Wed, 13 Aug 2025 07:21:17 GMT  
		Size: 6.9 KB (6883 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9f32212a52f1b09a67c11516990b4816dde19da269943702084bae831bc377ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77656455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd68390faaaa4f39f2712c59f8409c65719092b9ef270ea9bbd10c07af724f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b72ff759cae89a47c9827cbc3981a075f421742ace3eaf0d3c40f8d242d2eda8`  
		Last Modified: Tue, 12 Aug 2025 20:45:13 GMT  
		Size: 50.8 MB (50819082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3bb2ee090cfdfaa39c0d6ccc1bcda36a80f4080c6cc16e7b75c64cf990c8bf`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26837373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b2f019cac2ecf39eb3f28186c263271b0483bd4b1d1d0b861dc57add8df9320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1443b0547e71b74367a1073ada23cfc087b5b58e57985e6c2dafdd62cfc47646`

```dockerfile
```

-	Layers:
	-	`sha256:75ccdeed73ec8dfa83819c973485e7f1c7db6bf8e2bb7867b63311b27227ccd6`  
		Last Modified: Tue, 12 Aug 2025 22:21:04 GMT  
		Size: 4.1 MB (4109511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72879bceaf668cd8a30bffa92738b2caec4ee1776909fedd8aca2580a2618db3`  
		Last Modified: Tue, 12 Aug 2025 22:21:05 GMT  
		Size: 6.8 KB (6781 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:792c658776779e639c8c5d2e759f62bfc2f116241832afe4f1b78217aa3fd7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78097808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0ed6a3a23fd00a8c203b6f9316d382d5bb3b1319738f9a099b3df8f44a9df6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5da413a3f50eb44f07bba0eecd786bf3efd93a4ca4c52ba8109a9b9ba14e688b`  
		Last Modified: Tue, 12 Aug 2025 21:13:15 GMT  
		Size: 49.6 MB (49562283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3d257b869b2a60078b7a65964ab94a9b367c5ab49593e2c17c1f7845cf6eb2`  
		Last Modified: Wed, 13 Aug 2025 06:40:49 GMT  
		Size: 28.5 MB (28535525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5f8ece5fb0bc4cc7553ad04de6288f130827d4954508a01a0f6f077057db9e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c64783547b54a226b1d912e712c6ee812c6fb184235a2939e8788a6372d263`

```dockerfile
```

-	Layers:
	-	`sha256:ecd03ea8089aa9dc7ca02b304c16da4bd884f6a16b75e6a15aa216e7c347a9e8`  
		Last Modified: Wed, 13 Aug 2025 07:21:24 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3d8b97ffd3f4c22a63f6ea98f3b5607e6eea9993815b25a89450339a5fa25e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80217002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ae0a4039f8a43ca2a83956e13a7aaff098c65c3b3841082164b28d86dd6657`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ae7a451fcc7e9bebf7ef51b031f5ec2600e7c017efb66e1de76397538aff917`  
		Last Modified: Tue, 12 Aug 2025 23:09:05 GMT  
		Size: 53.1 MB (53147748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48ea27c6408465e04631c45f46084191d49262124cafc6550f5e911abd6374`  
		Last Modified: Wed, 13 Aug 2025 12:14:50 GMT  
		Size: 27.1 MB (27069254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64e15c05acbe1de51039a5bfcb25ac72a1f7a0b179790765258fe19353ec70d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a134817a688da9db48ba038230fa67bc0c78990f69db802329714a201cd186`

```dockerfile
```

-	Layers:
	-	`sha256:6e2411b3ee2bf110bed1660766deab484d3fbcbf9974a5460a284cd03e8fca09`  
		Last Modified: Wed, 13 Aug 2025 13:21:36 GMT  
		Size: 4.1 MB (4116220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:359c1fe635be880d9f83899169ac8a8ff09117cf48a18fc0dc22c94887d01c78`  
		Last Modified: Wed, 13 Aug 2025 13:21:37 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:447940fa7bbf5230bc339aae8a40c39838ae959d7852061b8d2c4e2d9a6a0ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72820250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536d174447e56f3b2f8485a454e6937a772886d8fc9e46eb370e4b30450ccfb9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a9e91ea2edc2d111f6a67eba934b0ebded0b74c51de6a807b73d07cbf965e132`  
		Last Modified: Wed, 13 Aug 2025 01:03:20 GMT  
		Size: 47.8 MB (47776559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64af9f489cd1777e5b300ee5ecaa1ee0eb257910fbeea3b4885aa18546f4677f`  
		Last Modified: Thu, 14 Aug 2025 14:45:40 GMT  
		Size: 25.0 MB (25043691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d4b677973b25f866ca40a16b3a098d7534dee03b9eb3b4df07b596347e14d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:261608d6844cf4ea00520a67550d368943904d343b091a4ff7929221ef96e84a`

```dockerfile
```

-	Layers:
	-	`sha256:5888bb9986b42b8e73e10f191990d251a0014c33e068eb6552e09fa48e3ae50a`  
		Last Modified: Thu, 14 Aug 2025 16:20:46 GMT  
		Size: 4.1 MB (4104826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c76f90bec4cb9cc774b5e07ca51dda6877899e45683fd5addaf57ef9a94f85c1`  
		Last Modified: Thu, 14 Aug 2025 16:20:47 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c383f2e609956c30ee4ea0368a9de9f2a250ada914fef4f4052c3ffd53a31ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79373991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3029bcb85bd540a7de08375df7608f36422a0fca850b9497b3246a717b239a86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1754870400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4959d43b6e4e3bb883ad4324fbf3d2d46fc88486af520d990c753fc3a7ba0062`  
		Last Modified: Tue, 12 Aug 2025 20:56:23 GMT  
		Size: 49.4 MB (49380676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9f068820d21f743fb7a4899ffdac4cbb3c9018377c7ccd9ea60dfaa661d90`  
		Last Modified: Wed, 13 Aug 2025 11:02:14 GMT  
		Size: 30.0 MB (29993315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:239cef95408a40994d1d96b1a486418f5b23148ebf9fa19178d0c9053d9292e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d481c5b84fb79e4f4a64c902e5a650ae70b47fb89804a0f609a9cb8bebae777b`

```dockerfile
```

-	Layers:
	-	`sha256:a13aa6a6930536cd344c49672b2092a5fc7c43568815ea82ed859223f578ea24`  
		Last Modified: Wed, 13 Aug 2025 10:20:48 GMT  
		Size: 4.1 MB (4113802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2ea1577d7c6eada5d4b7fe9f05a719b7d76f24569443ac2e3359c4ddc6d8059`  
		Last Modified: Wed, 13 Aug 2025 10:20:48 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json
