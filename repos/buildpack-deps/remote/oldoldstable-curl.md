## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:84720e7ed8888b54593056379f760c73ffaa4b8ca3693ea4d968f918963d9676
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
$ docker pull buildpack-deps@sha256:5ae04d0e749e1489684f8e8bc1d1db1c09ba2827041cdd9574be9b15a8d9d45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69563814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784b4bd061f33a87d629022368c8315d4bbd18f3897e373d0357a390314e9ee1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:41:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816526a6d4acf81b392ec5a1e6d8d402fbc4bf0460323c5ad45b376b247ca6fc`  
		Last Modified: Wed, 24 Jun 2026 01:41:36 GMT  
		Size: 15.8 MB (15790805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04887befa531150c528f6b3e14ffab5848a29ada28f69bba48b95133ae95b068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4644287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56fe3bd794dd0b73b498657a7c89f6150e2eb96844f906ae5e1139bb7a5e3bc`

```dockerfile
```

-	Layers:
	-	`sha256:83ff6b23198b7c45cd4a46834ef796d0494c796c248818c9bd31bc67de636739`  
		Last Modified: Wed, 24 Jun 2026 01:41:35 GMT  
		Size: 4.6 MB (4637523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d43590724ff68a02e52a2bb81bb4d0b274841534794eef8dc2a8922bde55f4f2`  
		Last Modified: Wed, 24 Jun 2026 01:41:35 GMT  
		Size: 6.8 KB (6764 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2e24d6727e858665f46a19a526780ba2ad3c9eee562cfc1d4df13c91ce99c1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63969400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c4642435a19756c95b11f7cfe24fcb55cce3f87bda60ceb90b5f80f408265`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:057662c04791d47966179d44811cec5af4565f7f7a6a4690c7d8e834d0ba3bd2`  
		Last Modified: Wed, 10 Jun 2026 23:40:48 GMT  
		Size: 49.1 MB (49064004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa240a68c3059c2e50ee1949050052855111d59f6865103a70421028ec0d924`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 14.9 MB (14905396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa9d713b77fcbc8addce53d998acfa0036b9baf8646a04f1224fe8a233c8ab60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4645987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641e6a2aa286d59f3970fd02dfb7f54002e03a076052e0855aaff3e00eed3be6`

```dockerfile
```

-	Layers:
	-	`sha256:9a2ed76fa5d2c9c2085b53a8fe2a714adae6edbc1b4e38a563bcf25e7f14aab0`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 4.6 MB (4639159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c796a4ece53a1fbb8135db709417f2e281ec32aedb67f268617ac76028ad1e3`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
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
$ docker pull buildpack-deps@sha256:eb15c1282a0dbd35932bf6b041beefebb48715a5a94370c6568374f81b443ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71008602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227f3929736cb176212eeba54dcfb629d4c67e79a18bc7e4ce4abd80b36d20eb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 01:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:508ffc251196056212d40e318af0b7425af79fd3069a3f9ab15fd6220917ec75`  
		Last Modified: Wed, 24 Jun 2026 00:28:09 GMT  
		Size: 54.7 MB (54712884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f059b391cd2cd82464a697d38282bb9c5437ac5b83e7b92cde4d9a0644a137f5`  
		Last Modified: Wed, 24 Jun 2026 01:44:13 GMT  
		Size: 16.3 MB (16295718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea2327506faf2adb61a58e378c579e8bc39949993bd565a49619c4cd883429e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4640768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c829bb0976070e0ded0dfa5da89b335264aee3fed1fc2a10b1f4695bbf601`

```dockerfile
```

-	Layers:
	-	`sha256:3ae6a734c598fafba2a7ea7fb67318093d67977ad20dff871d284c7a349bd6da`  
		Last Modified: Wed, 24 Jun 2026 01:44:12 GMT  
		Size: 4.6 MB (4634026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d17908bd53053b88a6866737e9fdadc616ac01109ab8c640546190ce0f27213e`  
		Last Modified: Wed, 24 Jun 2026 01:44:12 GMT  
		Size: 6.7 KB (6742 bytes)  
		MIME: application/vnd.in-toto+json
