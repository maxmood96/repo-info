## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:681cd261ef99ed9a69fcf7b7e168ae17d89f302b838c10f3a4d9dc632ef0fd72
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
$ docker pull buildpack-deps@sha256:96282d6fb162ed8712e260fd2427d41dba6ac748326a49766ab2c11e835fc7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69512039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d4c80d495356959bb14d01a85788de3ed550df3c7ae5b5fa23d9ee3d09a2b5f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d168c1d3cb5d68297853440a2ddee5e5e6cf7f097050df86e8144396a46b756b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f0704cb464079ba88019b6318f0c85cde4d881d570ee92fbed116005a6fe01`

```dockerfile
```

-	Layers:
	-	`sha256:f4c10c9e5dd3bfffe71fc2035f50c71e362f2e097c2e8e820e9da9dbc5b18f54`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 4.5 MB (4487541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc173a9010ae1cd3ae56ed9d6fb10528ce8f8a7dacc0124dbc63ca8ea874b6d7`  
		Last Modified: Tue, 08 Apr 2025 01:24:23 GMT  
		Size: 6.8 KB (6800 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8427dca52a52493e7d3240f98868a95f1d3828496935790a60cf0e6905cf744c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63700573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea8a5fc1bf257a38ce2244b984e467312fd5358071c9ae700d72930311dedc2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:63e394fa58f21bcaaa0292069e46019661e0f7d13c25cfc06c20c942d4e14e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340f7486728be70782401b98c1eb1e4a4ff048f9a51d4ddde7093aac9103937e`

```dockerfile
```

-	Layers:
	-	`sha256:e70dd8d4e233454904ef47a40d16bbfe48e0011c238266c21810e52c21dc1040`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4ee067e62a374391c700d214efa930d07d3a0f2439c126105e2bacba43ff6b`  
		Last Modified: Tue, 18 Mar 2025 07:26:05 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c8ee6187ea3cc91dd6bb40d548257bf6918112c24d15662a38b214191a6cdb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67792398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a95291078f96d17278f56639020d5ee4c92313170ea024c401bea95645076f3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87d689a49f90a22c98506df2f84624057188c4660599f2b4b27596be35d7d827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5052c7ee71e6639be55a112e90e711b2be530149c6bbfb88b6c9173d9eace810`

```dockerfile
```

-	Layers:
	-	`sha256:79a3d18eb2a22628a433203d164d6eed64cb7ffbaabc3f2440682659e2518fd5`  
		Last Modified: Tue, 18 Mar 2025 04:59:59 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d8d30f571eae89327b9754c1c242a72bbfdbca915694557f2c890e270dc6e45`  
		Last Modified: Tue, 18 Mar 2025 04:59:59 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:017e09529f76ffc5e45ebd386ab06a2d54e664652d6314658a5da967bce63ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70951502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c50c127271b9d0de4a1906d220847fb51134ae52a2cf1f39e7c158ffb7fb62`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:137c4e56b93caabf3a57e5f6df5c1646e54646cd765142245eb2151b5c4c36a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4490761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0354999ab03741e1535ed7a9a6263a32c4cc3a71b27f1f7b0c8492bfc11801f6`

```dockerfile
```

-	Layers:
	-	`sha256:378a478606614956bcff0cccf74bbbd9e2e7f9e604d2b53cab40626f7b1caca0`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 4.5 MB (4483982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9e2de973a31a9b82119fbe82f08a1a9049711595b4d8a681c19229c6ed37e7`  
		Last Modified: Tue, 08 Apr 2025 01:24:11 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
