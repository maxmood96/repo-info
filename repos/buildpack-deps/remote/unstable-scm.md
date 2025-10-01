## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:ce86724062653ee89d0a1ac60487a33f4ff3ddfb3582389f538fbe5ae46763cf
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

### `buildpack-deps:unstable-scm` - linux; amd64

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0856de76cc89faee049d944fa0bb2aeb348092d7b53a34004861e93f6d396048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (138018701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5786c740a828a06eb100ba48674489641dbd707ee594bec2d1a5edfa1efa4d4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ad1c1ed68f65cb1c94163af3a8f54c7c8b00cfdd4c1c64d4129035587399407`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 46.5 MB (46536602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f466521323edb154d60c581fdb38dbebed8f12bec478faa074c4c81846031`  
		Last Modified: Tue, 30 Sep 2025 01:01:28 GMT  
		Size: 25.6 MB (25584742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4855b9d94c21523e35393e46e12e43c1c3dde8d121a86df27935bbd16f5115c`  
		Last Modified: Tue, 30 Sep 2025 02:18:23 GMT  
		Size: 65.9 MB (65897357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:62b05db11bb0058c21d4db3f0b2502d543f5ebca4b339df956243c76e2d9fead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7745540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d8adfe326b6b27b130554bd7b0b6802a89e86cdd48ab187456eda59b1bebdc`

```dockerfile
```

-	Layers:
	-	`sha256:0357265ab1c3b18a28b4419c52bae9b8107d384034dba493be4bafe414e302b5`  
		Last Modified: Tue, 30 Sep 2025 07:21:56 GMT  
		Size: 7.7 MB (7738179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b71d4164154b2bac446dd3bebad06ab87b12e554a780f3edcdd860d9404d79e3`  
		Last Modified: Tue, 30 Sep 2025 07:21:57 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0cdba8e04b14acaac47ff534c7fc5bdf2f60db8181911a5addbda35ceb620f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132930871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd76f4a3b8950686cbadd306d7aa8bd387f3f1b66ef8b1e6164bb02d37bfce6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d30a0c5c579644a88a894fd0b1f1db229651b30c974b07aef6ab9bcde5b64440`  
		Last Modified: Mon, 08 Sep 2025 21:15:47 GMT  
		Size: 46.0 MB (46006695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf528d0788e249a97adf6d73be0b9ae329c2651a09b55c47f7bfbe9fc96a9cd`  
		Last Modified: Mon, 08 Sep 2025 22:48:40 GMT  
		Size: 23.7 MB (23710180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717220db35946b78b9fb18d38321ad58f2681e6386e6e8368e047874b841311c`  
		Last Modified: Tue, 09 Sep 2025 06:19:30 GMT  
		Size: 63.2 MB (63213996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:386f46d7c22716e49960956217a5ff81ce502a865be4944e9474206c4eb5ba64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8267cbad4aef56b48cff3617497f6652caa7b36c58d5bc6e95cb92603b34ec6`

```dockerfile
```

-	Layers:
	-	`sha256:9bd83afcee8b648362142b9383fc6a6c69309b50d2272417494cc621d2d0842c`  
		Last Modified: Tue, 09 Sep 2025 04:21:54 GMT  
		Size: 7.8 MB (7770956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df4b72b54efd25fabc25ec283658012f24fe5378395e8e75e1ceaa05df06d89c`  
		Last Modified: Tue, 09 Sep 2025 04:21:56 GMT  
		Size: 7.4 KB (7361 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; 386

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

### `buildpack-deps:unstable-scm` - unknown; unknown

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

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d738329437502b669e772e7d295d2063b83f036fb2d371defe2a2603b7e09c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142883769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5db20af0230068e1698ac5589826ea5fc56b66186c1ac0cf1b5340bc7d459e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e92e35711c7a07432f12289818406bab4746919197592d38fb8632974832ff9a`  
		Last Modified: Mon, 08 Sep 2025 21:18:22 GMT  
		Size: 49.8 MB (49822261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5720cce3339585de6afad24f3a7efc526d8b9755873fbcf07a2420b66b3573ec`  
		Last Modified: Tue, 09 Sep 2025 04:23:26 GMT  
		Size: 25.8 MB (25756499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb4a8a71b5336697bb6c651f14886de4102aa103fde259ca53a8220e8dc6746`  
		Last Modified: Tue, 09 Sep 2025 17:48:41 GMT  
		Size: 67.3 MB (67305009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8fd3a2b2fe3eb3d61c57cda8df34cd73aa5a955b06b2a904f73ffc46ffe0113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4988746c5974bea173a29e007f4c2f34595ddb50d951837a3d598849b1abbe63`

```dockerfile
```

-	Layers:
	-	`sha256:4d531b29ea61806a8ada6fdd1f8365af5c01e94a046ebdb5f2e1227a9b7d7a0f`  
		Last Modified: Tue, 09 Sep 2025 19:21:10 GMT  
		Size: 7.1 KB (7130 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b263e008b06055da328b1f498e32c20a82ba11dd27c59f5efd9c2b791225fd8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154175582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092c48609cf218774f42455413f255c0de2231bd13949ef2f749b69d79364525`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:772eb1186277ef333cc2188830519c27192dac48fb00016f4bed1d6fb65f0e2e`  
		Last Modified: Mon, 08 Sep 2025 22:22:18 GMT  
		Size: 53.5 MB (53458792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383909d767bd90933a41650a2f22af3654b67dad5eb9eb12c8f0c5d5619ec04b`  
		Last Modified: Tue, 09 Sep 2025 03:12:59 GMT  
		Size: 27.1 MB (27099124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21675bb5849f4e08ff04ccc490a1604dc152c26899ff15f1b7123fdb165262d2`  
		Last Modified: Tue, 09 Sep 2025 15:27:53 GMT  
		Size: 73.6 MB (73617666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db74429c766917a247241aae9981d553aaf26091010775f3d0700cc2883f0037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7784885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f81d5d78b677188ee7022dea0cafa367bc8e01da25fa7d482c64ecca781996e`

```dockerfile
```

-	Layers:
	-	`sha256:738b71b2be435cfad62a58b4a2a32c49e005bb8355e72496cd9342a9ad6324be`  
		Last Modified: Tue, 09 Sep 2025 16:20:58 GMT  
		Size: 7.8 MB (7777556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5be2bd4149b6996278519f613b197c8112acd3bb66d76f1a26fa9f4090a20d`  
		Last Modified: Tue, 09 Sep 2025 16:20:59 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a60e44821ff1eac1493f1d9ce9b665bac47e8b9dea70412b701591c00ff67726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140344285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec57c9015beb0e5f4b82331fecb4a8fbfd8cd6678afffb6716ddd7f3d6e2664`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:347be58a551dcf8aa3dd300ae844cdfc6ff2cdec19870bd090fdef86fdd7d393`  
		Last Modified: Mon, 08 Sep 2025 21:38:55 GMT  
		Size: 48.1 MB (48052647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a5a581d6d2c97cf774bc90f07071cf2fb0f1b3c0571346161822b7094bcd3`  
		Last Modified: Tue, 09 Sep 2025 09:13:34 GMT  
		Size: 25.1 MB (25071945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db66c5e84f1e64845f6aff4b1b0ac7d573e0b57248e1ca5ccfaf4eba4dd11ee2`  
		Last Modified: Thu, 11 Sep 2025 19:17:11 GMT  
		Size: 67.2 MB (67219693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f512908a634ee2b8150d4d21a87404b9121fceecf7d2c7bba09d419d00edfe20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7767588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316fc4649ad7916e9a29490161717e93fd80bf677e2158c2072affef480ebf3c`

```dockerfile
```

-	Layers:
	-	`sha256:2263506e812637cdf3cadbc5ff04087605f043c19f4a0ecaa01e4dd92e574990`  
		Last Modified: Thu, 11 Sep 2025 04:20:47 GMT  
		Size: 7.8 MB (7760259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1626cedf6c825679b91cc3acc46d535f233694009452e817e2e0fc153025fb`  
		Last Modified: Thu, 11 Sep 2025 04:20:48 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:35919d1cfcf2bc87cc49636abdc5a135ab392ff5a55b51c35aae3eeb19855329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145714055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f779c84511a1aaf7fda5ed5c3aaec13a07430d575ba748214b45038feab8575c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1757289600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:75e6f7d74f7a64a858e5c9cdecd19e5f33e99956d1f33d14985ac51b655eba01`  
		Last Modified: Mon, 08 Sep 2025 22:22:23 GMT  
		Size: 49.7 MB (49652038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f495f7a03a882cda8ba1cac3fcd8e67045987237ece386400cab302efabfe1`  
		Last Modified: Tue, 09 Sep 2025 10:20:34 GMT  
		Size: 26.9 MB (26893291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a29a0faa66c0d5bc6228e67d1d922c479797207d6a82c57cc284e6c444b5ac1`  
		Last Modified: Tue, 09 Sep 2025 17:57:25 GMT  
		Size: 69.2 MB (69168726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e4dfb0ec934ad3c1c3af17d5bb6ec7d404c96b0f74614fee9b30c3169c1bd245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7778666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399270849c32547bad7efd15345cb35a023ba7af3755164740c61bb65e669117`

```dockerfile
```

-	Layers:
	-	`sha256:262d3d3abcd873bd29005e1cf57a37df4622b86e7360df36aca2910c43e52f27`  
		Last Modified: Tue, 09 Sep 2025 13:20:53 GMT  
		Size: 7.8 MB (7771370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6f47d8b471eaf0f99743dbeb9236862bb81f040386fa3d36e628eade19f89e`  
		Last Modified: Tue, 09 Sep 2025 13:20:54 GMT  
		Size: 7.3 KB (7296 bytes)  
		MIME: application/vnd.in-toto+json
