## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:bd07daea41e25d5d7d2ad7fc1b16e8a8ac1a51263c35ccc314f1c3f62b168b5c
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
$ docker pull buildpack-deps@sha256:0bc7c8622cd8c56e48874ac60e025120163b8040e967d2f4b49223b586900e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63910162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57adefe8be669da2dd0e065aa10a7ef4e46fe525416a9dccf8caf01455b53e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74a2dc6b13d6a4245ced86bc9245eb06ec8b7886c73620d364aac822de60fee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87b3e511becb82558ce8158ceca3612127ae88e84065cbb0ba3ddea4c76c79b`

```dockerfile
```

-	Layers:
	-	`sha256:2b2158ca015230ceda97b3f0ea5d09f32c66171fcbce3eb8623ab1c8cac4c43b`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 4.5 MB (4489177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d8384c0c4ddea09e556f2f25b5d4410eb4313f61dd5405ff7d5f056ed24dde`  
		Last Modified: Tue, 08 Apr 2025 07:38:25 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c2d3bde12cb01b63210b0267c88042926cd3196127300b61b2402c59ea15998e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68003308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1ef2ff53a579dbfa9e1235ab11f8348d841539ab9350b08ee7eecd67075997`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:34a0e3d2f03c84c8659c79a0ccf799f7efd43965078580da2f079639edc23003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3417529ebeef7d165205c013a7ce026626264d9bf6c18397f76fadc26018cd3b`

```dockerfile
```

-	Layers:
	-	`sha256:4e601ba990d7c970f12770b33aa3d11ef202e01db99a958eeafbc02b731a7eb0`  
		Last Modified: Tue, 08 Apr 2025 06:03:39 GMT  
		Size: 4.5 MB (4487155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4caa97b0e18521b70bde8bf387af2f0fd929d793be3f3f54a11f9c4e66a561e8`  
		Last Modified: Tue, 08 Apr 2025 06:03:39 GMT  
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
