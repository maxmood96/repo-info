## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:12b7cf8a8eb1532e12d731cb60a883c994e16db824b6d9410dc04f3470fbe256
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
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
$ docker pull buildpack-deps@sha256:1412dfc03840fd323b8d2d8f19b7d8355805b5f7c7d532f11e144db422433ea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136859904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a888098749d9ffc4df081d0066983b0bffeefed4cfc8ba634b798e10b682246f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15a0811b2608aa97b4e0811060ffea557de20e605122f0c38825f47469947704`  
		Last Modified: Mon, 28 Apr 2025 21:10:19 GMT  
		Size: 47.4 MB (47428611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453de73db44edcda29182f13881db794c74b0f335096c735f5f88ffb61b994b`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 24.5 MB (24474447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e19d072d3ad687af2af376c719bde109abef8c58cb05b32faf7ed3c425f5c84`  
		Last Modified: Tue, 29 Apr 2025 06:25:46 GMT  
		Size: 65.0 MB (64956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dc679e06c8be5219b394c1eec8cad11ad6b7e8764f232d32ff54213bfc521c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4cf23939981701f244ad0236b28df9016ccc01ba5d3ecfee948fd3528db249`

```dockerfile
```

-	Layers:
	-	`sha256:9712fa778f2f662faa3d0a50fd4885b50b808fb76488f738c4c59a2ec9e215d4`  
		Last Modified: Tue, 29 Apr 2025 06:25:44 GMT  
		Size: 7.6 MB (7598203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd9cd8560c288edf38f090d3823998b7c147fa39f6e10fc9e6420d87ddb24521`  
		Last Modified: Tue, 29 Apr 2025 06:25:43 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e7b975361342aa99185f100b50088f3a0413107b5be475dc6bb5c77127052a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.9 MB (131905483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2290b97599432737e571625265b8df1f85a3048ede548898f6be19545a8ef4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d877c043ab6ec52d6d4eaeab7dea355ef83893e584af00854b55ca611a3bcd99`  
		Last Modified: Mon, 28 Apr 2025 21:19:08 GMT  
		Size: 45.7 MB (45683821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785865296d03ccb31a01d56e5adab53e0c986bcfdc0c9920d48d9b1d2d93eda8`  
		Last Modified: Tue, 29 Apr 2025 03:39:17 GMT  
		Size: 23.7 MB (23738374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e434d6c9a7d808d76e24daf0efac32e9c61b3a7b5f489a41bb49c2842179975`  
		Last Modified: Tue, 29 Apr 2025 13:26:13 GMT  
		Size: 62.5 MB (62483288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0d8a1672ca937c282e5fe0f56433ae573969f90af495d126b87f6b4ce6fd419e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7599123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d326d1f35b8cc39173d833b1664dabe6107f5675ce4a988a78886c1b37634a`

```dockerfile
```

-	Layers:
	-	`sha256:6bfb0a2a3133b5eaa9baba858dd8d414fa9467aaf769f1f4bdeaa09f972bc0f2`  
		Last Modified: Tue, 29 Apr 2025 13:26:11 GMT  
		Size: 7.6 MB (7591749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f75b222ddad45d341088deedea8f3b3fd5f30207aa8ed0d681484dc900cdf7`  
		Last Modified: Tue, 29 Apr 2025 13:26:10 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e9e46b2f36a23cf45dd5760486ec3c94cd7a2babe22e0813da5774777fdb43bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142007056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2c84d5bab1c16cd6a3d94e1f59c3307651d5ac21ebb7ab81135ecb2076bf14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6faa4d9377738e3cc52e5d3cadb55bd77d367fb6439d9d14741079130dc9e4e`  
		Last Modified: Tue, 29 Apr 2025 01:48:13 GMT  
		Size: 25.1 MB (25116968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d10b7fbeb9c563c295c91ba384fe4305118a0d8b88117bbf9e5d4d3c3f9787`  
		Last Modified: Tue, 29 Apr 2025 18:39:19 GMT  
		Size: 67.3 MB (67265970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39ffba9b627d09471c71bb4cfe185589f163e49d0e227227bd50a89e9ae865d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f67d247c9872d543bc2dcac9c5a5bf9b6f09fde360d86e1876f1cb6499cf89c`

```dockerfile
```

-	Layers:
	-	`sha256:aeecb0922a3b1d3710995c9663bc641ef930cb2caa32b28e538fb91fcbc22b88`  
		Last Modified: Tue, 29 Apr 2025 18:39:18 GMT  
		Size: 7.6 MB (7598913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:597ed807e0f36e840b86a5b5bdacfd74e55217f5708e69126d53a3efdbadbdef`  
		Last Modified: Tue, 29 Apr 2025 18:39:17 GMT  
		Size: 7.4 KB (7393 bytes)  
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

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:88d2be4218236fb2eef3d7dfb081eda2123ed01c0afb31884896b0e1b17008db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152752343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cfa5bcc9d6752b022d4db81da3415f38b32fe32bc8a2ce147a71513582b7d60`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed88abda34c2c7766794d61fd8b43cac1ab4eeadc9f85398417820583a09e36d`  
		Last Modified: Tue, 29 Apr 2025 07:48:18 GMT  
		Size: 27.1 MB (27143577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fa77ab766e4eed4e829b6e08390c6a1dc6b2350ee6134f9e56b8061b308247`  
		Last Modified: Tue, 29 Apr 2025 08:30:35 GMT  
		Size: 72.5 MB (72536214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ab36080f6c3c361af82a2d86a977e20106e0990fb4f4542abeef0fc6738ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b010a6d67087304ba741855ac4126845fc1eb73b24697dffdcb65c3a63ae437b`

```dockerfile
```

-	Layers:
	-	`sha256:279c1ae6444f3c665dde4e022a361339957b1ef482fc73b79d2c4f8204a94c79`  
		Last Modified: Tue, 29 Apr 2025 08:30:33 GMT  
		Size: 7.6 MB (7604384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ccd06349b9a6a423f38fa57e22e9f2241541eddb53ae86a6348a143a3db552`  
		Last Modified: Tue, 29 Apr 2025 08:30:32 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:86b67b8d80cbcc5470103b8694778608eeb6e48dc9cc76173fb0039248b43b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138849588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48d619d57c159b2665e0e1fac0b2e7b645df57d20ba735b394494ab8ad93815`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e87a3ef7201dacec1e06fe511cdfaa924c5bf89f4f022c082b59ff14eb11b6f`  
		Last Modified: Mon, 28 Apr 2025 21:16:24 GMT  
		Size: 47.7 MB (47740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b410971d43e4d351db365aaa47795c79f72faf119ac6c217623f17c39d9714c9`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 25.1 MB (25062721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c741c2f68d1e90ffcc6854d741c8a67c48cfcbc304e660bf2ebfbaa12e1eb21`  
		Last Modified: Tue, 20 May 2025 21:41:48 GMT  
		Size: 66.0 MB (66046518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa8724613d780dde10502243003b9f836b122d05b3370ebdd22fc22bd1cf3bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7575298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424b3a4da8db01094d20710f9946357e16266d42735c29c75558d2e83f023fa1`

```dockerfile
```

-	Layers:
	-	`sha256:bbb6a14cfd75e844711b4fbf82b8de510938e6fbc4cd34d502926e7f4cab92b8`  
		Last Modified: Tue, 20 May 2025 21:41:40 GMT  
		Size: 7.6 MB (7567952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a17d283f7bfbbc4db0e5d53f0e26ebc59e1945d92662d71afd2a9acdbd28012`  
		Last Modified: Tue, 20 May 2025 21:41:38 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7599203c83c28f74a5f6dbd6c45154d089670b7a8a6554fcbb5aa46e8f0ca13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144551237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278b8cebe082d42caa4a6222d639ec76b8152f0e91717003b96b438e827285b3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2dfe09dce90ef60478379ac93bf4db4640c14411109c4ddd5060ffa49cdfa1`  
		Last Modified: Tue, 29 Apr 2025 00:02:32 GMT  
		Size: 26.9 MB (26932582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683df7242435f0ea9a0034ffcad35c09ebe0ed400dc39d5de0e749bf3bf141b1`  
		Last Modified: Tue, 29 Apr 2025 03:00:34 GMT  
		Size: 68.3 MB (68302009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a2e78066a2a3999c00d11df2d67cbd6d2cd06b2be689b3aed428d8d178e1fb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c868da5307cb540c135b927981f9173febbf221c7cc2d2d7705ec831311ff5a9`

```dockerfile
```

-	Layers:
	-	`sha256:e0eb794b3efd94a295a01ca43ba194ae1519115b8e4563be50f3a405d07b2b0d`  
		Last Modified: Tue, 29 Apr 2025 03:00:32 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1646ebe9f132b1fa4bce0cd295eb7f9dec03ea39454778726210cffdea487573`  
		Last Modified: Tue, 29 Apr 2025 03:00:32 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
