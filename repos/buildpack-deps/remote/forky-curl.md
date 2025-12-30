## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:7c5eb108e20a7da214c4727abb4d02398debf3d98fb40c724270715a9fe2b035
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

### `buildpack-deps:forky-curl` - linux; amd64

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:28d8562d13dcd0a169a7e39380211f80ab9e745a0283d39509d32158e9dfee3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70015495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a0c4e32ecd133e05cd4d7191c7b8b258050e8abb46fc8babd1804e262c85a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:241c7878eb5bbc21e3d5116dd5ea31832b2d3bc7489b0d564310ab3bd542adee`  
		Last Modified: Mon, 29 Dec 2025 22:25:59 GMT  
		Size: 45.1 MB (45129806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cfe0fcd77ad4f32a187bf7cc2a756d93850a1250b0bb64207ab8263c6fe614`  
		Last Modified: Tue, 30 Dec 2025 00:35:10 GMT  
		Size: 24.9 MB (24885689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:706dbcf3b065ad0f790368a98e59b04c0e70f966583c436d2521cc675b1a87a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d934fcb7eb50316491459d0c103f92f7149a783b54a121bfae3432f39f17654`

```dockerfile
```

-	Layers:
	-	`sha256:02743654a08ca0ca3b63f0f3db423596624119f6eb8329c2402809fa1fd47f2e`  
		Last Modified: Tue, 30 Dec 2025 05:21:27 GMT  
		Size: 4.1 MB (4114407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2821c711a980758b647bb78bbb4be06318ed218be7b2b95d739a3790c40eb816`  
		Last Modified: Tue, 30 Dec 2025 05:21:27 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4529f048af313f9d59cfcf471e5f428ddc7f6b96e036e2ad20004916dbdd7b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78368613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9441d5c6332f7f73e0fd17e293bc655bfea6d8c069692ef7b4c44a0d11bd8aa3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:47:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a557815b7e39210fb0b4048ae58b1ffddbc8cf0f656a5974b6c3b24f7bdafed8`  
		Last Modified: Mon, 29 Dec 2025 22:25:28 GMT  
		Size: 50.0 MB (49955836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5e10cdcca6f1b0c95acb93ab2b6af2d31550b8756e6b5bae03f69991891b7`  
		Last Modified: Mon, 29 Dec 2025 23:47:37 GMT  
		Size: 28.4 MB (28412777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9c26f5175053b9cf247f89e88d8d194e5037c38e60dce5d9bd9ea22a5418ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fbd4bd97d5c2c0414fe53f4b15c3139d3d19b8e42e57cdd60614b413944a20`

```dockerfile
```

-	Layers:
	-	`sha256:efae4ff1445f8863e1dc1ba99529125aa1428e04ed18369971629b6032fef0a3`  
		Last Modified: Tue, 30 Dec 2025 05:21:34 GMT  
		Size: 4.1 MB (4110020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a148e5c43496324dfb81f532f6cf6241bcb92971044de727dbb00eb543263b`  
		Last Modified: Tue, 30 Dec 2025 05:21:35 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; riscv64

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9fe6298ab1162b85ca9e6c5611cbbb7809d463e47235431d17292fe6b3a0fa0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76668324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d60e7ddb6fa6453001ea8756120b49cd4a9368bb372b6785b1813b32851811`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 03:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ed754f864448d0e594994dc11148ccb02da6ea309851c997288e88ce4fa4e08`  
		Last Modified: Tue, 30 Dec 2025 02:08:24 GMT  
		Size: 48.4 MB (48397553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d28917da9bd93a97bef96b25f92932fe3babe10b8325e0cde3317e7a34eba7`  
		Last Modified: Tue, 30 Dec 2025 03:24:40 GMT  
		Size: 28.3 MB (28270771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9345ed3fa0b9f6cc014a7f52f4923b15d34b8fa45b1b1acbb0ba384936b066c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4121093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c387aa648632f2b8348ac1ab734805ec3b044808d80b48c73ffa4b45f66bab`

```dockerfile
```

-	Layers:
	-	`sha256:e991dcdc11f88e714a426fb0607f89ffba20683d5d6e043c1789f498cb96dc54`  
		Last Modified: Tue, 30 Dec 2025 05:21:46 GMT  
		Size: 4.1 MB (4114320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11fb7494be562cee41429034fc6c04807042e5d27f9dc3431457ecb7e2bb4445`  
		Last Modified: Tue, 30 Dec 2025 05:21:47 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
