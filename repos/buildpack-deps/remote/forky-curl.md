## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:4fc51cbe46ec00d5379727890be400eebeea222dd7f7b2398725fdca3ad20411
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
$ docker pull buildpack-deps@sha256:dced7ff7ff550d6416cdf442af6642c7528b4a09b03ce8308ac4d88fe0add2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75686424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee751994840dcc956dd4105abd1e70dc55d2567eccbaed2c4d40d56351e95944`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c7cbbee3050ecd826301596e459f3fa12ca32f5ba2b65d33b56172341d2cd3ff`  
		Last Modified: Mon, 08 Dec 2025 22:17:14 GMT  
		Size: 48.5 MB (48512511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd84557bf7a7d4887bb1011af57bc292a828ae0385421a537869e26f5aaf10da`  
		Last Modified: Mon, 08 Dec 2025 23:07:35 GMT  
		Size: 27.2 MB (27173913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c04e2a6d702dcd1bc0793445a07448c5b61027151fb99a1eccfdb4c8b349668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4113981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad641eb91359f1ba55b6825c3289c8a794da9df53345688a4227180e9cac96fd`

```dockerfile
```

-	Layers:
	-	`sha256:a456078870c97cd13cf03e8fdf853127c460379749f86686ff3913cca3b42b03`  
		Last Modified: Tue, 09 Dec 2025 02:21:55 GMT  
		Size: 4.1 MB (4107208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7fe2b0c264232cd613fd60ddf5e10ad1ed66ea636fc0fc0a2bffe608d79f237`  
		Last Modified: Tue, 09 Dec 2025 02:21:55 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

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

### `buildpack-deps:forky-curl` - unknown; unknown

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

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e07b3f9ea1555c568dfccb68b2c13915971c1375400b68a4e4112b0447d3fb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75071131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faedc507193f1c5277e8948374e66d0e129b888b5f55210dcd145b6a3c2e27e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60db063fe1f6101cd454be84b0b672c499625ca27e05c40ddaf285db3af29997`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 48.6 MB (48599337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ca0bfa7c46cad923ad76830a45cbb46a0f64043f0882f050c618ba02ce26a2`  
		Last Modified: Mon, 08 Dec 2025 23:11:11 GMT  
		Size: 26.5 MB (26471794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f6b750fe47eccc5d18ba94a24b9f0351eaaf72122c68bb46ee2af7de03c5d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8439fa0f7691b48a309fe6e37370468ce30fa6ce312062e0441a15f7419a672c`

```dockerfile
```

-	Layers:
	-	`sha256:6db050688d686f71959280abb2ee5c638be8716314d3d800f2e8cdd2d98252e3`  
		Last Modified: Tue, 09 Dec 2025 02:22:05 GMT  
		Size: 4.1 MB (4108101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b831af52644cbb5d45a43138f4e98231695d4183e8f86833dc70f27a3b067e`  
		Last Modified: Tue, 09 Dec 2025 02:22:06 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

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

### `buildpack-deps:forky-curl` - unknown; unknown

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
$ docker pull buildpack-deps@sha256:8caeb160a69c812ae54bc1277c0746a406a39b6b31c42e13cb99c81e29bffa56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d53ccb4ec9ed83a6ffb34e6f287fe110f5e755e501bf8e675d65512d9da0325`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1763337600'
# Wed, 19 Nov 2025 19:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f062c29e53f6114ba8255e90dca3ce517e3e0563bbe15af71540ba740a9253d`  
		Last Modified: Tue, 18 Nov 2025 01:31:28 GMT  
		Size: 46.8 MB (46806333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7e03bce6d0d0951954641ed6a59e64caf78431003e1f4dc54250fb69de83f0`  
		Last Modified: Wed, 19 Nov 2025 19:31:39 GMT  
		Size: 26.4 MB (26395035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1439ec7041af855fc76bbffb603a296e49b5b532a32a0fa8248155e6b5aa29fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4097579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9287ef59b25a39d7555b6197c69711059a0ec0f87825e178dec60265409d9d`

```dockerfile
```

-	Layers:
	-	`sha256:cc363b7e0744a9e9ea1091a0784c305e0c1c22b0acb16e57b60c1f1cf57a3680`  
		Last Modified: Wed, 19 Nov 2025 20:20:08 GMT  
		Size: 4.1 MB (4090774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8efdef3d20390c11ce2e31756133bcbd98227b183de0566a5652a9f4fa9795d`  
		Last Modified: Wed, 19 Nov 2025 20:20:09 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

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

### `buildpack-deps:forky-curl` - unknown; unknown

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
