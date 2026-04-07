## `debian:testing-backports`

```console
$ docker pull debian@sha256:0ad889acc1e7c3235c42af65afdf38425d5b496e9d689b743d9b3fff72b3c7d9
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
$ docker pull debian@sha256:59f6ef3303fa693606c3686d9ff057ee53ddf5409581d569a4c25c97b8e7b5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48587308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342d17f6847c41e04c61dd90eae273d99ac398867ce6da1c2d222e9936bc1204`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:16:55 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:22b89b881e9d5422fc9da3425719efd67131de7d79df86578efa8c704089ea0a`  
		Last Modified: Tue, 07 Apr 2026 00:12:02 GMT  
		Size: 48.6 MB (48587086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11f2863caddd5de73e2f13601360130e58c0d572ffd6207d80086bfdad708cf`  
		Last Modified: Tue, 07 Apr 2026 01:17:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cb8c0c06e92e885dc6f5124965e554043b9ebfe40f64ebedad2bc8a939c40673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5020b1650fdb212c723c010e0139aa1f61c8d909eca08d5a17f799a9cc3a458`

```dockerfile
```

-	Layers:
	-	`sha256:f3e9c38113a4baed3d0c552d67fd00dac50d00a3bc4f73ac5cf455f1580a2989`  
		Last Modified: Tue, 07 Apr 2026 01:17:02 GMT  
		Size: 3.1 MB (3143292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf291a259b4adb87750ebe64d2c49caf3e361bc0d52a054d7ef489690092176`  
		Last Modified: Tue, 07 Apr 2026 01:17:01 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:a856e9ec230e3890b3fc78006ca428530763e3899e98c0cffef7dad4f3a305a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45541012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4172b089624119e2348ec2365d13f35bb67f5535ff05ce253fb2f860e5a23623`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:15:34 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:402bd1ff708e9d322bc9f206ecf7f5640762f978a64656cfb24d9af98d044c29`  
		Last Modified: Tue, 07 Apr 2026 01:00:00 GMT  
		Size: 45.5 MB (45540790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b29091329d84bc370017cfb878810488e60fbac18809b46f67a3ae6f9d4869`  
		Last Modified: Tue, 07 Apr 2026 01:15:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5e67d34e69d13455aacb4d5cc32ffdf41f676e0c9476dfee21589cb430e16dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6088de6f725f831d5220f3738a08d30f31216a2e6c0be3ed332aafe9a28c75e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6b7872805381465f97b07958440a149d2885e3cdfae92fc7ebd0ff1b4fd3ed`  
		Last Modified: Tue, 07 Apr 2026 01:15:40 GMT  
		Size: 3.1 MB (3144654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5943da708fd1ad98eff9e09c6522b6ad1045d54e7e99c431f0f9f70f0e01f75c`  
		Last Modified: Tue, 07 Apr 2026 01:15:40 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:8cbf5fdde6d94c6779b3b2997679a771c5753b0c3a535162eea1cefe5e60e55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48643580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0855c4222bb5727257feb3d87583e16a6ffa7963e1b3a9b9c7f64ed9eaec56`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:15:30 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:270e6fb5e8158c645c59da5292196f6d4ac5d2b940fb597c6b350535305ec493`  
		Last Modified: Tue, 07 Apr 2026 00:11:14 GMT  
		Size: 48.6 MB (48643357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0ae5bc718713e3ddd6418726b29f90155b4e5019b06693418df0752581d240`  
		Last Modified: Tue, 07 Apr 2026 01:15:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aa6c1ef8a63952e6179c7bfb25a774c8e33609bf9b481c229a3f301b7ba2beb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1092a3037fba76fb547f0e8ade2f8383218eb1d0dc1bfa58dedd2f20cd4066`

```dockerfile
```

-	Layers:
	-	`sha256:444a1c640ff0040a8e3f51c06b7b3cd746fd471b07d3f53e7af7565d17dcfd05`  
		Last Modified: Tue, 07 Apr 2026 01:15:37 GMT  
		Size: 3.1 MB (3149242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b35e0b36b8aa2946424d2f162315e7eaa571b0ef50236518d20571d4197c064e`  
		Last Modified: Tue, 07 Apr 2026 01:15:36 GMT  
		Size: 5.9 KB (5862 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:39d8bf172c425dcc098b292d7d9aea1230201a09d84aadeb5e0852e8614db68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49878613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f5e26f62a39e271cbd886b3cb52dc63ff55419923e78d411514a566c27f090`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:16:25 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6eea2c150e45b48e6aac55b6b9fe2828344605d677e78392dcced9a0643b00c0`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.9 MB (49878391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0af44ff0c37b24533ddc3680681a4407112cff18745125141fcb7f5d7a311d3`  
		Last Modified: Tue, 07 Apr 2026 01:16:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aca2f071690b90941b9fd84fdab9083039d71950f4881686c5fca1f454700f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e421caebb302d1d610e16519c36965a6f95e5a586fe050d5f6c06f4d119a059e`

```dockerfile
```

-	Layers:
	-	`sha256:1a19c32caa0972d596a80e02e0ba2ab1708db346cbd753c2408a10f10938f187`  
		Last Modified: Tue, 07 Apr 2026 01:16:31 GMT  
		Size: 3.1 MB (3140495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d5cc3c0e631d0ebe1d7b16af2933bbd1b6d6ac05c3f1fc0209863d986da650`  
		Last Modified: Tue, 07 Apr 2026 01:16:31 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f74ddac092aee8366abad8f9e50f7b9befd116df714cbdcc2c9012360f31dd9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53851461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b6cbb13a38ff021a13114d5e029b6cc8025bad06c58f233e07cbecab09ff0e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:17:02 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d2fff16aab3eb8d89b3bdbae0814c0146f162ecacdf526ba2f4a1dfd7b082ae6`  
		Last Modified: Tue, 07 Apr 2026 00:12:16 GMT  
		Size: 53.9 MB (53851239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eec16355a620fc29538fdae66067c2a42731baba813be99fc370d1379b0f31f`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ec257f422a0b4f040a5c03a47648890b1263e838ae9a709ef4be6c9e52475fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6844111d413c26191158db64605ec30c27f00a83f465507670bb38cedaa172`

```dockerfile
```

-	Layers:
	-	`sha256:ee793b0c90d98b0f266cee829c8d8acd8f73a3796f07bf0ecf2d85bae792c422`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 3.1 MB (3146791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12c5c8007c5911b24992bea510a9bd633453e823982b515d28fe5a2b5573eef`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:c8ffaf1112fdc6edb29f7f5b188c6c79c425212e198501dcebd316f172191368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46698399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e78b6227805a7aba0a3f491657c293d75c89feaf32932bb71dd9b7b09c59531`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 02:31:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ce74530515a7a4f9505ef6d9ea54663fe989f89d07d1fe1d890c7d24b8d28e4`  
		Last Modified: Tue, 07 Apr 2026 01:50:43 GMT  
		Size: 46.7 MB (46698177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d09bada4a845c5b04d63c27e3afd3887222a2790ca59d1c44be0ec740cd5806`  
		Last Modified: Tue, 07 Apr 2026 02:32:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b2983b23970c7b5d661aef6944aefc0600e4f949d4856768e51aa5d697055413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01865fed0a033c2e8302f3e7b2542250a8768290f5b6f896c4742d5551994929`

```dockerfile
```

-	Layers:
	-	`sha256:0469063934b8bd2dcbfb2b731656e5f67749743097d8a5c549d2939bec68f161`  
		Last Modified: Tue, 07 Apr 2026 02:32:02 GMT  
		Size: 3.1 MB (3134794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0810172bbc23e6dadc957112b2f331d14690d9e449f2d262daf165b93ddc12e5`  
		Last Modified: Tue, 07 Apr 2026 02:32:01 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:a024ce698caaee282a6da5ceec5bf9c911e9a20992353b6368de9643d4f673f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48291818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f405e43815aec27f8e8ddf01877d857ee4952d6d66c69ac003b0b9e64c85ee6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1775433600'
# Tue, 07 Apr 2026 01:17:10 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:06fdbadcb6481afb3ff06f57eb876e2c2622ce9f86876789a8dfa6db27908938`  
		Last Modified: Tue, 07 Apr 2026 00:13:02 GMT  
		Size: 48.3 MB (48291597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e4ffa698efc2cd010e52f0201cd5563505f1e0e5008e2a42ec368f4be7e290`  
		Last Modified: Tue, 07 Apr 2026 01:17:27 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:101334df051e5838f91ddc75f1c446e6485769f440c9ac636f396290bee8b6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1397106ddb932735e3423f0c7f4d3ab59001d510b065e8d6c0bfa43ea1ea22`

```dockerfile
```

-	Layers:
	-	`sha256:7bf314237a809c7d0a65b1bafc4e30ccc4f8c641508592811ffea3685fc67c6a`  
		Last Modified: Tue, 07 Apr 2026 01:17:27 GMT  
		Size: 3.1 MB (3144743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4e3068e1930675bf015f9409d442b64178f12c9b3c52a039ed6a4398c7ba71b`  
		Last Modified: Tue, 07 Apr 2026 01:17:27 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
