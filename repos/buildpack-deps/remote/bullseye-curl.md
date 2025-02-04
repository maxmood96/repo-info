## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:e2b0ba41a527ae2c8381d7e2a8658e37dec35aafc4922efc6d344b9d802566db
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

### `buildpack-deps:bullseye-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f278ea0e1aacd2ac3d797daf838446f76bb7fe002dabc269e3d32d27f939f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0422b90f4807ccd9614ef9118463e5e80990c61726943324bac5a3975fad401e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 01:36:37 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c10d26009d377cac6e65d06092dfb61fd1d729963f4514dca185a4cb86d039c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855812a9ac3b6ebaba4c3495c0e7c909ee453450b17678849e202a3eb77091b0`

```dockerfile
```

-	Layers:
	-	`sha256:1cd436b097ec741147c69b351e4e2e79a1af953b797934f02c828121818aa7d7`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 4.5 MB (4485627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1e31308f71b28230d96394763b0aa71c5225339cda77c606855758ef2d769e`  
		Last Modified: Tue, 04 Feb 2025 04:37:42 GMT  
		Size: 6.8 KB (6800 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:767b2203b916544bc6fd96e3bbc10abd889d47d074ff29095e88444ba41d2497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084f0ad1b3c54358c0a77b1cd44ec66f929793da7d6aaa8ed7f55cb71250354d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d8b4e71b0057b288fa0b7cf9b1d15edc9bec9dc37df63d3463ce28e4f414dc9`  
		Last Modified: Tue, 14 Jan 2025 01:35:36 GMT  
		Size: 49.0 MB (49025062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7055bc7f040fce3e9b8f05fd7f56b8a568950e082ea8ea3aa96cf99f49523ca5`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 14.7 MB (14673832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e13ecefb18aaafedaf409af698fa7126ba827ba4e354cae865b9e9eb4294b5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b98974f5b8914c4e909819d86a041d28830762b6219a0d0f617135b2450c151`

```dockerfile
```

-	Layers:
	-	`sha256:8d45b3795921c8aa97cdeaa25d8c28994a35982ee349414402b5697365b07129`  
		Last Modified: Tue, 14 Jan 2025 08:58:39 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c65c95730cc18c4ed3307699b4c0ae87ced96778d931a1fafbef63602ac99e8`  
		Last Modified: Tue, 14 Jan 2025 08:58:38 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

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

### `buildpack-deps:bullseye-curl` - unknown; unknown

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

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:fe810b67717e1433e97cbf12d1c8cac82a2bac40e14211e3c6b9164d68cf85e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70738010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b913c0ae133558275edee8f3575418d30a1f8c5cfe7b0861b45e33a499f4d32`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 01:36:38 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 04:23:38 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f08e0e3e50b65e876418183cfadf4b9d25087eae4563596822b7cbdd5b537b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8d4a982f05b421f194496a7acb871eb45d55828addd847cd37b531dceb1e2e`

```dockerfile
```

-	Layers:
	-	`sha256:eca027a0d706d22c12a86d884435eb6e047b4cf46c279a5c80331993e00d3d10`  
		Last Modified: Tue, 04 Feb 2025 04:23:37 GMT  
		Size: 4.5 MB (4482068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f26919f0b635f677f0d4b88840cf876653771192f92c6058a0ed2d4a72a971`  
		Last Modified: Tue, 04 Feb 2025 04:23:37 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
