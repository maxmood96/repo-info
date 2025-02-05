## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:a04301b3f0228ab87b3c3351ca312ef17a8d2a1394e341b98b40c7048793662b
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:aee25dd8533c4987c4174b90b38c111bafbbcb7d62625571ed88e06c5d103e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74387342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ba49db818dc17b8375378ca48a72a856869186b91b7cc1bc25cf591349ed9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:af4da4e2d364845ad19d8dada5d782436e7eefced1b551d8d6a613212d528000`  
		Last Modified: Tue, 04 Feb 2025 01:36:46 GMT  
		Size: 48.3 MB (48348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1be2f67d683c399ce2229317b243539533edd5a34194175f614d9715ed155d`  
		Last Modified: Tue, 04 Feb 2025 04:37:54 GMT  
		Size: 26.0 MB (26038437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13051b3a62affdef39f0b11959ab2f3e5be76cc4dbb01d84f0882ebae8ebe7b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4048111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6b5b4470cf325c65245a4121edda03884ee9dd31ca16a14c891cf36080c7cd`

```dockerfile
```

-	Layers:
	-	`sha256:baf1bd4a8e8ca39f8474004a7082c2789d2157ac1f6784ca6dd790f2c10e2726`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 4.0 MB (4041291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f014b0fdbc84aaa05d094e879a3865d8ff0c20f33326bde23301a0f144e7dd`  
		Last Modified: Tue, 04 Feb 2025 04:37:53 GMT  
		Size: 6.8 KB (6820 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c8b72309a00c55121660036dc53fc7a55227dd584a370f77d25f8d06e544c915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71245572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c5897d4a1b1f8a5acad55b61b1aac3c28340525f575546f22605ce71a4b008`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:65c8e105f1e96f93defe25039ead5b48a9870e86175b80348bfd23ae3445cf2f`  
		Last Modified: Tue, 04 Feb 2025 01:40:53 GMT  
		Size: 46.5 MB (46502404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e17e53e6ecbca4d6fed6a359edf4419edd97930a581be4b6ad999669de4cdfc`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 24.7 MB (24743168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e3c37ea07ec604ed597239c3e420144e4445ac99f8ebe34ec8d721c622caa657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95d254ad2a5dead6eb395b06930bd6dd081a28e79a3adf074ed155d8dc59799`

```dockerfile
```

-	Layers:
	-	`sha256:008cc661fa77c12a00af319e8adc81a6ad24da66847717769b4f90b93b6dc8e8`  
		Last Modified: Tue, 04 Feb 2025 08:04:29 GMT  
		Size: 4.0 MB (4048918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438f772e281905bb522f01575f7ec1286452b5b73198927e065d129b4448a0b9`  
		Last Modified: Tue, 04 Feb 2025 08:04:28 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17ce56187dd8b5bd14eb7c413f6bc63b31f85a987ed03de91f8c44f8f8f4244c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68525856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad6dd9272c626efbc13786e9d52c18d1ea6af09a6ea304e613c00980e7bdb0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e33ebdd9205b4932e0915a58ae82fa3919bb7ba65980ba80c0f55146637007ef`  
		Last Modified: Tue, 04 Feb 2025 01:41:14 GMT  
		Size: 44.6 MB (44632834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b579f9683272f3a08c4aea06231a8e2c1bb0d003cd712e88bfd308809a74d5`  
		Last Modified: Tue, 04 Feb 2025 22:18:45 GMT  
		Size: 23.9 MB (23893022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d895484555f88bfbe6868c65a3b8722a26f16f50b03ebb8bf95e112a52130c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4048393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb28a48d69df1a402726ad788fa4ea4658f7e9ed9a370353466ebe85fe13e8`

```dockerfile
```

-	Layers:
	-	`sha256:b52032a92ac270b2d9c500993ae54800682187997a4344bff92629e9e3c71bc0`  
		Last Modified: Tue, 04 Feb 2025 22:18:44 GMT  
		Size: 4.0 MB (4041512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf59eae7bff5f72e387a4ef57402a8ca24040a76fc27433ee7e3c8efca89134`  
		Last Modified: Tue, 04 Feb 2025 22:18:44 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7680b91d4d72d5fa6e01ad7110a7be2a65c2c1255c7186a6bac50da12d15c650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74239100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410311625c1c975966a96b8c08c37737161d80e4792f19eee2142b7660a3528a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5e40a2b9fe32b2158c946023b700f61f57f567701b6be2e04192bbcc68fb32d`  
		Last Modified: Tue, 04 Feb 2025 01:40:49 GMT  
		Size: 48.7 MB (48735381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7a097e6822ff46406de4794f79cc58a671b1cf4aca2e12e0e5d75f3e88af8`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 25.5 MB (25503719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:303d7512961423b549ecbc3135fa423ffc439df03b4168223325681753f21177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338e85b070ec19c90c8f570a3d068cfe50e05677cc95e41bb216dbc2aca9fcd1`

```dockerfile
```

-	Layers:
	-	`sha256:8da040da9e8301aa2cc9fab27ddedef51e88742ead9e384fd037dccfeeff1449`  
		Last Modified: Tue, 04 Feb 2025 09:01:34 GMT  
		Size: 4.0 MB (4042186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad182928bef2359b12df2205d712273972389550d13ce80f836942225a82f170`  
		Last Modified: Tue, 04 Feb 2025 09:01:33 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6b88c5ba9bea73f06a57983ae54bfd9807848ce638c923d2155fab2143198898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76938960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b74a863b4d8839ed028b8736187a5fd7519b596282d0e5c889f6d931183078`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6eab4c65eb241da9efbcd7f3af754621262244b11cdb15579a1ffe95621258b`  
		Last Modified: Tue, 04 Feb 2025 01:36:50 GMT  
		Size: 49.8 MB (49751669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f716b567c64e0e309015fd1a02f5a6cc44d9337e2d33b9f6b8078b32a497ea27`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27187291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5bef7b21a0b6b48c3cc0c8710b313ea295df7028cfbd4a432cd82c296c19e3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fb60dd8531f4ef2f9f0ab88a0d2c4ca3bc676fe4d34ffb8edf7fef45312b50`

```dockerfile
```

-	Layers:
	-	`sha256:77f1f939488d24c35d246e6dc7da23e7bed192f4991546e81bd85ad236384f4c`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 4.0 MB (4037042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2058966afd76dd12c237c44e52deaa671faffd214c395bcd6637cae7358e86c`  
		Last Modified: Tue, 04 Feb 2025 04:23:41 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:86412e93445910f1ed1074312e25572705d586496cb7f088b1392e36107ebf2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74577983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a331b214c2c756a4c2af343495e0e4f68416c368b983d1bbd906472fcdefc25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7826127ebc82b4ee7746953f0d6a69270e61dcbbf770239c14d7990a9a75f3f7`  
		Last Modified: Tue, 04 Feb 2025 01:41:04 GMT  
		Size: 48.5 MB (48512402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1db1bb102af1e1e6cc9344b3dc0fe8a2eacb41e418cb6879c409441345ea5e`  
		Last Modified: Tue, 04 Feb 2025 19:29:29 GMT  
		Size: 26.1 MB (26065581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e38a36244521f22a44637e5e6de406bb111f7888062bf17485e8b93821f66683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b04128000a2994fec0c3792d9199ebb1d6edfb0b7810ca105754efe943abb28`

```dockerfile
```

-	Layers:
	-	`sha256:ad5c6179ea903265d77a106dd51ba2c4baaa83660a3702c0df0311e586c1ba20`  
		Last Modified: Tue, 04 Feb 2025 19:29:26 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b417044fed6946b9ceedb24ded07ce965a1f3f21c1de47a18d938bdf6e2ebd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79735448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29cfb8b66e8c24333411236ca2f6e24b1daccc2a8b815ba3b35f81ec2d2ebdb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f8f4c2cf61c41cc250d2e87b5eba96ba3e64ef3a295453812dac1f66ba73216`  
		Last Modified: Tue, 04 Feb 2025 01:41:20 GMT  
		Size: 52.1 MB (52139243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae7e1fce86863c28c734873936872848b6798972c915ef83ac0ef8757fcc152`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 27.6 MB (27596205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83c2b87868ebccf9aefbed4a631970b5183e1e34f1b0335cb950386d48243ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feed53bdcc8f3767006fd26ebd376b9354cdee8fa89f8b62ff1bc2cf5e3321e`

```dockerfile
```

-	Layers:
	-	`sha256:58ee292a17e1fe38d5ccfa1ab34ceeb018c8c04929e010691e86d22a0460d25b`  
		Last Modified: Tue, 04 Feb 2025 07:26:33 GMT  
		Size: 4.0 MB (4049966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2714839e58afe52b34955a96c5e386d431aac0e80ebee0fa43014a0129f7b5`  
		Last Modified: Tue, 04 Feb 2025 07:26:32 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:08fb9b8e25fd7d2240644cc0fbab6ed7665dbb8639050790bc175b21bfabdf8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72320391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa13ec122275564ca0bc6af020b5182073076046dbb42e69280eca2af5af20d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f61e2eb7e669ffedfd7c292056ec3801e1d5a47c8a1ba8e2c9d94bf08f67ed2d`  
		Last Modified: Tue, 04 Feb 2025 01:45:19 GMT  
		Size: 46.9 MB (46907213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f3a589a8b6cbf639225cd2803ad3cdd7c9e4e67dbab48d826e7a48a0cb9682`  
		Last Modified: Tue, 04 Feb 2025 04:41:59 GMT  
		Size: 25.4 MB (25413178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e3fa6627834d0fe4a8f126e7a1eea14a37d385bf6decf38cf72e4454d76190c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30968d1267b0076b09edbb66aaff2d7245c6a25ae073593499bfd88c6da07b6`

```dockerfile
```

-	Layers:
	-	`sha256:0b516cb000b606b307b6aa5a0268e3a0bd502e28feda68e16fa55680fa39a28c`  
		Last Modified: Tue, 04 Feb 2025 04:41:56 GMT  
		Size: 4.0 MB (4032691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fefc9c5367ed3581681873bdd962151dcee6a14a309dd861250e7d9742ea6573`  
		Last Modified: Tue, 04 Feb 2025 04:41:55 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:17f8f4d673ad80a912bb54ea841d21fd9fd8cfd6b44b036d4e25be59403aaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75630946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ef2d13ba22b276248d3ae18b834d40b0699b7e34f64603fd8ac544927a1b6d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1738540800'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5071fbe67e05b7dce13c72a6b655c4750a6b0653fdce60a9071966d5a747a2d8`  
		Last Modified: Tue, 04 Feb 2025 01:42:04 GMT  
		Size: 48.4 MB (48414760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748bb8f4316900467409f846adce939a746b7f2adbe1e2ba340715af7fac142`  
		Last Modified: Tue, 04 Feb 2025 07:31:59 GMT  
		Size: 27.2 MB (27216186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1daaf0aee6f2ad2190f02166b924c8e24614ac3d30aa97b32836c15cd9f0cbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bd75c7e66e74cfe8701b21e4e463f81141d737e3d0837bc0e7181fda7f6595`

```dockerfile
```

-	Layers:
	-	`sha256:4c3f5b5b0a126e49897e13924462d03bf660d7788720d25bbd342ca25d88cec6`  
		Last Modified: Tue, 04 Feb 2025 07:31:58 GMT  
		Size: 4.0 MB (4047624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1644a119df56dd6162ab16cb8894344b6c303f51c4ff22bb5a3d32f34108f3ef`  
		Last Modified: Tue, 04 Feb 2025 07:31:58 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
