## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:845de4a60c3498098593185102842603fd86f171c9d51bcf4187a552ceb04f5d
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; 386

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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
