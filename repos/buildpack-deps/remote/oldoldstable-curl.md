## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:0d22167f5623042efc0eeae09bdc00e309f86bbb6ef99115f892547dcde8ed4b
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

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0389b6043df8a79629b67340730c17dc0e5624a1b032d698be02ff9f8193ef52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69562593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bcd43ffb9e3b64784ba4f9b383cca4444a34edb288dfd1a4a6e3a6a1ce457e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f53a3a71a19cca6d8312e9c60a5428b23742024a0057b1f0e46517df6ae4a9`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 15.8 MB (15790824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb163b1d4f2ec53e2cccc63b31981950b54ea2d844c26d4b89d73e795b13a9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7545b04b5b2d04a2e6611acae861cfead4fbaa37f1dfcd859fdc8343c7e51672`

```dockerfile
```

-	Layers:
	-	`sha256:9f11887b2a4e8b7801a10715068f9b2614065e1d39da987653e9a44232836b8f`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 4.6 MB (4637523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724a3b0a1f91fcddcf8df7d26ff604b136192facf6ad8321cec8d5e2a9ce0aca`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1777d2b8b996b5323e0272a30b5c23dd61c4ae448c949262df5c5dd430faa5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63965186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a9caef4852572672cc4de33056335e4438d84b5af0862b3743f698f8e21d48`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:03:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c303da1bd3f277cef3c251ecb02fe6ceb28404700c2776e5e52078361e0d5a63`  
		Last Modified: Tue, 19 May 2026 22:36:43 GMT  
		Size: 49.1 MB (49059808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6159604253fa0b585197db46cb3703cf956f0b1a4d8cb67a661c9f449e5220b`  
		Last Modified: Wed, 20 May 2026 00:03:11 GMT  
		Size: 14.9 MB (14905378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99020c6a090a1b1d3f592a40f5a0c9afbe7ea54ae87d351486421dfa8d469420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22a8667b56f100ac7b37b052bb7edbdffa5cd69f7c00d5ef01f2ed01774431a`

```dockerfile
```

-	Layers:
	-	`sha256:b579ae0d03f6e28528765da58c76b9997adf47cb0cee8959a3f5b0e5a55a1614`  
		Last Modified: Wed, 20 May 2026 00:03:10 GMT  
		Size: 4.6 MB (4639155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244d56ffd34dc447f1ed32f7857eb45a0ac55a0d815aecac4cdc828206f117cb`  
		Last Modified: Wed, 20 May 2026 00:03:10 GMT  
		Size: 6.8 KB (6828 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb5a29660efcef32c61dc4ffe24388b10c91611a3e693d1ccb4292680bb048d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68038947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68ee2c74ce1be7ef53c06523d1c007dce7d520dac93513b4946661e6bd742da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8698eac281c2783fff44c0d5a2c381eeb273791e12f4dc8b407db26260bc3b85`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 15.8 MB (15774833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:248092afc5c7d03d50a422024beaece9d19d6b3a8fc19e082eeae6e04633ed81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274f6ec1e6da73828fa4c7fac67e5c1d09232519a495af6dc74d6c6724567455`

```dockerfile
```

-	Layers:
	-	`sha256:e8bdbbad71d50e0fadcf92425287fd3ddda38b4e7ccb54d99b7ef6bc9973f35c`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 4.6 MB (4637137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aecda9263a2e90b7d19b775c75014785f5001d3597169b5b6d6691f421c37e73`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 6.8 KB (6844 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b280cda449e7a4b363bd384ac96d0a60ae155f19ee3a7fa7bdbe2eee35dab66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71004838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7971d8ec0b6c5c33d4b0ba5479ee3dd60100c58b7929846ccbeb2b72a7de2fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a100a514adffbab3ef3834e4740a809fc60c49ad1b434f56a2d8254524b75`  
		Last Modified: Tue, 19 May 2026 23:25:19 GMT  
		Size: 16.3 MB (16295788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c732e3ab77454747ee2c74c85ea62277a6fa49d58ff3a40e5fde988fe2848452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fba51c33661a2a12e013520b8ed67c2431ba1337fef8707d15bf8a592fad4ed`

```dockerfile
```

-	Layers:
	-	`sha256:8c7d32b1afd28a65575cf528e0e3bb12c4da1ec8967def5264bc7449655e2a84`  
		Last Modified: Tue, 19 May 2026 23:25:18 GMT  
		Size: 4.6 MB (4634022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b03473a8f14f594e277b0d3dd4fcaf1e5dc1493ab26eedbf4b89e0210d708b`  
		Last Modified: Tue, 19 May 2026 23:25:18 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
