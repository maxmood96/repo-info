## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:1313f39a372be817a7a418c1082da7a8cb139cccf14d9e95849f51c2a68107f4
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9d86dade34934566e6c18f040ba53c0e11dd999a277a8a0a9e65c01e48eb1a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124051910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29afb157b269f26701a2b9d44f585fb56abb102239135d8a365d1ab0a0cfad28`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8839e2bc871ae3753120cc90b7579e8420af27a9a923ddaf6fffb6f313805ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7715539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ba323cb8e2a91309487a0f9963c334265a8dc6451e81e476c8fa468774ef2c`

```dockerfile
```

-	Layers:
	-	`sha256:61908d48b58147a945338cb667a471444fcabc278cf8b1aa10e9145d0cc76d85`  
		Last Modified: Tue, 25 Feb 2025 03:13:47 GMT  
		Size: 7.7 MB (7708186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a559df725d634c8ac5a06672936b50ff8cf27261380f9c58553729acff18a12`  
		Last Modified: Tue, 25 Feb 2025 03:13:46 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

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
		Last Modified: Tue, 04 Feb 2025 01:37:44 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Tue, 04 Feb 2025 10:42:22 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7c48b43b3adcfcfb794cc307d61fbdfd95ebf9cf80b1a014e90a497356d90`  
		Last Modified: Tue, 04 Feb 2025 16:21:50 GMT  
		Size: 50.6 MB (50640069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

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
		Last Modified: Tue, 04 Feb 2025 16:21:49 GMT  
		Size: 7.7 MB (7709588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d2b811b6219eea73d6c8b83b201bed982a4ee4828fe61b778f3dd01c65abfda`  
		Last Modified: Tue, 04 Feb 2025 16:21:49 GMT  
		Size: 7.4 KB (7412 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

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
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Tue, 04 Feb 2025 09:00:33 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Tue, 04 Feb 2025 19:02:31 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

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
		Last Modified: Tue, 04 Feb 2025 19:02:30 GMT  
		Size: 7.7 MB (7713920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5849e88b3ed6a2a75719ac4430f26df5edd7694533c45962801bd3c3384ac56c`  
		Last Modified: Tue, 04 Feb 2025 19:02:29 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c47f7fcd7509e06d8f28c0d9708bc40d2fc930ce7839373f7484dc8a29431323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126771063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fb3b28d97abe71cd7cc96adc0237d71719f7e07d906d16a70b8a5e50a18ad7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d1be050999cb7935766008eed6d6c4c054de5ae2d30274f03f83b84dbb3b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7711005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6b40348db8bca6028e75ce907a7de8226aa43018a5463f8f00e249901eb485`

```dockerfile
```

-	Layers:
	-	`sha256:8757edb440e90354a28d2e404c16bf60a77f788cb52d4968fe1fd9b7f3a58ddb`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 7.7 MB (7703676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:043ecac4f8f54e0a88050166c3ff290a4acbc411a2a4d023bdc2eb4c369e4884`  
		Last Modified: Tue, 25 Feb 2025 03:13:41 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json
