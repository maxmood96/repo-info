## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:ca86ebea45f6fe11fdeb5641e4458c636cd3a50f3ac98a38b20577f1fb4954bc
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
$ docker pull buildpack-deps@sha256:58e3ab8543976cdef8a421701c35ac0981681c445c24def156a663b10164f15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69299825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f6459c8d5d9d47d0fa2616b36fb580f94717a690ed5c967d32ab68e973907f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b48b9c62791aeb0938bd36ea384553847691ae2eb09c8674024ed9bab24e55b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4eef7300715acbd5bf649442448f814c91e3edd81cc7ce318062eb9ea1dad75`

```dockerfile
```

-	Layers:
	-	`sha256:dc79dc38503e78d12c1b30f402a159fe56c880ed8e7748332c78b8234200b793`  
		Last Modified: Tue, 25 Feb 2025 02:12:51 GMT  
		Size: 4.5 MB (4485627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be30347d3aa47789f020cb647accfc520423ad1d6e5fcd3a9d4388b90106cff2`  
		Last Modified: Tue, 25 Feb 2025 02:12:51 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d095285c12a1b99487b28af042f4ce855d09e71ccf4cfd805149f321614f1a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63698612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb55cfbf146794456e45adaf1201ab08eceffde02bbb25893d450fe648223cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7e0941255238d0b686ba4d057744cdb1334d8412c6bbe0222601c199a7825004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ea4476b8d9fb50bf3cb725815db433c4336d055be7f7d0270018b1fd893d64`

```dockerfile
```

-	Layers:
	-	`sha256:f5c4256cb66c59fa61a61b00edd596fb4ea9df538ddabb04405f6677e4055ce8`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de126843dd3b845a38a5d44d84e924dca553937f671c097df333fd6d0bc14e19`  
		Last Modified: Tue, 04 Feb 2025 10:42:21 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:699d0f65411313f79bde102e935b03f05646e0ba90f9e589b53441d582595934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67789750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6daba633b8e3b34a7f1ce1727329a37c04f9919263899a96fa7cf6ec202154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d5ed3cd0162799c08609a036c8b39212da061b12174a4a202fbd657186c301d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c58d44733426488446ed36c9936b91cb83423e352e68b6fe40e74bc1561106`

```dockerfile
```

-	Layers:
	-	`sha256:87a5d01b879d7622edad54e86b025c3a014ac7f446b1556f2f242b7a52f27181`  
		Last Modified: Tue, 04 Feb 2025 09:00:32 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb2dad3364e37229e045f4ea4ac1d95ca1f1dccbe56ba9ffde542f483711d0ea`  
		Last Modified: Tue, 04 Feb 2025 09:00:32 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a729e51ec06cbe12f4dd1bac5ec38a821438026cf63b12389f9f009fcf6bd122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70741040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6b72f777b453b90ae6a87e82720f95913fd7c7a8e8ede878a7312b2a19964b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66e0de36951c27f66704e8a03a544133f2ac0c265e20f27c381d8730ade20b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4488847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430dc7366b29e64df776173f933700e1e1e9e7821f3aafb306e09b26525f4220`

```dockerfile
```

-	Layers:
	-	`sha256:6dd9e93e817c91e9b7fceb5aa4b77a47b1cdc4f406bcdf975029b5d2b10ca0c0`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 4.5 MB (4482068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:792c2cc7fcaf0af63428d36f8c73794d8735592ee847a9deec17387aa70b87c9`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
