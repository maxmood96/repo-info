## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:d69e8a1b4da6f156aa3c0a858d0ca11335dc8ca06e0f4e7c2fb0082f934ee6a3
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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:980cb5036fe28323f056442be97e50e5f7f406bfaac6a64f5c528c11487c4d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63700706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36935908306bc83fcc5ed3f8b7597bc6cc391ec67adc1996293cd4d7e3dbc9f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f825d0d4f40316241fe1dc4972626fc738ad42f315280df37eaec16682400cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0de80203df6acea81c3bc88ac27d6a5829e64dd0f2b5540eb16ba40095818c0`

```dockerfile
```

-	Layers:
	-	`sha256:4f5013c38c8227845edc977e621c19c9c996f28a39b5a828567ffae0f493dc4d`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 4.5 MB (4487263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d117a80f010b81ed4a920c2ccdc10549b3f41c798b5ffe5386630d8da0e71eb`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 6.9 KB (6861 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4aba98ebe5257d68962f347c7dee5a140f7d4da7b7cf92c51607f4fd72ac21c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67792790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a758b79e8e12e28acbd659bcac50a98ed535814ca5f93c30269797404db74725`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f1e24a5b752f11cfbc554ac155c83162b583406277abb992cacc42d0812ebfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4492122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecb221b67026f12d42261714fbfee577ab33ee23eae0607486378638df23383`

```dockerfile
```

-	Layers:
	-	`sha256:a1f0a6d35f767bc54a67efd498a65ac8d42c7ddf235c05349b112ee652def0a3`  
		Last Modified: Tue, 25 Feb 2025 05:42:10 GMT  
		Size: 4.5 MB (4485241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9361b69e532888b2d3194c2ff10cdfe7f633b52cda74dcac1ff25fa169669b3b`  
		Last Modified: Tue, 25 Feb 2025 05:42:10 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

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

### `buildpack-deps:oldstable-curl` - unknown; unknown

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
