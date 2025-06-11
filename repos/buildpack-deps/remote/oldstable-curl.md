## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:6544225f14b17a98352c7e7a1703be19756d8a0def5f21638f6b9d63b1a3fc18
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
$ docker pull buildpack-deps@sha256:515fcf04ba056429ebee62fbcf672d2bde08d5805830b41124968ac08648a121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69519921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86b5eb1a082675a1d80dd116530f6883f4b835bf6cd797cba679170e7dfa3d0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8156a957a8b63a670ed89130a2e1eedf5c1b2a939f33a952c4159b4ebcb0a`  
		Last Modified: Tue, 10 Jun 2025 23:36:44 GMT  
		Size: 15.8 MB (15765139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d3a1104916c86ec83a5747c8e633c5e6a390c0dbdd5bc0f94c97267b2a5943f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c3d79ae9421feac66d97d4ddc0adb912b6586a0e7a9cbb561a322df85dc96f`

```dockerfile
```

-	Layers:
	-	`sha256:bc88771a7a79518a75ecd38d86620125a77ea3bfd2047014d8c2cc0727a390ba`  
		Last Modified: Wed, 11 Jun 2025 01:19:53 GMT  
		Size: 4.6 MB (4629093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490e6206df775cb69679892caa2c6ede1b5184d9699ab680489de70e0579637c`  
		Last Modified: Wed, 11 Jun 2025 01:19:54 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1135d2b8a5003fc4c194caf24d0876991738191ab92c0e819133c305eaaa44e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63922507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12093ca040c4d920dadb5eca090038728d8dc7cc434935165023accc33cbcdb9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5053ce02008332f5d21c8078e9333bd265abf67e1c9fc7795ef38fef0e7ee2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4521805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29111f0461b7afe2a4c13e858af6b5ad3ad65f1567f77ad94eb85318b15efd8b`

```dockerfile
```

-	Layers:
	-	`sha256:f4081543aee1e1039ba9786fdd6dd357c97ab1fe2649851fbbf8569ee87857f3`  
		Last Modified: Wed, 11 Jun 2025 01:20:00 GMT  
		Size: 4.5 MB (4514945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e6b4a71881cc4768b18353f0d952a4026c71ecfe3d8af27c82f3b7bdf1c89db`  
		Last Modified: Wed, 11 Jun 2025 01:20:01 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:badb1e8c71ac4a0430d0edf9510da28e86b8493834d7edd59181b6143c14a181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67998137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2f0637b612281cd2b99945c5d2f6d4a70542ff4d2106a431ae51f461db5535`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c284d1fb20a7202e4a179c37fe99325b9e47f527f59ca18bcff30295bd115fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4519802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f274ef3e6d0b3fd24f2b4a6d2093b1ad71a14ac3f039cdd845637aa217b47f0`

```dockerfile
```

-	Layers:
	-	`sha256:526e8bd3fa862aa29174553e2dd977c0171ddba81ab2e083128d7794f0be0a12`  
		Last Modified: Wed, 11 Jun 2025 01:20:07 GMT  
		Size: 4.5 MB (4512923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9760dab3c3fd222f5421db90e412905059c82b79acde4f7d858acadbfeec3e26`  
		Last Modified: Wed, 11 Jun 2025 01:20:08 GMT  
		Size: 6.9 KB (6879 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4eb2b7dce67f595c84935c4efc0d19c9e2219f9e98916b18734359c992707872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70958629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a1b2fd3f225b14e162d2febe0afc78240a90a3ca1b203b56780481b392bb49`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e7c1ed34c380b4c9e9f08e94b0f7b9bf90a0e8c42de246cb4b2159e2126fef`  
		Last Modified: Wed, 11 Jun 2025 00:00:47 GMT  
		Size: 16.3 MB (16268617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18e5f62f541623b085b1ac220a18694c1555eac27e8a78c5a99f3033b5f45f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23aa675879b87d355814ac082aef7aa54ecda54f94cc3942bdaf018d76d36f93`

```dockerfile
```

-	Layers:
	-	`sha256:4fba12781b7d1378ef087efc88baf5752a3e7fb7d57ff3f37e275cc5fbf48c16`  
		Last Modified: Wed, 11 Jun 2025 01:20:12 GMT  
		Size: 4.6 MB (4625596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8e32e1d13b9cd655b8f52fd5cee62f6ae2ec79d99a99544c31015763dc0625`  
		Last Modified: Wed, 11 Jun 2025 01:20:13 GMT  
		Size: 6.8 KB (6777 bytes)  
		MIME: application/vnd.in-toto+json
