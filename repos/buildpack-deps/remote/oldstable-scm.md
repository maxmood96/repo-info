## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:eb1709ff3656e83eec509352115e84944255b4ad964dbc78a0c86a2c7c71d566
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:be24f8797ed5230c6fd3860363573ea858436e97936e87ca3a63b8a119617bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124051060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a685de74d3fc8deaa1f3590389cc18856dfb1e9877bc897066dbc4d0cafbc0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 20:33:12 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:930cd5bdb7ee84526911fe15ad484e5623938c69db10fec1889cf6f8458eee9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c34e429cca43ca9bf0e8c90dbc9af49c12a68d8599f448c5c6804018af4ccf5`

```dockerfile
```

-	Layers:
	-	`sha256:e857d5533f06601f914b909b042ae13ecddc2574e60d3426e06ec85ba184cbee`  
		Last Modified: Tue, 14 Jan 2025 03:18:10 GMT  
		Size: 7.7 MB (7708168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2b8090556ff4d7a861ca11dceab6b93c707353f0eb17dfebc061e6a4a22753`  
		Last Modified: Tue, 14 Jan 2025 21:01:13 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d774943785660ecc2de823027779a925c87651bd40f06fbc6b58b9de1c8bd809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114339540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5ee24dd46e5c5e26ee74d9f511fcc3735ef780de9003547e3a914b976008fd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 21:05:11 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681398f28ce19a7af317e3774529df465ed1770ca10164fdba3b20f23a5d8026`  
		Last Modified: Tue, 14 Jan 2025 16:16:27 GMT  
		Size: 50.6 MB (50640646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c91b0f90f1ef91ce5f6c48aadb2477540546f65adf63b3d90982ec86f15a6be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7716983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d58caa9f61dfed2e570b426db1959ba75ae97217fa6a9a80716c68ee7e4355f`

```dockerfile
```

-	Layers:
	-	`sha256:d98b7e41b3cd63c512f218dfab9c9d65b81f3eea63c8b836f660301b020c5d66`  
		Last Modified: Tue, 14 Jan 2025 21:01:17 GMT  
		Size: 7.7 MB (7709570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3bdd7383a4b1f4d3f50aaff18c4c7bc58547a6b215c9b01676e6337e8dfb72a`  
		Last Modified: Tue, 14 Jan 2025 16:16:25 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7cd12446ba7224b5c2917b1c38ea6cc66ca5d1b816e2220b6746099844d83a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c009330911b291df3f419696b4f356ad17a61817d491820586e38c2b0009d1bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 20:36:01 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 21:24:41 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d23ac0e9b25076f1cc90469f31bffaae783c6a3a88272620af5e7dcbe0b8202`  
		Last Modified: Tue, 14 Jan 2025 13:31:46 GMT  
		Size: 54.9 MB (54852602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c15cf8ae3f7c2b7a8e902962590e6c9064ebc3de259521e75513e13f2e9583c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea1bc11e1597522ba927e7cf032ac12c2f5c0b48f76688a2c41cc8df5ff6d4c`

```dockerfile
```

-	Layers:
	-	`sha256:cb5b7433e723b0023aeae558a9a132cd43f7fd43bf007e6f3bfc19ad25dd8b7c`  
		Last Modified: Wed, 15 Jan 2025 06:00:35 GMT  
		Size: 7.7 MB (7713902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1092df41e57f424822625c9e363e68af5c5429b0bfca3a72c6d7952e77fbb0a`  
		Last Modified: Tue, 14 Jan 2025 21:01:18 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28e2e646f6d43fa1efe2cfadbefcfc97d0380f2fb1fcf337ab186a6a7694becc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126765398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0118d9983c200cc656718334f332c8d84fd5f7bc12e5554cf8ea29c7b2feff6d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d0c381a5fdef1263d351e698c4afefeb15eebaa7c61c01a804b75362d039c4`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 16.1 MB (16061977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b411024e8ae7dadedef448d7486b9035f3faedd43c62d2f773ed5d8f87362be0`  
		Last Modified: Tue, 14 Jan 2025 03:18:01 GMT  
		Size: 56.0 MB (56027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5c522c409986d11759765e3e0c479a45bd072e556e7624ee98c0c73c3835010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7710987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a548352d1deb18bb7a6cda130a408e2c0be735494fd19641527f0595103f0137`

```dockerfile
```

-	Layers:
	-	`sha256:4e73f9ec08e9cbdf6da3e91919fb64cbf348bd682d5f59e968e2c1650d71f9a0`  
		Last Modified: Wed, 15 Jan 2025 03:04:12 GMT  
		Size: 7.7 MB (7703658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05bdfadf9495531b969a4de7992a3cda944d204af076ec81c8f11114c1abed82`  
		Last Modified: Wed, 15 Jan 2025 03:04:12 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json
