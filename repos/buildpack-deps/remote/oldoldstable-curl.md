## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:c93e16227b899bc7096a9e99f4f8989e933a9aa28c0b412d16c022faf3237672
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
$ docker pull buildpack-deps@sha256:a3c87ab79551a22cd08fee98ad38ae7193a0a50086c2d0af7cbd0e88f639eab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69559710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31253fd5b2a8d7db323cf17fbc54b5cab8120231ae5bc0a58adc4794cc7d3fcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725631376ff1c8c144d62e01c2dd134ff006899cd43c1aff2afbb3141faf91b`  
		Last Modified: Tue, 19 May 2026 23:23:13 GMT  
		Size: 15.8 MB (15790858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50da054d6ba7445fd6fcd8ae243d235fe6cb6024550e9c4d1f91220a13f54a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c971c0119e3d6b7231798ae2ece48a1470530a54413195f181efaf4430035f`

```dockerfile
```

-	Layers:
	-	`sha256:ea7eada9390a066e04faf441f55a70d0bccbf86255c5711db46e10b7a22ba284`  
		Last Modified: Tue, 19 May 2026 23:23:12 GMT  
		Size: 4.6 MB (4637519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e00ad808fbf2aee801f7da761c4f4c720760c2974c6ffbfaf57c6030e94e736`  
		Last Modified: Tue, 19 May 2026 23:23:12 GMT  
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
$ docker pull buildpack-deps@sha256:0c971bac7fd8a7587109ab63c71cfba6a6475f2b840195d1225c343ea22f19d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68031458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec2b50fa2d11a1ff94fe9d42f2a14e491933f78aeb8e7555de7174e4ccba4dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862d1986560a28dd19f86c2aee630b1502d7f508a9266ed7d99d6f03a48419`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 15.8 MB (15774880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fe542c8b0c001d542ada6a081a83e5820105b7c8ea10ef55e92157fc2dc7c6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4643977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e28fa271124d8cd1994251690605cebe04e90c73d0c16d0733914910785760`

```dockerfile
```

-	Layers:
	-	`sha256:0c924a06fb8335973785caef2c6b74ed9c79823ef62286355304bd080a4b7b76`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 4.6 MB (4637133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438b58de38112f3926c6477f0849a6030af8fba2a8ed585f05412eb409ae9bb2`  
		Last Modified: Tue, 19 May 2026 23:26:58 GMT  
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
