## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:f9b73c08b68f5992c27a8107070072d5173644bc2eb12edd704c485a1e7828a1
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
$ docker pull buildpack-deps@sha256:4814e93af668ad776156987b0a30c8b308b118e01fbbd17f741b791b8851bad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.0 MB (124049061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581d121fb96975fea39e8d8b79c9c4de4cb6ac154abf3542985c05e89625228`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 08:47:02 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 09:04:02 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ef9e6950a308d27ad0fed70063500c67d5f94b60458bf35e69a461c78d601501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9ec6144be5fdec793e06b9bfe76a1ab2b4f60224d307ec385d56b9d387f4a`

```dockerfile
```

-	Layers:
	-	`sha256:52a22ae317e2876eea325b36b2cc60b6f80c3cb88a7dbdba1853d7465f8d0e0b`  
		Last Modified: Sun, 16 Feb 2025 03:04:46 GMT  
		Size: 7.7 MB (7708186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5117857f7ca0d3e1bf3a461cdcb72b1ca27dbcbcf55684d0fb889d6ed4006b`  
		Last Modified: Sun, 16 Feb 2025 03:04:46 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:50e90a27d27f707ef0ab57cee35d09141b5d5ddc48f5c50f19a658401f1998f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114338681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76476e3bd8b989a1439f7ee7b80544250788737a0ef47e49940fed248ab5972`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 04:34:07 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Wed, 05 Feb 2025 10:42:12 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7c48b43b3adcfcfb794cc307d61fbdfd95ebf9cf80b1a014e90a497356d90`  
		Last Modified: Wed, 05 Feb 2025 08:37:42 GMT  
		Size: 50.6 MB (50640069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:35074129b1e55eaa09100441ecc321d3a2508a3f7d4f66c8f8f041956a5192e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7717000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5628027d82bd65a7e9b5770bfc6efcabf7e11b2d7e8347c1fd52e0f80d6ee7e`

```dockerfile
```

-	Layers:
	-	`sha256:8aba24c42f43c7b1d07553fa5e44303bc244c197a6233a130a34ffefffd1d9f7`  
		Last Modified: Wed, 19 Feb 2025 20:00:25 GMT  
		Size: 7.7 MB (7709588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d2b811b6219eea73d6c8b83b201bed982a4ee4828fe61b778f3dd01c65abfda`  
		Last Modified: Wed, 19 Feb 2025 20:00:25 GMT  
		Size: 7.4 KB (7412 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a1332e1af90cb26070b6baa99e36266cba466bfe681d6ba90be3f4b9ef99c882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f78e099d5e6095c4a70777461659c3ec9130718aff19f00ab43d2de60269c1a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 04:34:59 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Wed, 05 Feb 2025 03:24:45 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Wed, 05 Feb 2025 04:03:49 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee74d373b68a64eaa015105714cab1ff784c74bb896042425bb0d51819ef9564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7721353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532ed2744dc188b91200fab44e877b60851999ed8de46b142f4320588fddc0a8`

```dockerfile
```

-	Layers:
	-	`sha256:83eebe40a479ffd95c81b5e35a25c1397be272d3fd7bd2c1499c2c317f01818c`  
		Last Modified: Wed, 19 Feb 2025 20:00:34 GMT  
		Size: 7.7 MB (7713920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5849e88b3ed6a2a75719ac4430f26df5edd7694533c45962801bd3c3384ac56c`  
		Last Modified: Wed, 19 Feb 2025 20:00:34 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9a62f978f5fdc58bc19fc0153c3642c7986206935c5123229b9400de09265b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126767886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb73a16d07dcda55523ead47dacd4d9749d94ac0ad37187950d43b0fdbab437`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 05:01:41 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 10:05:13 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 22:03:52 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4c21667e744397eb3935c16797e52b0148b9d2656c9c5df160d776ef48f8019e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7711006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bd9c61c42af2df265f3d3c98356591cf58dbc8635d76bca719e8339597bd94`

```dockerfile
```

-	Layers:
	-	`sha256:fcedc0c587cb91d36a7804b4632555da7225541fa346b9a49d88f2ea9ef0ba0d`  
		Last Modified: Sun, 16 Feb 2025 03:04:46 GMT  
		Size: 7.7 MB (7703676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23633969f8f239808620f33b97db5f047216cba12a362fa470b4395f1a8ed0b5`  
		Last Modified: Sun, 16 Feb 2025 03:04:46 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json
