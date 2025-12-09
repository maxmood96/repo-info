## `debian:testing-backports`

```console
$ docker pull debian@sha256:01cfd3b98165316d3d3d2e7d2e32a0c49b3288b5d335dff9c395012006509808
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e033aeb3bec2ef70afcd2f9a41e41cc6c8b7ad0e53fcaaaa832af62ad2cdf273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48512735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce35606212ec50cbabbab718a99b619df079d267da66a584339ab20d7c23974`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:29:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d07e7493d30660e90d785732f6efa7dbc2cb9ffe13064e2383c3338b574466d9`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 48.5 MB (48512513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8eace65448f51a7986120eac444b1d6abc73ed206877cde6f11f831c7fd238a`  
		Last Modified: Mon, 08 Dec 2025 22:29:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:636f5794fffb4c3c3afdd2adc577fb509544cc7201bd790fa15f0e85b66313f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3139399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c85138143947fad6cbf8f461c28a54bc29bd67d1a361acbe7aadc34d6e3210`

```dockerfile
```

-	Layers:
	-	`sha256:2291711230ef809336e68db2cfa4e2274ef720b759b76dd95ddc5f461ef6abff`  
		Last Modified: Tue, 09 Dec 2025 01:31:25 GMT  
		Size: 3.1 MB (3133605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a0e2c163b8a55a23bdb09fd482931bac8d251f013c2442195ba1a912736735`  
		Last Modified: Tue, 09 Dec 2025 01:31:26 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:17448dd056f9f810fa5765d1fc3f0cd6a1754b8514cdcc6ef02978d3cb879803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45048266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577a7de4db214b76c31e716f6e096fe687067ba57991ed44805d5b5e09efc4ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:32:45 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:91b533abf4656d434dc53008257ce01cf32442eea1b3e818bc77f00130717fb9`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.0 MB (45048043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42fd7a3c6696d9c9e82a1388189ef6dac5400e0950d8c262f11b20f6ab19357`  
		Last Modified: Mon, 08 Dec 2025 22:32:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3e26936b0e5fc5bad5a0bb1e68f13d6eee69f0e6157f9cff0742206351db331e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f213da437599fb6cc0cffe5f8eda339fa121d675bea8162d8f4424c17ea3338`

```dockerfile
```

-	Layers:
	-	`sha256:842e0ae42b06e606e730dfc894527cf8e7afa8401a732bdd1d9a26e547339a2d`  
		Last Modified: Tue, 09 Dec 2025 01:31:30 GMT  
		Size: 3.1 MB (3134973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ed47b5bb489388758aed7050e949da5f82128c196c23008481e984529fd465`  
		Last Modified: Tue, 09 Dec 2025 01:31:31 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3492e5696c3231ae33f5937caa4eb3eee728e25c01de892ecaf02aac20aaa0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48599561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26f9745ad2ed1cbd482f9fa6431360e9dfca16913b1e88844cf7bfd6dfa01e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:32:42 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:980892eaed7a52ea486458964bd611659e21bc061abbc845e2c0e0044e32f492`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 48.6 MB (48599339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053f741c3f007f59d8fde0b4ae5d66e4bd6eecc592c4f91e0805b0a78da84792`  
		Last Modified: Mon, 08 Dec 2025 22:32:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aa4a299f9e05ded3e884cbd830b486839b2a0ebe3ee301c52b9a06faa69131e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7baef659f695bc41e1e7ebee359d61024ba58179871038f5bacef1724f3546d7`

```dockerfile
```

-	Layers:
	-	`sha256:2803bcadbdf95fc150c6c61c3dc8e6f3fa03e4103d3c893917c523498cedde0c`  
		Last Modified: Tue, 09 Dec 2025 01:31:36 GMT  
		Size: 3.1 MB (3134446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c341b07ea6333ecb6a8006feffdb5612f3a3f628c1016951d458fdde71f5a590`  
		Last Modified: Tue, 09 Dec 2025 01:31:37 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:781ed69f704a870f56f36a63c58caffa59442ab079c22dae148df9d75764fb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49874804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4cfd64a03f58d325314d2b49d736144feec4c40923eea3ecdf574aa2a8974d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1765152000'
# Mon, 08 Dec 2025 22:30:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c493222762af604803548557b7f7446193795c2901c28794f84318d3e7ad41e1`  
		Last Modified: Mon, 08 Dec 2025 22:17:00 GMT  
		Size: 49.9 MB (49874582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d659e7e81dfd24736662c7efc83a890bc17e317b1833fc5c10bb9d504fc8fdb4`  
		Last Modified: Mon, 08 Dec 2025 22:30:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ad640dcdc6eb18566ca6b00376c3064dd9443bcd10c0a79f018bfac49a82d402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f6ee7ef8f7253d162d22132ba3ee9c238f9c79d5286bdca52510d415e4bc9d`

```dockerfile
```

-	Layers:
	-	`sha256:88ab5b93a72733f165f7d5de46ddafb520d886d207069589d744b4c3a6c35c15`  
		Last Modified: Tue, 09 Dec 2025 01:31:41 GMT  
		Size: 3.1 MB (3130809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa24ce28be640de9e0f42860f582371548d396b159885a16cbc94dba0e6d1f7`  
		Last Modified: Tue, 09 Dec 2025 01:31:42 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:de698e40afec1fc98bee7356a079b74840504be091ef7e693cb9a1304a544b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53414011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a94ba2b4a0ec020b1aa375668de36931c4851950d2c37dc53b1909517696cdd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1765152000'
# Tue, 09 Dec 2025 12:42:37 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c77c02bf0ec741c5e6279842de5ec989f964c7c81eeb1105d5fbd8ab26246bd0`  
		Last Modified: Tue, 09 Dec 2025 09:18:56 GMT  
		Size: 53.4 MB (53413788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01c0052c41cf15b38d265dc4ee1bf2f75d671bc49329f0aea275caf7e8870ca`  
		Last Modified: Tue, 09 Dec 2025 12:44:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:77dbfbc59483995bb84b2701edc2e6e31c2b1d1bf5a54b6d73c84aa6a7f56ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3142924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd4f87f9fa923a835605177850f619b35ccb1417c4a52b0b8585a425a39a6e4`

```dockerfile
```

-	Layers:
	-	`sha256:f9ab972b07c8d4021bf45fd998533447016f44f40b5f14b39aa828edfac8afe1`  
		Last Modified: Tue, 09 Dec 2025 13:25:05 GMT  
		Size: 3.1 MB (3137104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8283fd3aa7c3944d61c8de7279f88fce72fe4ade52f16eeea1dd4c7b24aafdb`  
		Last Modified: Tue, 09 Dec 2025 13:25:06 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:c827af2dae30ae9dcce9c20dea87e6eb60b29a5c3219d3bf0bc32d16ee99a539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46840579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db56dabc408c7f067c900318991424a408fea84a35c6b21e9b3c6dc56546c83e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1765152000'
# Tue, 09 Dec 2025 03:09:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:50d135a30535a960e01c003234a8ca7dd600d754c005888bb7037b0f3c2128f0`  
		Last Modified: Tue, 09 Dec 2025 02:01:20 GMT  
		Size: 46.8 MB (46840357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216c72af0d94f64eb1d8588162890a2089e8b7e01f0f89c3ad6ffd356e82aafe`  
		Last Modified: Tue, 09 Dec 2025 03:10:00 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:60eb4693ac6d5a060af44d6ea17bf4dad5a019693958055f5e6b53985e32054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3130112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29c8c778c693443887f5ab37aa725850d150004d31653197ad24baf14403a8d`

```dockerfile
```

-	Layers:
	-	`sha256:70732c5f8f08c46318bbdf318a9d70b664cb850b11b0982d051dc2cc4bc327eb`  
		Last Modified: Tue, 09 Dec 2025 13:25:10 GMT  
		Size: 3.1 MB (3124292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3e441887a9dda2d79ad7f0fd66b400b34fafb73b8b9a34d995e25ace5cab7b`  
		Last Modified: Tue, 09 Dec 2025 13:25:11 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:c36d2b4b9f72a84ceeff119e6345f0c5e928109f8e6e2013c47d8f3c444d0471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48320062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399181503ac558a8e562400da4961fc8b6c5f978ad314302db782c14b1485082`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1765152000'
# Tue, 09 Dec 2025 12:10:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6ad4d5a8b1668f11bbabc575605b837454e88e85306364c279679a1eb23d3849`  
		Last Modified: Tue, 09 Dec 2025 11:11:10 GMT  
		Size: 48.3 MB (48319839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6145f6eac8db921a5e06d077ada3121fb8b283e35f197064a301c767bd3794c2`  
		Last Modified: Tue, 09 Dec 2025 12:11:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9bf576d986925f46d2f13444b9cbcd43157b341812af774048d63df1a14ca451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc3ca4340f15816c3f7d7c78cc6129018c5c36c8a47f4d13de8b5c66c78b5b6`

```dockerfile
```

-	Layers:
	-	`sha256:0e1c4437314d381fc2575a97f5367457e3ba190d580441d05f05e358ea5db9fe`  
		Last Modified: Tue, 09 Dec 2025 13:25:14 GMT  
		Size: 3.1 MB (3135054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c383f182e072728dda4c5f948e31c68b5df51d2e2fba195b497aa101708e4a`  
		Last Modified: Tue, 09 Dec 2025 13:25:15 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
