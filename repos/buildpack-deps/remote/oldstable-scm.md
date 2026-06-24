## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:fddf06fe45b6892cbcbe1a74e046f64bcea06caece29d22f0d257756a4eb43bf
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2d5fe1617c7662a6521881c045556508a8ce951b24ec923c557abb044deffae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (136950273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d145e1d579130e128e8182fcc7fa4eb40709f96e57749a75302103d9bd662423`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c68bc2063683c3d15907b8ed1b777cf14ca153c6f8e5b12db0868dfa7e38a`  
		Last Modified: Wed, 24 Jun 2026 02:28:33 GMT  
		Size: 64.4 MB (64404017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60b3de5aad8a8aef56ed4ba20a6ea2d11d52bc66c15e982837a60552e8c50c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d7556edbb304e085047ff7c473e543a77183933c2f29e845d52683de16e9ad`

```dockerfile
```

-	Layers:
	-	`sha256:97b6fa7156e084a55165aa3dbd1ca509ceaf8e5a12f9963ebb49694f8ae98ce8`  
		Last Modified: Wed, 24 Jun 2026 02:28:31 GMT  
		Size: 8.0 MB (7966088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a81408b693097efd7c56b6e24ce47a97c6a3e171ef228a65b191fb03166139d`  
		Last Modified: Wed, 24 Jun 2026 02:28:30 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:367f69f9727d8f09f484d261dcd2b159995aefe27689a47d27b8435cc277ef9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130779033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f00f666fc0221315a8a5e98098ce3f5dcd2db5e1ae0799b1436a9522992bdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:19:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b6f26285ba03744a306577b3de61c2f71cba83b0beff1d4a59aef5f7dab736b`  
		Last Modified: Wed, 24 Jun 2026 00:27:23 GMT  
		Size: 46.0 MB (46038207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2576c00204f880be8e3a137f521b0b0f1c2054ec6a7e9d73dd6d20fdf1707cd9`  
		Last Modified: Wed, 24 Jun 2026 02:19:23 GMT  
		Size: 22.7 MB (22718190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81160f0df179da45da421db0ce97a5d8701f99ba34b208c1f3b395a79afd440c`  
		Last Modified: Wed, 24 Jun 2026 04:14:15 GMT  
		Size: 62.0 MB (62022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:435740f0746618e9aad04a43e0f3dfe1043ac1fa4a89895af6e53cd39797c263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7975320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10151832d23d43af4b92993843e1ad7c1f4b2934ca2dea410582d9d01eb667dc`

```dockerfile
```

-	Layers:
	-	`sha256:938ab6520a9c617f653ab2a5f211125d5a5bf22b373fc90543df597a46b5b83c`  
		Last Modified: Wed, 24 Jun 2026 04:14:13 GMT  
		Size: 8.0 MB (7967946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4f3be942237e3933921e90fbada52c81fb92190a962f934ec0cf08c809259f9`  
		Last Modified: Wed, 24 Jun 2026 04:14:13 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ba6e6b586e3270aec73812c47265145770cc9ef6ca9568f0c609aa50334e38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125820029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f026e602c1fa7681c498a15b7d674fb28ad7aa0289db5c74efbecf3dfb2bad09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3622debffba3838b917703fb6dd9c161a4d93d9fd97c61d3e8400a2245f93c67`  
		Last Modified: Wed, 24 Jun 2026 00:27:30 GMT  
		Size: 44.2 MB (44208145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0df8de55f365d832099cabf27409104999d59b26292d91202ca6e160c4b513`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 21.9 MB (21949935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16c85bf5ff1b42ae66f83fdb64a6cd05a854ea2289dfe1b0ae9e4ee6a806d0a`  
		Last Modified: Wed, 24 Jun 2026 03:54:41 GMT  
		Size: 59.7 MB (59661949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87710cfdb47d95f845bd3254fb13b06c5ff9a7634109d00e93d60d8918d0ff24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7974739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27570a1f28f7de2f6e7a0d69fa8c48b5f00a4e44a8546e48c29ebda4142c749`

```dockerfile
```

-	Layers:
	-	`sha256:00b83188cd84faf647fd430f94717e95070e638061aaaadf6cdb96702a6203f2`  
		Last Modified: Wed, 24 Jun 2026 03:54:39 GMT  
		Size: 8.0 MB (7967365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc4e25a43f9f4dc8b5825308b9e79857e161d8715d6adb9ce4bbd4c7fab762f`  
		Last Modified: Wed, 24 Jun 2026 03:54:39 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b6c7621f7d37399c56d06c44ea04f19c77ded98c7b47aebf09caea2a655e88a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136490223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d74423d6ee50de698fe611f29309318204dbb926270d8a2be933ce2c72760dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebca214f1a4b66acfdb0bd20aa3ee139d1747885ef4b0f3d07aa2a68459230`  
		Last Modified: Wed, 24 Jun 2026 01:44:48 GMT  
		Size: 23.6 MB (23613316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb0e918720911be6cb7a1a5ba9ad0e1a308fcbf24961a23aba0cd220df6cf`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 64.5 MB (64487706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7fe1bdd16fa103ee8c90fe515b14bcc92ce393f1698c0a4ceda1b360653b43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7979871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd8e38d78ae83b07fd4bd6e90f8a09e4ec5ddcad8bb59cacbad7281c98a4747`

```dockerfile
```

-	Layers:
	-	`sha256:bfd71ce49561286d5581a9c0b2fbedfd023f8657f3fe5da56be0759cc2fec865`  
		Last Modified: Wed, 24 Jun 2026 02:35:26 GMT  
		Size: 8.0 MB (7972481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a6dcf4aa907dee578d91dc58f59e077340c979b08e470ce225afb86b2c2cc9`  
		Last Modified: Wed, 24 Jun 2026 02:35:25 GMT  
		Size: 7.4 KB (7390 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1a1b0c3177ce9e8159d2f6cd4657f2e05d6dbc48f47ff6b28a4fecf12aee541e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140615322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4606e22fd7500244d43e0444483e04bb341a80f7be19abfdd8ec46d909f5df4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45c9ce5ae5ea6ab37787312be8b0a9732642c1221f97d5689baacac874b4cd`  
		Last Modified: Wed, 24 Jun 2026 01:43:48 GMT  
		Size: 24.9 MB (24879740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db0110899c29fd647e62f912bfb740fc8af5310cdc227454d8f086f16cba33e`  
		Last Modified: Wed, 24 Jun 2026 02:35:05 GMT  
		Size: 66.2 MB (66244204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:189920fccc0c5d5aa1d24fa619d7a657cbe666ac87a7030edad7696af6e64b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd852cbe048f746155f4bdac8b1570f3daf792f8edeaba6810f46f55b4e3f6dd`

```dockerfile
```

-	Layers:
	-	`sha256:9ec287d25b458dbcb468a96daeb6515d98e9238d0c6467ddeab88d4d0e278023`  
		Last Modified: Wed, 24 Jun 2026 02:35:03 GMT  
		Size: 8.0 MB (7962246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ab9ba46f0ab35cf1b9bd7e9917548f5d07a62067502e1a2e6ece7cab919a1a`  
		Last Modified: Wed, 24 Jun 2026 02:35:03 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9fbf398f349de348f11af45a3a8d354265f7f4fbd20acc4d88ae4c80695aaead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135732593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565bac70ec79e61dd48d7027cd63a0fdaa34809d4390e38b96b58a28733841aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 14:04:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 19:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d06e8744a62761c63cdcacfb2a61022e2f4c0aa854b6cede18fced28342dc1b2`  
		Last Modified: Wed, 24 Jun 2026 00:26:53 GMT  
		Size: 48.8 MB (48792819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a2f466b887b6a2a52424171128948207dccef13979fc60f50cb7beb67f123f`  
		Last Modified: Wed, 24 Jun 2026 14:05:16 GMT  
		Size: 23.6 MB (23623971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911f76b03057793439aa57a4c1f92b3f5d8467508369f84d1b616a44d437f66f`  
		Last Modified: Wed, 24 Jun 2026 19:28:16 GMT  
		Size: 63.3 MB (63315803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04a171344b4e2bdf90c21248406ff02716a7fc649af35142dc0ac8dcddfaadc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db00fd9325ce69f50825a6fa556223f7d3fa71d2b460a9ffb79a3f13874668f`

```dockerfile
```

-	Layers:
	-	`sha256:d6a4588660ba04918c4c152b142690101bfc825da0cf766536007a8de5b5d6ff`  
		Last Modified: Wed, 24 Jun 2026 19:28:09 GMT  
		Size: 7.1 KB (7143 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a3d5d4f67ccc8d369efee25f591b5dfd482cdf714b32ccc75a43d614da8b57ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147887414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f1c0c3accfad56d4a88e1dd2d6edb422dbac6c0e4d98b60d3a33b3fe795754`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 09:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217268ac6656bd05839d5770fe7b3c0c976d29750b0c5635d099e473a789a10`  
		Last Modified: Wed, 24 Jun 2026 03:25:44 GMT  
		Size: 25.7 MB (25687048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6542f967f29885e49bf508e83dceee1eda4fdb044dcd68c1237588f15b795e2b`  
		Last Modified: Wed, 24 Jun 2026 09:10:08 GMT  
		Size: 69.9 MB (69853519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e60d8361639637a2652672fa2e784375dae317e0289963a967815a893077313b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7981303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca75c2a242a31384d6e7151cb879003f73f7717e0f7c83659c6b829e774f5ba`

```dockerfile
```

-	Layers:
	-	`sha256:2653d709f78f5d54272f39f169ce722e3c15bc76c4bcf3a506d983f3252b0240`  
		Last Modified: Wed, 24 Jun 2026 09:10:06 GMT  
		Size: 8.0 MB (7973961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e56189e30c36ef75e826b007469a9e1986e1284a8f1e00880d301c9aa7c20fa`  
		Last Modified: Wed, 24 Jun 2026 09:10:05 GMT  
		Size: 7.3 KB (7342 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a538cf04c1f605666270b2ebddecf2a057ac6cdcda14df5b6757c486ad2df17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134698939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78444a80e84f1229b386219e943537d1f89bb6788cbf6667d1bfdc4ca0c15654`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:45:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075239c7f31ef6bc9923503289fbabd4a216a0cc1314ab546cdb22b3aa178273`  
		Last Modified: Wed, 24 Jun 2026 02:46:07 GMT  
		Size: 24.0 MB (24038997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98bfd0e5e3c41d5610549c351f2a214a1057c70f21ae763c153398d8481275e`  
		Last Modified: Wed, 24 Jun 2026 04:29:51 GMT  
		Size: 63.5 MB (63498267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ab6f6c4f884ab4ec4e709b7dd5b4d685cb55b8d09af824024ad029941f220e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7969711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64983a2ab05c6472a33e7d9faeb85bcb984797d3f005930424c3e92d401a3622`

```dockerfile
```

-	Layers:
	-	`sha256:b565afcfa4fda8c277ada0a3cb65ee7bd7ad249e48fcc67b82d3fddd3a5f6275`  
		Last Modified: Wed, 24 Jun 2026 04:29:50 GMT  
		Size: 8.0 MB (7962401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f51365212f9213ab73ec9d073d56f0a5d42065ade54b2be0ba5077250f94e29`  
		Last Modified: Wed, 24 Jun 2026 04:29:49 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.in-toto+json
