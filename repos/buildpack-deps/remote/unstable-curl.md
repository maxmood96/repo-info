## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:bfdd50bf11d7b00d434b551765cf401cca8a1d1901af1c6e3d0d843e56035a41
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:897b9e8a898c6b8869a206516b7dd8ab7be3bd4551c93871ec86a444076bd324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75427035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a017aadfd0b77c30e60cb29d02ea1662dfa48fb8a5e0964a0320dc5a4561350`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:884fd6a247b21d0ac1c5a403aa5f764e7d008a8e6de627c0746428d906c5576c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b059e1b435a9b23c17101dac12e97e2858108ed2f8217d6d2954a33a61946345`

```dockerfile
```

-	Layers:
	-	`sha256:8249b1acc5df54ccd582a93bbb6e6ba993ecfbdad74ea92cbc60aba228394087`  
		Last Modified: Tue, 30 Sep 2025 22:36:17 GMT  
		Size: 4.1 MB (4080290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814ff26c901afb69bf6cd867b20411582b48b5fac9adb814b6f1d40bb258952f`  
		Last Modified: Tue, 30 Sep 2025 22:36:18 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9ade27eed61eb9843e2432b8cf87851ddea1895200e89e5acbc2299af1f97eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72121344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eacd4a91b649feca26c148b5bbec732b826e64ca6acadd39c041628c1abb8d1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88ce4798761810f32f50dc1c6ae345870c85df6e9ca32e89392f0293434570cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f21867b8a5b9871620f0e8d048f5d8681c0a202bd718a5737cf38f201f9542`

```dockerfile
```

-	Layers:
	-	`sha256:42e276965178e400c1a0d7ff0f6749e77d891e8971415960294b31e10ef01746`  
		Last Modified: Tue, 30 Sep 2025 07:21:48 GMT  
		Size: 4.1 MB (4083288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d8ab9f20a27982384c3d0378defeeae7e6fb0f501e061e3b85c7b9b043a9a3`  
		Last Modified: Tue, 30 Sep 2025 07:21:48 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:305835cedfb1006a7c1c0e36f6b4c09bb0664ec70239ec1475efad295db77445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69602650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9890c829102607a67c1d066126579b1804e5ef4fd7c88d62598a93af6e0fc6df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:410e9863388c7a21d38fa0364bd31feaac4d5fae5c51ecfcc10007da8077b744`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 44.9 MB (44858795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eeddc4fd7915f74eff81bac7a518e5a7fecd59b3a04c00f06c47816cda9300`  
		Last Modified: Tue, 30 Sep 2025 01:08:10 GMT  
		Size: 24.7 MB (24743855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5b22d8960cb657e4d666eea079f3776845bfeb2d37c35e79fecd93c93fb587b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8681a6ce5bb4aa3bd969371d2d8f08ffbbee1c46ba53374c5614ed9f630450`

```dockerfile
```

-	Layers:
	-	`sha256:dddc07ef2aad9b4601c310282cf1412f1a1c03d20fdb3bf6ebf103d47bed9bb3`  
		Last Modified: Wed, 01 Oct 2025 22:21:56 GMT  
		Size: 4.1 MB (4081780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e84428a2cb3c296dc9371aec861914a7eb35729bc91a69784c8cb74f95e04b`  
		Last Modified: Wed, 01 Oct 2025 22:21:56 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9ae43b3def6aca078862803a3eabe81cf3bdbc9135d4fa2d0de1a3ec8c25967d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74833954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63fce07c803f7908051fb571ab009daa24c45c9dfb34641288a12f2a0c63658`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc77c7b061ac2daa30a091eb0f97f41627da676b88d268d001ddd68a32906cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb378a04d8799cbdacfc924cfab87f05d009d48266ae23cb226b59129e0994d9`

```dockerfile
```

-	Layers:
	-	`sha256:a6c234c2b5d960a49fc2f836eb3d442c08795c23395e2959d3c950cb81a07569`  
		Last Modified: Tue, 30 Sep 2025 13:24:37 GMT  
		Size: 4.1 MB (4081181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6532ec0fbd2c1b975c6961483069c5b23f5698befb221b7950ecd70c4c4dd44`  
		Last Modified: Tue, 30 Sep 2025 13:24:38 GMT  
		Size: 6.9 KB (6883 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:73a5fa4cac13fb12d31d24f184e775745618080ca1590557607f520c7760495e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77875505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8047ae7d0aa855d38fc99e72fa810c58e1d0e9011bb4522a5ffb75db90c6ef7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4bdfca8524e1358569f48a5b54a8909b25e110209aa1567615a395de9171b8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4084195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b565a5bc7f7cb304263a2d3010c710abc2e7daf64c0c8ca3782dbb2d883970`

```dockerfile
```

-	Layers:
	-	`sha256:09020c000bc4d486fc71a7c935fc8d138dd23ee6d19d5697c5b27f64d21fe933`  
		Last Modified: Tue, 30 Sep 2025 16:37:47 GMT  
		Size: 4.1 MB (4077413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b3198d5057ed95bcd96efee431f6c9cbdcf1cdcd7241b631abdf2c44745ce2`  
		Last Modified: Tue, 30 Sep 2025 16:37:48 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0a613478cbb6eee4ca2913b2d33f613866c45fc823b725a20fc0173edefd0b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75458926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9063162ac42e55b603978debc16bc344353fa8842606339afb8de575e71439c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2d5a646cd4284da6560f26bd80a233e437af81ea2e42f0700d6e51c069debba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee02660d2a949bb719ffa0646212e6fdfe32e7a9ec50422028b5ca81f8b3242`

```dockerfile
```

-	Layers:
	-	`sha256:60b807c490b39d4bac3e4a906f0c66b899990ecb6bc0d3a9b204460e8a8b62b4`  
		Last Modified: Tue, 30 Sep 2025 19:20:28 GMT  
		Size: 6.6 KB (6636 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ff3e0b530e2d8d86333064a6e64a90e026779dd304b1e599fe9b72e643853ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81674315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d8cd29e672c10383c87652de0e30fc49c474246bdb5f4fe8928f698f15e088`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ade538815087a0145b6e7eebe8776c271b0753da42498e822d01c70229f9ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90fbc53fb988141552abbcba400119bcb4154765d7bf18ea590ec5cf01c7404b`

```dockerfile
```

-	Layers:
	-	`sha256:13e99f5287322aeeced13db907f80af02328c70d30fa8e0d93046f2368abde97`  
		Last Modified: Wed, 01 Oct 2025 22:22:09 GMT  
		Size: 4.1 MB (4084105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:227fa3a29db8219fb8f095221cf0b3c65c4d8787669d9f2e5a2f180d0780efe2`  
		Last Modified: Wed, 01 Oct 2025 22:22:10 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d4e2e40c89e88a921a07200052f9fa01a11a2d52d74c1490fdfd6b8315bc731c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76015828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759cd6ae890199fb8040deacc6e298266d44922211bc3a42c8304255d4646fa6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fc10d8ea86b76cecffdd3f625918c5f61beb816e2a1f697a01612613bdfa7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70deb93b7affdf67c7a82b5ccdff0d09fb50c8dbba4c3516054708247ef40a5`

```dockerfile
```

-	Layers:
	-	`sha256:838b0399f001f860e3f07a1a286cdf6f5d00fd4ec10dde753e22b170d50263d6`  
		Last Modified: Wed, 01 Oct 2025 19:20:49 GMT  
		Size: 4.1 MB (4072763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6241c0e3bc4f04ee754746ee799fdd95c43cb39c3bf4acbae894c9835f6f2808`  
		Last Modified: Wed, 01 Oct 2025 19:20:50 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:20587676752c5b1d185d1e8566d31d77010952534824ff56d4545abce375f43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76389604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec81f7906dd7e92a0f4f4a74ba3684f4a289d8eed22f559c54e12e0d0fe89ea7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1759104000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77f7891109f7b1f94301cbca7b3ec83d4d86bea19cd316fce7d693ecf9f3fe9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8fa41564b5367e1b7064ef318855270d2fd5601ce869e61f6e4a4fd5ca9dd0`

```dockerfile
```

-	Layers:
	-	`sha256:9f82395411904c312a4bf40287412b09159fc13fccf9ce57e810f7f1b2e71b2e`  
		Last Modified: Wed, 01 Oct 2025 01:30:07 GMT  
		Size: 4.1 MB (4081701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cc5fc9d5fe97f71a7de2e839a8a6f84d66c67f6b4aa7eb54210fe711733b89`  
		Last Modified: Wed, 01 Oct 2025 01:30:08 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json
