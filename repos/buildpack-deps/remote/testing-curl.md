## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:cfd664f05003f22fe5ee83073f65948e595ce8e53d95839c07f702e0699a03b9
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
$ docker pull buildpack-deps@sha256:36c071dbb294844d5b3a282b5fbead76a5c45d2437f54c82255c09b9c91599df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75994483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbe5a9ae4dc03527897af4f37e419aaed9376f2bbe45184560157bee785513b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:45:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9becdec1844ece10920454e52e9f153d35fd872e9ffaceb5593016edc7486d22`  
		Last Modified: Mon, 29 Dec 2025 23:46:16 GMT  
		Size: 27.2 MB (27164425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4abe899584b76c9bc56f583917287e59f7229a97deaba5a831fa6a5cbef32e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34c2b8a427655e6e0ec38e93052a8e5e457492cae22a89401c15de5ae4687e2`

```dockerfile
```

-	Layers:
	-	`sha256:cc20a27b5d3cd61384c91fbbde592bc1fcc79f075f3abb26e222a06474b27eb8`  
		Last Modified: Tue, 30 Dec 2025 02:21:13 GMT  
		Size: 4.1 MB (4112911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71dd4b3d7c8dcc8a8151b8e462dca892a3ddf19325334db33351592c285df2e9`  
		Last Modified: Tue, 30 Dec 2025 02:21:13 GMT  
		Size: 6.8 KB (6772 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b9f70b3deec1d28646de6eb0d8cc454ed1b5f3c66234a0db4519a439da6817d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69939092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8631914234db289df900fa64044367ad2ced299fe65f4d1277c5b6a9abd7f08d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1765152000'
# Tue, 09 Dec 2025 00:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:97c0e703f22fcbdd1717c90c9c81bde96e65c1c3051ad73d18fbc908c8b17e4d`  
		Last Modified: Mon, 08 Dec 2025 22:15:47 GMT  
		Size: 45.0 MB (45048041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b854bd09bce55cace36b7ecdbfa75886d833623af6ae1398f2375a0e142faf`  
		Last Modified: Tue, 09 Dec 2025 00:06:18 GMT  
		Size: 24.9 MB (24891051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c9f23a68602879ae36b4329178ed5f94626dbf6f19b0d74d7a5ce7e3c0ccbcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c3c71b6d529b15ffb00994fcce58e8edab9b8696aa61700fb169cd1898ac65`

```dockerfile
```

-	Layers:
	-	`sha256:8d04220ca1e90edae8a5f10dcd690c3742681a133c0a8cc81c84ce85a9a31276`  
		Last Modified: Tue, 09 Dec 2025 02:22:00 GMT  
		Size: 4.1 MB (4108704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70fcdd0417654548d68a482d68a8257a83bc513721b1b75073ac17b6e82232f0`  
		Last Modified: Tue, 09 Dec 2025 02:22:01 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee3cd4e9dc0b7d1ec0892316794421342306c5397ad7a497c959d03820c1aaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75292871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4485281fec3c932780a8e495664116a151edeae296e48e01cacd241e5d7086b0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf6ef9ff46c8cdd87f91591a96ba850200dfe34c376dffe91134bf667ddfa22`  
		Last Modified: Mon, 29 Dec 2025 23:46:56 GMT  
		Size: 26.5 MB (26460878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0f1d04cd51d7c1967eec7139cc223ff06a03e84106368543bad49536aaedb46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f22bff69185177b0840977e77c53842684b5d357cde2e5612439056433d712`

```dockerfile
```

-	Layers:
	-	`sha256:f072f7064d6acc5f8cf8c11ba0d02412e8c2529a61e76201a608678b2ada569c`  
		Last Modified: Tue, 30 Dec 2025 02:21:21 GMT  
		Size: 4.1 MB (4113804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e42bdaa4a40573776846f2bddd88366f6cc88b1c943d0611a3224bac8bdd3`  
		Last Modified: Tue, 30 Dec 2025 02:21:22 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:479e7c90bf2736492749bc397adcab9be0c9be49350db838affb560934fa1e78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78285451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c085da10174d2a94787f994cf38c4af9484483dec207c88bbe0d593f467ce6f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:14:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab10e575001e02de99efc833f717c00ab06eb63e6d406d2e8435c5550eb4b`  
		Last Modified: Mon, 08 Dec 2025 23:14:41 GMT  
		Size: 28.4 MB (28410871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e1fca201866040f5fd15b8c2ab2b423d3e82e520a834f6feaa96d9f9f9118f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66024bcb08a3198f6d61ee9ddd074d26d29ad9e8afa6585441946710f1f153b`

```dockerfile
```

-	Layers:
	-	`sha256:23a9b37d12210a713aa7ae6f8ad2a5cb121237521800c1d26fde7d61ec90987a`  
		Last Modified: Tue, 09 Dec 2025 02:22:11 GMT  
		Size: 4.1 MB (4104316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae4a2643f946a385852abf22da48b03d8404203a0c6dd1793eac99dfe1634d1`  
		Last Modified: Tue, 09 Dec 2025 02:22:11 GMT  
		Size: 6.8 KB (6750 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:db778f3686c5b69c7e75558f34f35b2e4336836613234973d49953d5c764062b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82278312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6ebd61e1dd9cacef459f723f7caa81418b13d5a27d43b34f5bc2a80f023e54`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ca6b6474de59c13edb40994c0579d1471aee6a7743baa1f84bd96cf0fbd414da`  
		Last Modified: Mon, 08 Dec 2025 22:50:05 GMT  
		Size: 53.4 MB (53413786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16460d60e48e0172db82e752033b5336b64df38a32ba4e288da4b3068cc402ff`  
		Last Modified: Mon, 08 Dec 2025 23:21:53 GMT  
		Size: 28.9 MB (28864526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7642e958390b14ea3895cc7d7192fa3144dc4d8e1507d62e7f9fae834b1d834b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4117868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2440724cb4a209e3bf816cb6437abf9ccf75f4f76bdedc809c938e0f4251d87b`

```dockerfile
```

-	Layers:
	-	`sha256:feedf24d73f4f2533721f7523f3b56e4ce720afe8adf4e82e89edc06f746518a`  
		Last Modified: Tue, 09 Dec 2025 02:22:21 GMT  
		Size: 4.1 MB (4111063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b6e9b02d791dc99ddb808ff69e569e11c8560a03016f876de32bf40b3bbc83`  
		Last Modified: Tue, 09 Dec 2025 02:22:22 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c26164c5201010dc358db4cc184c281c117cd22d65e4719589444e735547e7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73251510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2be461941d4b472f545bdc9cc47a4626ca42f190ed040bcb6a1a4f58409df7d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1765152000'
# Thu, 11 Dec 2025 08:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:002664050c13ca9d4571d9c24b2cd8235785825417d0a59db3d16cec4b277530`  
		Last Modified: Tue, 09 Dec 2025 01:49:57 GMT  
		Size: 46.8 MB (46840355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79762d676bf44b71b19af2f5e9bf3520032115760ca18d18b1e487b509a74b9a`  
		Last Modified: Thu, 11 Dec 2025 08:33:56 GMT  
		Size: 26.4 MB (26411155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51a70350157ccee97311aa1e78c981cb35139f1d522dd7c0b986bd7428ece401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4100053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55780d678da330a1e60e0491820a164aae246f405482bfeaece2300950f6fe18`

```dockerfile
```

-	Layers:
	-	`sha256:7268663f4c5a01d1e36e5b0ab077a5bb84ec907beec09577a33b52da353f5990`  
		Last Modified: Thu, 11 Dec 2025 11:20:14 GMT  
		Size: 4.1 MB (4093248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15235160361d7109abce6dc3e0edf60bce112b5eddee2472f029e91b44b7efcb`  
		Last Modified: Thu, 11 Dec 2025 11:20:15 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:30886d1c745d956062cbb7025a016d8512ff16e6e3e9e9d9f8be7dc1e88f9593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76612004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee44dc6ca0344eae1635811df90b3641f661b7ee9700d4569e6278071f8c569d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1765152000'
# Tue, 09 Dec 2025 00:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:88e5ed2f2b5ebe4c22b20536e853aae0963f42dcc4ff80e14e14172e983096b3`  
		Last Modified: Mon, 08 Dec 2025 22:20:13 GMT  
		Size: 48.3 MB (48319837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d47897a01efebe9154a3fe179f72cecb78c93572d95a8b9465a3989d8d1df11`  
		Last Modified: Tue, 09 Dec 2025 00:11:09 GMT  
		Size: 28.3 MB (28292167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:071168c5e48d80d8327e79c03c4fcc0a6f1d401eefbd58669fa5de784c8b55a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb90ef8c4f27cdfc871a5db89663e09d986f72d14f85fb9f785442722cd247c`

```dockerfile
```

-	Layers:
	-	`sha256:cb11b8d7e5b9e9e419ae98b28ab7ddddc770d6df53ad802da59d2a754ad4c434`  
		Last Modified: Tue, 09 Dec 2025 02:24:17 GMT  
		Size: 4.1 MB (4108617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2c3e98554c9c90fdc6f639bdfbcf558cdbb7c410e4fd13c482f4c6ae30e2b2`  
		Last Modified: Tue, 09 Dec 2025 02:24:18 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
