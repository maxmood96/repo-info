## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:0203a82c68a97508555972c3a75ad56789362580a871797be451d7276938dc83
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:78a08550c4d21fb51ad2fa5b9450d7e48def6886e714978f83bd1318739b9a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143978109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a8fb2eefc800f6d568ce38982c17d3d0a1cadb12a8023c2fea0c7beff2dfc4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e26574e4db891d66a1e5b6eea7efe5496bb61e65ab34b6bccfa4228941ecb8`  
		Last Modified: Tue, 30 Sep 2025 03:17:23 GMT  
		Size: 27.1 MB (27050070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86429f6876fb8da0a626753e746ec375d5f24414fad40449bf193e18157416a`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 68.6 MB (68551074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32b1cc70f2d487d0b4bd7b85c579d45e39ab7df7fa25c88d43f67d650665491c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7744430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0da7f2744518f2553e0fc5f18b3e4524f93303700bae107c78ead6090adf4d`

```dockerfile
```

-	Layers:
	-	`sha256:2fec28d9e8b2b25b92d44f1308e2a0e05f6d244d07a041e55dc6156b616ad2c7`  
		Last Modified: Tue, 30 Sep 2025 22:36:27 GMT  
		Size: 7.7 MB (7737133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb49178059fbcd11530bf5b08d730629750b2108b985706d8307e4f88cab679c`  
		Last Modified: Tue, 30 Sep 2025 22:36:27 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c223a66ffc590873d4c2bf64d9462b63fdc02febedffdb40e0e452c4f39d358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138318245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58489e8af514d871cd2ead66c3f2e47c1de72e631d749ef51ad0478b27b3ab4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:204bc56c72452e737a2bccff3f4208682016048e825d5ac2bc52dc2c4d4649de`  
		Last Modified: Tue, 21 Oct 2025 00:20:34 GMT  
		Size: 46.6 MB (46593513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3882f8d4f2701b8365480052f7e556ff8fd1101d8f1b72e8141c4360f1d695`  
		Last Modified: Tue, 21 Oct 2025 02:32:18 GMT  
		Size: 25.8 MB (25784458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff346c12ee6ee902eef6ce2e57381cdb35b81a53850091071c07fa57c84dbf1`  
		Last Modified: Tue, 21 Oct 2025 03:57:08 GMT  
		Size: 65.9 MB (65940274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aed025f08383477e19bb13b1616d8e380b4f8008e6e2a48258c271c8c9db74ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7755491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18925bbd133c4aa947aa81fa4a42d3e6d55cb5cd5d5dad87c1d63955f6e8e3f6`

```dockerfile
```

-	Layers:
	-	`sha256:896f8033f2d33dc78216ee744bd43184b44ed315910bc776017412ac81d52d6e`  
		Last Modified: Tue, 21 Oct 2025 07:21:40 GMT  
		Size: 7.7 MB (7748130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95dfe831681bafbf943c96341b0477d83e9912e5d29d3d1e389b86ae4489fdb4`  
		Last Modified: Tue, 21 Oct 2025 07:21:41 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:027c29889b9b50812dee3b113d570b0de3df4bcafecacc5f3a15920c81ed5914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133128737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40454afb32c885390447fcf9cf68460a577da9ddf659d80713c1569ad605a4e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1760918400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d46bd548fc78deefe00dfcd2b559377066496f2d6beb8d1543970d5a2164151e`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 44.9 MB (44911556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ca5d6a8872c7e1682c82eee718887aef134a416249261516f2ddbf348e5bb1`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 24.9 MB (24922039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffa63c9ab104c5969f04bb0672948fcd7f46b1680b5c36ee57bb532b455b361`  
		Last Modified: Tue, 21 Oct 2025 04:11:34 GMT  
		Size: 63.3 MB (63295142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72136c9115a0570232c01a21fbb937ae3591a63b8a970685b0a3b461ebecac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7754942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e45379e0f1eaab3dbebbd3f2251031dd4acf6f8862615e33b423da0703d7973`

```dockerfile
```

-	Layers:
	-	`sha256:79d3aa1436ea63574a966c1b9d313a57c5aa02d3777220e1bcf9696bf1692e6a`  
		Last Modified: Tue, 21 Oct 2025 07:21:47 GMT  
		Size: 7.7 MB (7747582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a175056fdde3a74733e4a9063b107c3ed50b8dccb84a41ae44b4dbd51a74e17c`  
		Last Modified: Tue, 21 Oct 2025 07:21:48 GMT  
		Size: 7.4 KB (7360 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:97071d7469776f0b0d13749c6d496558fba067dc31abde30bcafab9cbbd8de07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143013509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff2e0ee7ce88697abcc77b0d346b5c0d1c0fc6bfd3e3fef4b2c4a15d0a6dcad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5aae340a376cad680dc8a41a7fd30a241ed4bae3e53125ebb424c8fc7996aaa`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 48.5 MB (48487991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f20ec06b0e305a026538da296c8990c47be2e5df6951865d9920759cdeaeb5`  
		Last Modified: Tue, 30 Sep 2025 00:14:12 GMT  
		Size: 26.3 MB (26345963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98b53826f16396691cd675240f8b08bf70b30d5a527d2aaf12eedd7838ad3b7`  
		Last Modified: Tue, 30 Sep 2025 02:14:02 GMT  
		Size: 68.2 MB (68179555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88db25154ca99e2a3d7d6bd30da1ee9949f58a1dcc1b37367c4a474521130e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7751533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddbace54b4eb2fd3a603204a947c5152c9d945715013c1074ba3751ddcb1980`

```dockerfile
```

-	Layers:
	-	`sha256:b8f04d14f0f1974b9243f374ec548f602a4dd566b73b9bfa56773bf11e89f05f`  
		Last Modified: Tue, 30 Sep 2025 13:24:50 GMT  
		Size: 7.7 MB (7744157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf08eba61b135b258978ad38b99cd07e3e17a4d629a44b11be8134efafb90738`  
		Last Modified: Tue, 30 Sep 2025 13:24:51 GMT  
		Size: 7.4 KB (7376 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:73afce5a847829a48cd74a3b4dd8b40b231f4a2e16bb470c7dfe503129387ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148302470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515553b1056595772958616c4370287a95d9529b8d525c3a426237a39e490f48`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e022e41d633c4affaf1ac4e552e4213448a292b3aff35eb2748ee936cdab8ed6`  
		Last Modified: Tue, 30 Sep 2025 01:19:38 GMT  
		Size: 28.2 MB (28189334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbc4641a87c97f6e9e6e2361254a7f1b45a142ef503068f7c0cf3708f035a44`  
		Last Modified: Tue, 30 Sep 2025 01:20:22 GMT  
		Size: 70.4 MB (70426965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d472db167527743858ef4a6e0bf1c29fd99079c2e91183574b7c2ee9f37929a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7740560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21010f03baa073ca4ddcaba839ba5f153e7d3b854a8aaa783b38e0211a0c1360`

```dockerfile
```

-	Layers:
	-	`sha256:b7df37a5479e8dcf03d0ce0e285be3a0433212f4705b5180b6bea3be0fe7b066`  
		Last Modified: Tue, 30 Sep 2025 16:37:58 GMT  
		Size: 7.7 MB (7733285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64273a0b57d5fd9992e8e9e8bb8f16913b12591bb72953073c43708dea5cc750`  
		Last Modified: Tue, 30 Sep 2025 16:37:59 GMT  
		Size: 7.3 KB (7275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8d9e7adb0d6da11b21f4a45b666d435d7f19ff0542343d4969bfecacd68367a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142849847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772c5739057062d7135b49fe5c7a0e04b2a2657ea60b1428be0c40833b2f623b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4775def833a620dde4f1cc169ae067301bfe3a34dcf5509c22eb227d3468f1ec`  
		Last Modified: Mon, 29 Sep 2025 23:36:30 GMT  
		Size: 48.5 MB (48517068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9e4d8c8e300db469e918627e177662d2c9145c896127a833eae485613de801`  
		Last Modified: Tue, 30 Sep 2025 14:02:31 GMT  
		Size: 26.9 MB (26941858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355dcb4e6f8d4305f466d18918201a1d1987966e7ad83941fc93d52a3f5818a5`  
		Last Modified: Tue, 30 Sep 2025 20:30:18 GMT  
		Size: 67.4 MB (67390921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:626b16bf388cd353586efcab02aebed2307e1b3e4d14b38058014404f65c8343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0831a24731a90b23610f617e00478b0a17c81c0eb6e4af78a46de064a606ce`

```dockerfile
```

-	Layers:
	-	`sha256:ed9d6b344ebfcfa31f7a655119adbf9751002d021a6fb3dc4607d371d5231f5c`  
		Last Modified: Wed, 01 Oct 2025 19:20:58 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a87ed7c334e35802f51129c586ddc65400a2836d99fffe8647eda8dff3312a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155394594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb1dc6ce7a34904fb57fd75f98d6f27a3d7e93af06a2a5fec5af4dcac91c895`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:77c8b650eb6fce09ed4263c2e250af93b45ee5839eef29ca2155317e0945bc1e`  
		Last Modified: Mon, 29 Sep 2025 23:37:42 GMT  
		Size: 53.2 MB (53152155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d111aaffc2c801bff609a6e02c9de336f2bc1ea5c09d43a29d51e58997b20a73`  
		Last Modified: Tue, 30 Sep 2025 19:07:37 GMT  
		Size: 28.5 MB (28522160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984a3c965c22954420e5fc5d6d364efb5b25cb9467e9ee7553350dc94f4ffb93`  
		Last Modified: Tue, 30 Sep 2025 09:23:36 GMT  
		Size: 73.7 MB (73720279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75d716d7c4e03caf270c12fc91372cf1bbd54fb46a67b48c5a1641a2f886828c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7751550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40eb5ab59b9b3784b539b9404a365bd608a06fe394242bce0b01f36dbf18cadd`

```dockerfile
```

-	Layers:
	-	`sha256:9c644bebbc3d6a3d657bfab634bae192d77377cd84a225eca4f08db91d2517b0`  
		Last Modified: Wed, 01 Oct 2025 22:22:25 GMT  
		Size: 7.7 MB (7744221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32d356a702ed7bfea07cbfc3b1c35725bb1363775081a7ee8e46754ba2055704`  
		Last Modified: Wed, 01 Oct 2025 22:22:26 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:23f17cd327db62b22a1444b64dc6673d230f782876076f5e031270be4f6fa140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144148398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9667e18ac20a3f26ea4ad13acbcdfa8593f06d7c0fb8942285b3bc9e3a0e5c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5296fd171b043d9adeac427b668a2c333e09261704a2befe2a2593421c6da9fd`  
		Last Modified: Tue, 30 Sep 2025 00:53:09 GMT  
		Size: 46.7 MB (46680971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d995bc0710c59defc3b6e948b5fec04402ad900b4af1204d7420bb8e2736886a`  
		Last Modified: Wed, 01 Oct 2025 18:09:27 GMT  
		Size: 29.3 MB (29334857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5342a4415df6cfdfa16b453bdb12523178508b905f6d7a7425c52c9dbe807e2`  
		Last Modified: Sat, 04 Oct 2025 09:26:31 GMT  
		Size: 68.1 MB (68132570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:deb1f03bfdbed59713bb74f6ea096156ade980096f6ab8264e7d367663621811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7743459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09e357dcac8d89cf8fd1b2c1f9aff86ab444ad6d03c98a2465f046dce42c8f5`

```dockerfile
```

-	Layers:
	-	`sha256:6de0dcec7d3bea8635e2794cf8803d2180fc98608aa87810fe3a7ea4c50ecb60`  
		Last Modified: Sat, 04 Oct 2025 04:20:44 GMT  
		Size: 7.7 MB (7736131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f794f21f54111e248d9c50528f28477c22291c90a0856e240272a5e684b0039`  
		Last Modified: Sat, 04 Oct 2025 04:20:45 GMT  
		Size: 7.3 KB (7328 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:36ea4018e87900f2c2f46b4a4f43e075c07a731f95892c9565651e5949f8cd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145651201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ba05169c62993c8a27b5e389c11b27851197e3c20c9d91a2ad8a719f0d4d0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d997811a60a9b9144b07fdb085fc1feb6f43f5adf62ec1daf292a386279413a0`  
		Last Modified: Mon, 29 Sep 2025 23:37:26 GMT  
		Size: 48.2 MB (48234517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263fee109e376d69cd8ab45eebe497b85f6bb9dab4d00421e46048f3b05dbc2`  
		Last Modified: Tue, 30 Sep 2025 03:10:36 GMT  
		Size: 28.2 MB (28155087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1c052f36ed7138d27ebb7e300cd8fe66223f9064d8cb89d721192113efa6f0`  
		Last Modified: Sat, 04 Oct 2025 09:22:53 GMT  
		Size: 69.3 MB (69261597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51dace851ea579899ae87626a7f07b318216c47b8a063a387534dc74d137d8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7745343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409df6aa9bb2e21bff6515efeb74cbedafc53773453e5c9798def71f16b5acfc`

```dockerfile
```

-	Layers:
	-	`sha256:d6c39508545d3b4725f80d4150ae87587cbcb2bf2f9d3de52f8b537def3a9802`  
		Last Modified: Wed, 01 Oct 2025 01:30:31 GMT  
		Size: 7.7 MB (7738047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b035baa73b68a360a1cb183da33e8163402c9857155b3e26e40a39a1f50c4ad`  
		Last Modified: Wed, 01 Oct 2025 01:30:31 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
