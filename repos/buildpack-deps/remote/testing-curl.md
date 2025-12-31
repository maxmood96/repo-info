## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:b22e28676e0ed26bdf5ed4c62ebf26c1019c3b0afa4a5a84a7f820b9b896e5d8
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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - unknown; unknown

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

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ada2d98b462b3be79df14a2e74667b6b72a73d4eea696e19cc969e0a64e7b2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82401011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6cedb2589e45f9af4d6f42cf1cbeb5fbc65cdc68d41df87c0fd3b59daf4038`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 17:37:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54599ccf89984b4276abd319313e6196e0c98d5dab089007f3a268e18b7c0773`  
		Last Modified: Tue, 30 Dec 2025 15:07:59 GMT  
		Size: 53.5 MB (53522113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac8df3938d78eed997e73e6ed82d97f340e75d6e7ff2a81005a02b1da64c9a2`  
		Last Modified: Tue, 30 Dec 2025 17:37:47 GMT  
		Size: 28.9 MB (28878898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da59e05b7d313c0293a973677d97ff123097e5be721f4bc6bc1fc9da18df6ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d7d53eaacf2ec759db8a195ea25c877ed26bcde002aba5fb87d695c7c5171e`

```dockerfile
```

-	Layers:
	-	`sha256:d9479396a0cfd6bfbdcd3afd883c6fe1277b2ff3e174e72d97e109af4b7abeff`  
		Last Modified: Tue, 30 Dec 2025 20:20:35 GMT  
		Size: 4.1 MB (4116768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed72a1d266a3bc6ab0da91a26e23ed2b7d2c7fdc9120ad519cdec27340d9e326`  
		Last Modified: Tue, 30 Dec 2025 20:20:36 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cdbb119d0eeab2ebdc7de024dbbfbe544add4a510a5f7133d5f9c14d4476e956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73248287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be2b8b5e6d8c5664190f6d1675c98ee1fb588fc2ebf761935c9947d237d65af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1766966400'
# Wed, 31 Dec 2025 10:08:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fa050f4b17c5ceeeb0fa97b5cfc16570d13c816d216a6d728fdcd2ef48d6b8d2`  
		Last Modified: Tue, 30 Dec 2025 00:33:03 GMT  
		Size: 46.9 MB (46883497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5c10df2b542888be6e462c52a3b48b5c82db52fcb9d921487bf6421096dec8`  
		Last Modified: Wed, 31 Dec 2025 10:10:34 GMT  
		Size: 26.4 MB (26364790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa03b3234fc76c41e31277ce817a011f7ab005ba9f193002d0bbd131e410b73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b1862635053b530ba3e8e2034eddf30eeef2c4f048d86a9fa80e78fb605976`

```dockerfile
```

-	Layers:
	-	`sha256:5ae23a5ba8ee1045d76f93f66b6b4d39986d5390041a2edf90818f5403c7c4db`  
		Last Modified: Wed, 31 Dec 2025 11:20:03 GMT  
		Size: 4.1 MB (4104603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3544b72c68fd8fbeabad547c2ca9949e091b3f5573e3c4031a29bf31571c816`  
		Last Modified: Wed, 31 Dec 2025 11:20:04 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

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

### `buildpack-deps:testing-curl` - unknown; unknown

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
