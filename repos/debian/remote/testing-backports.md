## `debian:testing-backports`

```console
$ docker pull debian@sha256:1d28e2a23f8192b1f9f2fa4df397944dd5f662f92cbc114aa723a3ea3125bdcb
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
$ docker pull debian@sha256:9e9baafd1e6ad705cba4a71199966b1027be2b2556502ef8852bd861c239906d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48697871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf87be01880862e44ca00278fcd2d3c081ab489538f5c681816412ad4ed7dbf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:15:31 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:abac6300560e52d30e8863740fd61dd35f371fafec8988cf290ccbea4887753e`  
		Last Modified: Wed, 22 Apr 2026 00:16:46 GMT  
		Size: 48.7 MB (48697649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4305ccf45f13fb635370d2e8dc5453b91c22de16668e7ac35866e2dcb285ab7`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e15922942cee1808a3977bf4c6a0b3e285d241d3239813bd752398c67dde3a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427d871d3b0da4f54b3b0fc947455f6fe396040fdf963d43e84f017154ecae0d`

```dockerfile
```

-	Layers:
	-	`sha256:ad5733b470185f6d1f591ec05a52be2e663fc9f892da1f7877b05c66d535f32e`  
		Last Modified: Wed, 22 Apr 2026 01:15:38 GMT  
		Size: 3.1 MB (3144424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb840412648d860b3d70a55b2db2a0267f1632a2c393bbf3f9f28f4a22e1fc3e`  
		Last Modified: Wed, 22 Apr 2026 01:15:37 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0eed4bb68152ae7cc79a431b53fa1da1166f6a6228a22cb7110c76175a970dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45622355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577d2eb1f338941090e1c14d9ad36cf3cbce4f4c4de17c074dd3ab36b0f0a20b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:15:03 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cc58ca000cbe5f8100a66887fe4a78a7f18408863d4b871783fe724e67a1f289`  
		Last Modified: Wed, 22 Apr 2026 00:17:01 GMT  
		Size: 45.6 MB (45622133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975216c97eb0dfd531bb898bc3e6579610bf09ceeee5339c3cce1bae88834a2d`  
		Last Modified: Wed, 22 Apr 2026 01:15:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c5a0a050cc133a90ccefd5760860524d754dc3b1e5939cd6673d7459ad4b7568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b725c91f16469087c9ebb7b28a0aaee2a9a8e67f096d4d3e9e35658f623a2b40`

```dockerfile
```

-	Layers:
	-	`sha256:4646d7cd27dafcffd1415109c14468e8ed5d1b002120ae9efa832bcff0a8c18b`  
		Last Modified: Wed, 22 Apr 2026 01:15:10 GMT  
		Size: 3.1 MB (3145786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b145c9c7ee2ed9eadfbacd7d34b6284ccb951891e9577ec26ff0fc715915a42b`  
		Last Modified: Wed, 22 Apr 2026 01:15:09 GMT  
		Size: 5.8 KB (5850 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:68a60377f5a8c57b8a4f75e538e2eaea3fc65fa3ec1cecef9b00b8087f1f3a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48726332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a97c98d8ac9af3897e8e7ddedff4686b47dfa35908b138d551f1bd4467ee21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:15:07 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bf17e2bd9d2bffe1d04cffd7317dcbb7a2a4c186c9dfb9d304256a390be3e654`  
		Last Modified: Wed, 22 Apr 2026 00:16:36 GMT  
		Size: 48.7 MB (48726110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f0885571673a03352fa4f87ec6e0d61866f084bd83dcfae0a42d787bd6d212`  
		Last Modified: Wed, 22 Apr 2026 01:15:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:21e74dadc15d9b4d552e602adfec653b1d5f5693a198c551e75170f821c34e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d6c5cf6475486343309ce58bb0f9c39a1f34c9967ace859eb932506a372c83`

```dockerfile
```

-	Layers:
	-	`sha256:355ba5add09d33a15116977bbbb6dac001c512975ab48cab66ee807d4c4b9659`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
		Size: 3.2 MB (3150374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00734268caa3b1dbaa033e8dee279b091fe14f945587c86a3176a04baf4da34f`  
		Last Modified: Wed, 22 Apr 2026 01:15:14 GMT  
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
$ docker pull debian@sha256:d63257cbb5d64c07ca19442da8b9ae1db2d86a276891a2afc5d3a2e3b9feadfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48407827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23d524163556392ab5adc19a1ae14521d6733fe403bf2e311e9ee35ad0c1259`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'testing' '@1776729600'
# Wed, 22 Apr 2026 01:14:37 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7d15de2b1a4fc4a6aaea8920bf366a7c0eeaaf95efaa5bf45810c4f134cefa77`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.4 MB (48407605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb678c0ecd0cc88914b678f5985249e90d83fc9e2711d73867083211d6fa380`  
		Last Modified: Wed, 22 Apr 2026 01:14:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:74df894fc9da1bcc7e6e808bd5980b2f2ef737d5ac95d94e08dfebf661e1e110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8072b783eff5df29d76bb8239847a6db25d685dc8648d901b7c4c4d25f233c`

```dockerfile
```

-	Layers:
	-	`sha256:91f1c1263d6356457f3f5a9af68ba4ea9c6e9ed861b279fdc6f5e683fa01b47e`  
		Last Modified: Wed, 22 Apr 2026 01:14:49 GMT  
		Size: 3.1 MB (3145875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8b0023f648acd1884be4203b76c51adbc9e23370eeeceb92e7f26396a82663`  
		Last Modified: Wed, 22 Apr 2026 01:14:49 GMT  
		Size: 5.8 KB (5794 bytes)  
		MIME: application/vnd.in-toto+json
