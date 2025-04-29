## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:0c30e02e67236a53d3dc341343bfb884f9c9e134414f2488787edcb28da2c664
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:eb6f3c5f3de89f4191b61a355f9b68bfb718c0c015cdf9119267c0ef270a44ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142271941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c628528f1af230569b8092f94dc5e4859c31817f732b02d2ab10ac18479ecbe0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Mon, 28 Apr 2025 21:08:35 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723664ae2848fca92e9c796c763cdd28a6906becf75b0bfcfbb3c85be887d97`  
		Last Modified: Mon, 28 Apr 2025 21:56:17 GMT  
		Size: 25.7 MB (25744486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c56640361c19abf9b8129978ab6e07a598a9c0bf24f8542fd21b2672ca8881`  
		Last Modified: Mon, 28 Apr 2025 22:15:52 GMT  
		Size: 67.3 MB (67279216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b4172989aa183ddf5d173c80637ea2d7ad2a81d114e097bcd88225b7e878506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31b4672c734859a418eeab5f1254031eb2a7b9ce459b4623e38c509d39df4a6`

```dockerfile
```

-	Layers:
	-	`sha256:f0e7130e6e3039089d00fe4416e4a39bdf7295fd378b354fd53aa0c946295fcf`  
		Last Modified: Mon, 28 Apr 2025 22:15:51 GMT  
		Size: 7.6 MB (7591250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25adfdd1830d0bcb7b9497ffbb922a3e232cd34b1421c9c7e1415dec86fd7e84`  
		Last Modified: Mon, 28 Apr 2025 22:15:49 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f70301e9d6d766d5e3c2a66b235913218074b5a2644120b7dba6bc6fe9a379f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135729959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b45a53c7c545c41e03ed78cc47f6d2a09d386e8d331db3ec77aeb0aa662521`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ec645b8b1764e458ae4d21700842e441d914fd80d6e0135fa393952e129298fd`  
		Last Modified: Tue, 08 Apr 2025 00:25:30 GMT  
		Size: 45.8 MB (45786687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9068871a08a0535e32e79d1a45670b225b99f46bbc4e55433b3bc2d040fea9`  
		Last Modified: Tue, 08 Apr 2025 05:13:28 GMT  
		Size: 25.0 MB (25013942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8929ef57738cef401ed1f8ab43e4013b674116ce7a1c298b5e5cdf5147046731`  
		Last Modified: Tue, 08 Apr 2025 08:39:49 GMT  
		Size: 64.9 MB (64929330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54b1135c459db2e28bcb08861f957b3e06feda4fbe93b1b9967c16ac82916a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7592094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:811effbf5b63a29215ee28a087098dc5aa22e46cdad90c68c418d8d06a7ae2de`

```dockerfile
```

-	Layers:
	-	`sha256:3e1dbaaed6d2d727b29be281de0082f54d3eef6e1a43c4c7efce93071e1c9750`  
		Last Modified: Tue, 08 Apr 2025 08:39:47 GMT  
		Size: 7.6 MB (7584720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b38020d05463f0b98f3c91511bd573557c52dc56cf7a4c3387d72f6e6865bf`  
		Last Modified: Tue, 08 Apr 2025 08:39:46 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4ac891368c43dd195f9fb8ab5de5ec16d6e881855305ea3fff7943687f40e630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130607740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b09b9f84bb75491212d3945744d4841682ef429534b89cd7ca46dabdee52d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f935b3012df284a962222bcccf691a593747f69aa524b90eccdcf9bed048a7f`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 44.0 MB (43962830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705c4ef1fc9cf5c68338bdc47ec99f95384a22547d22ce9113fa1a4477154`  
		Last Modified: Tue, 08 Apr 2025 07:39:55 GMT  
		Size: 24.2 MB (24201775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9372173581cf51eee4c98494ac2b0977a2019e7d1175018467ee54556552146`  
		Last Modified: Tue, 08 Apr 2025 17:32:38 GMT  
		Size: 62.4 MB (62443135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4565ad9b7070f810010b43ecb31e74b0ed6663c7069fdf2e17d8bdfdb79a25a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7585638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7a96541ef585966d927cf55ed51303a0e575ee2d6b8846e479c527009608b7`

```dockerfile
```

-	Layers:
	-	`sha256:dba3aa10b1b48408a16bc6962bef1ff7f25172bc73edf6db2d72f308b8d09c2d`  
		Last Modified: Tue, 08 Apr 2025 17:32:37 GMT  
		Size: 7.6 MB (7578264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d0e177b27c9fd6ab089338d618af046ae9ccfc1781f0c76a115769f2494cbd`  
		Last Modified: Tue, 08 Apr 2025 17:32:36 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fe4a5e7bd46833ab459cfdc03f0eacfadaa8df93011e6a601b66be0caa11b784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140892958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac10438ec4afedc3a3db1b2f307698a2896201c58ab03d23f20cb54e550ccbfa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60dbfae895846be1589b057802d5cd4dd276320555a3dce75612dc628209cb7e`  
		Last Modified: Tue, 08 Apr 2025 00:25:57 GMT  
		Size: 47.9 MB (47922433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb7cce4b3d3d4958fcc2ffe1fbbf0181efd0f5febf1b3b140f3c5fb190e3e83`  
		Last Modified: Tue, 08 Apr 2025 06:04:42 GMT  
		Size: 25.7 MB (25728139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bcad993240040602e9e9d51c79d2c2f69a2ce32db81787fed4ac65abcc1c07`  
		Last Modified: Tue, 08 Apr 2025 12:20:12 GMT  
		Size: 67.2 MB (67242386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:67baea24716421b277affc099e6731ac7c16ba60c9713147189d4b3285ee2eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7593467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586acb64f2b3db1f5a83816fe5b519d3a69ee03afff433faad291ccea8855f8b`

```dockerfile
```

-	Layers:
	-	`sha256:6fde004f1d8240c28b9a859da3f8dcd616bf0eebece31daea980ba9d53d7ed07`  
		Last Modified: Tue, 08 Apr 2025 12:20:10 GMT  
		Size: 7.6 MB (7586073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b567220b75d1d5dcb3ee5fe2fc311ac3fe72c05e7889befb395281a69e4ae350`  
		Last Modified: Tue, 08 Apr 2025 12:20:10 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:76862985c9bae4c22dc78e9f7a66e765ff638746441d91ec0176d6155acf82d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.7 MB (146713164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3506433535aa88772bd0643bec1b16fd68c3c104f9f5056303d932f5fd5cc3ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed5e8397bb7752a7889fc6f59947b41ffcc3d3218435299a473ce5a254d892f0`  
		Last Modified: Mon, 28 Apr 2025 21:08:18 GMT  
		Size: 50.7 MB (50743157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec898d3c3ebd3311a66f69a4e126ef0cd8c4ca8f645a36cd5ded8a3f3b5c9e6e`  
		Last Modified: Mon, 28 Apr 2025 21:54:00 GMT  
		Size: 26.8 MB (26775040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08677a88d449eb952fa6d6174cbea68fd7c8c35b56d3c18db1886165ce9a008f`  
		Last Modified: Mon, 28 Apr 2025 22:15:25 GMT  
		Size: 69.2 MB (69194967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:126b2815471425052216402585a4a1c363ce64ef5e05e578c5ab0ad589a9bb82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0378147dad339ff45546655dfefb1918465fcc2b983052cdbfe09c4ca990b639`

```dockerfile
```

-	Layers:
	-	`sha256:bd794f5bdcf032420c12f8d53a61a57c87a266636d9630a35100d9ab59dec4fd`  
		Last Modified: Mon, 28 Apr 2025 22:15:23 GMT  
		Size: 7.6 MB (7587321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3da7dbcd4e7375b0a42b10aa24513f18a2501a02720382e82e3b1c312a6c0d`  
		Last Modified: Mon, 28 Apr 2025 22:15:22 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e32388e39b28196cf9525d9334447ac3f24069a58b4c7625c376d343634a90b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140545770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159abcde53150b095b8b099a1a04ac158d31024d4ffc8c90e532592bbb84480e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:574fdf9455a60a8eef233edb482713c5b89d1180e8a134426313714c5369a364`  
		Last Modified: Tue, 08 Apr 2025 00:25:55 GMT  
		Size: 47.8 MB (47767083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6009983b77d9776ab3b7d6cb770b45be9311a22590aa9a6de0b4730c3af4ac0e`  
		Last Modified: Tue, 08 Apr 2025 16:35:37 GMT  
		Size: 26.4 MB (26374545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158fbc6d91957d6cf889428383a76b4e5c13eb0a5c4926eedd8db6d97f12ff95`  
		Last Modified: Wed, 09 Apr 2025 00:44:49 GMT  
		Size: 66.4 MB (66404142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6da8b66cba65aa6d09f27b22e6fed4be54980fcdc46cf6e6b44a2eeed080007c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91514422255cf44767862a4f0950e1c140cbcd4013be7e0c86966aa77bb33d1`

```dockerfile
```

-	Layers:
	-	`sha256:2ef0c6b361dc02167f20a216e87698cf4ffd08272f4e6cae1008c2deaa264afc`  
		Last Modified: Wed, 09 Apr 2025 00:44:42 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8c689d9d795ae3ee0a31dc0275cfce2441b1ed131a2ecabbdf2cb96dd1bed34d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151568308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5967edd461e25212aa6ef1e7c1e4569ef0e1ad5e2697c7ea7c6b372479a1c59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2152bfaf5665d7c627f661d81f1ebb038ec9b798a3becef3f95f6ec6dfa2adf5`  
		Last Modified: Tue, 08 Apr 2025 00:27:27 GMT  
		Size: 51.2 MB (51205085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0924c3716841f5effee584d0edc58283639e6ed70d2000758424dcc55e8232c`  
		Last Modified: Tue, 08 Apr 2025 04:32:21 GMT  
		Size: 27.8 MB (27841786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd195c05796e75d6c49a1674778ee5cf1851af8875fdfe4f94f09464edecba`  
		Last Modified: Tue, 08 Apr 2025 08:41:06 GMT  
		Size: 72.5 MB (72521437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c9e584fd0fa8c6a76dc5a0fc19ced9e9de61138e1df18693c49b8d1699b4531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf8869e994deefaac90dc9f615cf72048324f8ea957d6755815ac4aa624a4b`

```dockerfile
```

-	Layers:
	-	`sha256:2fc332dda7c0306e039174358312798f0d3ea2574a0194c274df8b412d366663`  
		Last Modified: Tue, 08 Apr 2025 08:41:04 GMT  
		Size: 7.6 MB (7590903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad88d6c17a3b9c6d106a7e7f20cbf15b4c0be571935a0b1d9cc5d49cc314ab5`  
		Last Modified: Tue, 08 Apr 2025 08:41:03 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6afcf371a78005bb5ef196bfdff439422c5bfccddaf2000e2f7ef3bc7c7064f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143368004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6db8263c7996f52ffd0e4749f2c763439b60bdab70e8774b364066eb34c6a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:19a5a2e5eb505d0c1814e6d65469ecbbf0abf7cbe214ddd85cb24c5fb088dc02`  
		Last Modified: Tue, 08 Apr 2025 00:27:13 GMT  
		Size: 47.6 MB (47577872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a838b52d3c41c71c15b487ddc0ce4cada3e3fb6a44e40511f7176fd1633521`  
		Last Modified: Tue, 08 Apr 2025 03:45:39 GMT  
		Size: 27.6 MB (27569332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c84145d0b040e4691b868f5a57cc79bd3be75960c21092b456873daf06064e`  
		Last Modified: Tue, 08 Apr 2025 06:54:37 GMT  
		Size: 68.2 MB (68220800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:150f70f03ed192f9226d94bcdbd708b1ec678966fb6797a02403acfe4c3cf71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7592203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7648ed6e28808fcde7715456b1f8c62f25c1564e78a7ad80a45473c41ea4ef3f`

```dockerfile
```

-	Layers:
	-	`sha256:684f2f822f4774b73a2881fab1738550e1eac9fabaed50f540a4f59ae9a48ad7`  
		Last Modified: Tue, 08 Apr 2025 06:54:36 GMT  
		Size: 7.6 MB (7584889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb1a65a14b7eb02a6a34b49fabe641703700275a2ab45e6f5c99da6dbd78ee55`  
		Last Modified: Tue, 08 Apr 2025 06:54:36 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
