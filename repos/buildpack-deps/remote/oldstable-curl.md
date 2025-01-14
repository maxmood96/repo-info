## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:e4681085cf890b13d6ad6e186d9b0ffbd1e16be488c925555167f45c14ef174b
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7a64dd470637e11a06d4334a55bf50c78ae729fe3e700b7dc70bd0bfa6d61943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d7ffbd59cd4b0068cac31a3797e149709b13faf9785c589e5efaba984e013b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1730845ad6ec3c63feeac96fb57dcd512411c023ab54f808582870eb3485f490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4751efcbab8974d36a3026a20d83c34d5e96a17906745e7bb7bb23895142aee`

```dockerfile
```

-	Layers:
	-	`sha256:f067d0d747d5429697f3e0ba51e3d4c50a2c782e615030ece10fe955a616eff0`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 4.5 MB (4485627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c36638c6dd6cadf3d2ff2faf420ad972c0520b72bc5ea9af1db8e4d8de402cc`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3bc819fb65ff39d8d6d3c29cf7feadd21b3c518e9a129cf12a4d137d765b2a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aba920290612b71739e7f66654b2824689756bf1e97973bf0f2bfad2c81357`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:709fbc835081f3d738aefdb318cb058ebdd40a4f2868ac5c5605b614336082cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118f311b73d58cd869f276c771003f99ad619d08e755f7fd695933405c3ce3aa`

```dockerfile
```

-	Layers:
	-	`sha256:1ec0b08d0b6d41a5248c133c7763f4bf635d3e822f0cafe655cea8b68518ed15`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8244277bb9dd34ce818dcebd94b67d3965917748d6b78dc1004c7b49000dbf2b`  
		Last Modified: Wed, 25 Dec 2024 03:44:14 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fc6b203ac7406782c92bdb8077dcbea34f68af7efbf9cccced39d01822f184c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67790153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7111e06f12ed6fb58aeb64d13dbf6b37dccaded16d9738b5981d69432c77e104`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfd6b176342cb480b79cef9a7188364b0f5702ccc77422fcdb5d7d8f3f42c8`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 15.5 MB (15544093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:afcf598dd6028954a3eb82e52e676a77dc0baa075ec1710c1cac1c126eab898c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e0c6dd245e0f44287a0ced30d9fdfced3ae24aa93542905f740d32bc582b09`

```dockerfile
```

-	Layers:
	-	`sha256:95d03d44547af211a4084751134515e54160bc99fc281d9057900ba43fbc0117`  
		Last Modified: Tue, 14 Jan 2025 07:00:18 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ffd977507cd8ce3a94cbd32493472e8045db032053185c721ee2ccd920fbb94`  
		Last Modified: Tue, 14 Jan 2025 07:00:17 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7c9b71ad872a6c4f31f012b9080753aac210f0603165395db90a1e8444bb6baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c876d22bf9fd327d2c5accfbc554ab58b81da45ce58a449fd46d9cf6df337480`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bbc6e7143e715184c2a61944b34715eff9f22c2a6512c93e1c585f06ae1c3153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a71e52cf0f6c153aa98c0a088f1d255490bb16de544d26a08f8a68442e683`

```dockerfile
```

-	Layers:
	-	`sha256:0b0d906f0d39212879670eef18af69544afd030c734ff646a956d7008dc12ab8`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 4.5 MB (4482068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eec984eb9bb26afe266318c1d52e65860eb24666fa5ac68d41240c49cc06b65`  
		Last Modified: Tue, 14 Jan 2025 02:17:15 GMT  
		Size: 6.8 KB (6778 bytes)  
		MIME: application/vnd.in-toto+json
