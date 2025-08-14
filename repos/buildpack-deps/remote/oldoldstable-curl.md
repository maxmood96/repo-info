## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:d017b57919fc9f4f49612ad376da9818ae0597f90bdbf8807d643ebc546db3c2
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
$ docker pull buildpack-deps@sha256:5050d459748889cb8fb1fb4194af955cbc554139ac693b291cbbf62823e3dd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46366f24a468e740f80c3697a6e5e66ff5003fd49fce24e15df974c410a85715`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af1462618b5a82afe7df2de786fb660ccd6e456664a52ddb21b333ab5e72d5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78aaed6c5d97152190ca1b7ec6e2769b4c3332805c2dbf7f28f19fbc8fcd8842`

```dockerfile
```

-	Layers:
	-	`sha256:aad2de9bdf72c8eb1d9ab38a4b46982287515743b736f36ddb97705cf454b899`  
		Last Modified: Wed, 13 Aug 2025 01:20:31 GMT  
		Size: 4.6 MB (4629093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:154363fce24da729cd5ff9890b420566801379d175ddcb770c3cad74abdb22d9`  
		Last Modified: Wed, 13 Aug 2025 01:20:32 GMT  
		Size: 6.8 KB (6801 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3e480e510c0695e7efa5cc7d062daa485a519bd017a4da2b2bcecfddb3b215b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8a6b122901618f0660ea5c22a64062af69b34f5e94c5ee4263b3267b9f7e94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:27a0e70a6a342a82d61d13664b90c890c24d71590db74ef7eb6f4dc1b731387c`  
		Last Modified: Tue, 12 Aug 2025 20:46:51 GMT  
		Size: 49.0 MB (49044404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae3c82b80881167fea789bb8cf043d4de732e7b062431e2c261928679dcd3b3`  
		Last Modified: Wed, 13 Aug 2025 00:15:42 GMT  
		Size: 14.9 MB (14880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a865c82a207090e2733d17abeebd52fd06ee272ed6c6974c04d94479067d729f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8e0cd81b31de959e488d67e066333accbf18a0d984e10af511fff0ea407279`

```dockerfile
```

-	Layers:
	-	`sha256:c8e0cfa61b813f3c2052faa38f1ca9d660db4ea0b633e0b896b64b0ad6e4dbfe`  
		Last Modified: Wed, 13 Aug 2025 01:20:37 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f0e0616d65d787a2b5662f1b0b052b49370231128102253db6c74e378c2320d`  
		Last Modified: Wed, 13 Aug 2025 01:20:38 GMT  
		Size: 6.9 KB (6867 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:59499984c73882fee3c66a0fd6a96cced071fe250706b7d55db012dbc3ec2852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67999085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233f2bbba3451d5de06678395b526185939d16bd979a1cb06400bf578a80eb33`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25635cbca821869ea9220087d35fa6b59e758fb2dca635f36530cb5e44b7c481`  
		Last Modified: Wed, 13 Aug 2025 07:20:06 GMT  
		Size: 15.8 MB (15750676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:28d66af0f2ec6d2665e2f97c5fe4dbc4a9bb09f0297f5eb97eb81331dfb84db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bbbed29980a5fb259b4bf54c2362c7e640b8d28f6d99cac2a41f7c8d4e0785`

```dockerfile
```

-	Layers:
	-	`sha256:b646490771126aa6b7e35a97a7a510b02b92b06b827b43b39639a48955095d2f`  
		Last Modified: Wed, 13 Aug 2025 07:20:05 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17f879a51df89923725e2e4e01b1003836739df5ac2462620215c2b6493b27e1`  
		Last Modified: Wed, 13 Aug 2025 07:20:06 GMT  
		Size: 6.9 KB (6887 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3b8b7637acb2cd8823d486e608692369dc9022165e18e8589896559bd78f053b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70959560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44265a2fec66a6c18290f18e25ef5e2a458440634106ff97e2936ecf32ceaea6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b148e76c29cc0ae2d2cf6449d62900f5cf24990640523768d8221eafa133979a`  
		Last Modified: Tue, 12 Aug 2025 20:44:54 GMT  
		Size: 54.7 MB (54690594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae804adc09e05ab2a1f1dda5903e8e254e92e67f845b9280059ef40044deadb`  
		Last Modified: Tue, 12 Aug 2025 21:20:06 GMT  
		Size: 16.3 MB (16268966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23800e741810d376f1ebea899ae64ef8ac753927e6f6eaa846a7896a1529d7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485455e39b36aad6526fb4665cd744c7991bb63219ebfcfa7612c5c1f5778a28`

```dockerfile
```

-	Layers:
	-	`sha256:760bfa2553a1c100c5806028668d21d2a2ab2c6749377030e48756d6173e93bf`  
		Last Modified: Tue, 12 Aug 2025 22:20:23 GMT  
		Size: 4.6 MB (4625596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1ff0779f641727465b51d18d95c1a6753b26ed6d4a46157ae47b7c98c9bacd4`  
		Last Modified: Tue, 12 Aug 2025 22:20:24 GMT  
		Size: 6.8 KB (6779 bytes)  
		MIME: application/vnd.in-toto+json
