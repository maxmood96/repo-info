## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:19ec5ec8ffd70993d362f8578d906b2d0205ed6660e6baa1a7c23918e6972502
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:479db446e61edef3b8d3d310a3e61dda7a9728e36113872f26ca3a7ec42fc519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124277744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dce43685cdde11b0461fc2f23c76e5b6b3917d5ccbff91bbb7d360ea4fabb7e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf4e3059e088f15d90d719c388546de462f8152d07d724a4895907f69c1ce`  
		Last Modified: Tue, 12 Aug 2025 22:15:17 GMT  
		Size: 54.8 MB (54757082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf15e3cb19f8e13ef43e0de927395dc608d675542b40788d4452451f1b148a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c26c813932ecacb060bf3be9a103232890c777cbd33f1a2c94409053dfe854`

```dockerfile
```

-	Layers:
	-	`sha256:21367e3c1cf9315a9061e8e03c90b58ad63219fe138a885dce36b4bb71b4e92c`  
		Last Modified: Wed, 13 Aug 2025 01:20:37 GMT  
		Size: 7.9 MB (7912154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342e7ccbfe7de233b6d5d91d9c13537cefefa42de708e73596d686d37f9bad1e`  
		Last Modified: Wed, 13 Aug 2025 01:20:38 GMT  
		Size: 7.4 KB (7352 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b291fb69a3ef37e64ecb7e57290b52c9bce32f235748b6710a91da853092fdbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114557630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0145941c72629080882575ef04f0d3d95e4d88fbcba27f381fbe015876a374`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:27a0e70a6a342a82d61d13664b90c890c24d71590db74ef7eb6f4dc1b731387c`  
		Last Modified: Tue, 12 Aug 2025 20:46:51 GMT  
		Size: 49.0 MB (49044404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae3c82b80881167fea789bb8cf043d4de732e7b062431e2c261928679dcd3b3`  
		Last Modified: Wed, 13 Aug 2025 00:15:42 GMT  
		Size: 14.9 MB (14880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7e2d995d706697c0af2f117145d4dbab9dacbc5f34e7d500b3d99b0062c6f`  
		Last Modified: Wed, 13 Aug 2025 06:47:54 GMT  
		Size: 50.6 MB (50632440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e983d60db806856078cafe9ff20a5f100c41516b57117b0d629752fc3f9c3c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe3bc545a97914d5e18286c49d63ccd6a72f80de0a94907a3fcec5bfa293ee2`

```dockerfile
```

-	Layers:
	-	`sha256:a39d512d1cb2469aaee7dfeec3e294e1d86755d385e821eb60b72e7363f2ad99`  
		Last Modified: Wed, 13 Aug 2025 07:20:08 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55c474991302cdd3bc2ff3c9914dca95657066924663c8bb88873325b53f0ebd`  
		Last Modified: Wed, 13 Aug 2025 07:20:09 GMT  
		Size: 7.4 KB (7419 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:489497cd9738d2b9c0261381fdba9f682987391f41afc84e2c57c4c81d264fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122855219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f602888aed4a2d6a036cca4b4edbf0b9c62a49793eb6acb7945cf5dc9fb0c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25635cbca821869ea9220087d35fa6b59e758fb2dca635f36530cb5e44b7c481`  
		Last Modified: Wed, 13 Aug 2025 07:20:06 GMT  
		Size: 15.8 MB (15750676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06836ab0250fb74efa819c381a3a62f540817c74a1d0468d4e03f53c6b03758a`  
		Last Modified: Wed, 13 Aug 2025 15:28:22 GMT  
		Size: 54.9 MB (54856134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5b8ae0f63d51fa8390eb102db7427f11e6697c911e96f439b8f25b79f92634b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19aa6abcc4212e131e019f70c8bbb55ef1e71d85d7abded1bcf4957802fe1e3d`

```dockerfile
```

-	Layers:
	-	`sha256:d709bc5f5f08c0c659e20232c2c1dbe08bfdbf94108c7cbcfc011c157da9aced`  
		Last Modified: Wed, 13 Aug 2025 16:20:01 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00ecdfdc03825dda985387c6435ca6863258dd3ecbbb8db670915496336a7e6b`  
		Last Modified: Wed, 13 Aug 2025 16:20:02 GMT  
		Size: 7.4 KB (7439 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:878467f4323a7db542d5fa9e6ac15e489508663b2b075f81d6c2ca2268ab4378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127009493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb4b9dab7a641a9cdba49ca74a7bcbf3a27bba333676840bfcdcd0a6c4685f7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0956db1fbb0de06709cacad88eee1a92edcd3eb326031290d4f6e321e68d7c6d`  
		Last Modified: Mon, 08 Sep 2025 21:55:16 GMT  
		Size: 16.3 MB (16268970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8151bbc2095026ddf31b19dbad5daa6653efd5a630af32432a4736a4ce7bc56`  
		Last Modified: Mon, 08 Sep 2025 22:13:43 GMT  
		Size: 56.1 MB (56050010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a17f0c7337a5eab9cd77a7a4da379bc92ff57b4fa143868a7308f56fd816cdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55de13e7fe329b6d5dcba26e487e6c4916843df3b1bf31aa82f33f75ff463ef`

```dockerfile
```

-	Layers:
	-	`sha256:ecd5c1894f051793e6c86780cfc07e9fe465cdfaf43866a4da3e49f31e95d3f0`  
		Last Modified: Mon, 08 Sep 2025 22:20:17 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0c3f0eed592caba543ac00d1488d0c316f843f08c015c82955d6b30c876ee6`  
		Last Modified: Mon, 08 Sep 2025 22:20:18 GMT  
		Size: 7.3 KB (7337 bytes)  
		MIME: application/vnd.in-toto+json
