## `buildpack-deps:bullseye-curl`

```console
$ docker pull buildpack-deps@sha256:2dde2f77b75833618308cb73f822c775e8bcb8ddb2018b575f2ed1d11f5466ae
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
$ docker pull buildpack-deps@sha256:fc19c2a1bcc8acb1c294e613ddcc478307fe91b3958eff7e69604a28316a3b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39981abdc8bfc48bf45c8c1a803c302ced8acc85b39dd5200d1521ec6cfcfe9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18bd264456db040f06bc3702cd40558a1a177e2dfd52092f186c47d6020618e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed87f64a5158731d391bceca06e56114deae05d53d25e7e8eeb15569fc93aba7`

```dockerfile
```

-	Layers:
	-	`sha256:1123b903a66ae0f18042d3a92d01522de2b2469d9342b7f2ec85ca7e3f61b439`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:484c54d8131c431c8b6421fb7c085e7822973559e562d8b6eccf681eac37002c`  
		Last Modified: Mon, 08 Sep 2025 22:19:57 GMT  
		Size: 6.8 KB (6807 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77c39dcef80f2805d988803c7c3d76fa47d8bd79143a7b3c1033e70b0a71a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94c8cf012cf3a804ee22f87243b200b3449d91a722740bdba7a432a47f1f21`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8274f5d2891e4b4a199e88ea54bf64be2b431cff01268ebaebfacd12519d655d`  
		Last Modified: Mon, 08 Sep 2025 21:14:50 GMT  
		Size: 49.0 MB (49044356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f7d1af869adfa648959578fb79545e78d3ad3763e029dfc7f93e144fcbcf1`  
		Last Modified: Mon, 08 Sep 2025 21:55:59 GMT  
		Size: 14.9 MB (14880715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd19e63e5f27bb754bc71cf6983d4ab526d0eeda369273e9452bf07d86d26089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bab03517e3c9220f05865574d2130422d3895b42ef61c4935e7955b4524f8e5`

```dockerfile
```

-	Layers:
	-	`sha256:ac95d559ff3f76294841a7dcf23cf880de8cc5f9d9894464691ad61f49f51ede`  
		Last Modified: Mon, 08 Sep 2025 22:20:02 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd3da0e00a3867abb305465cb206471fb4d2c757eca6e25e9f6454b454b1db7`  
		Last Modified: Mon, 08 Sep 2025 22:20:03 GMT  
		Size: 6.9 KB (6871 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6d4e6b4c3bcad8b33ad8ac80cdaf7f9726aa4faa776bee2cb5c7dcfd607ac4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67999036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6da8ed77782026f796bb6b236e9edbf81fa460a3dd3a7607af95cd5df1242c2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c26dea2f52a9cb0633591a828e9fd53a32d89290a8c2b4b5d5286f76f5332d`  
		Last Modified: Mon, 08 Sep 2025 22:20:05 GMT  
		Size: 15.8 MB (15750666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1286082e4e6fe392833a4e396fcc5171aa59845c8d602fc338a5db717187be6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e05bcdf621bca18349d544fde61a86399f22875cfa13bf806366bea630645c`

```dockerfile
```

-	Layers:
	-	`sha256:abef9a830eee2cebb5f2b5925b3c7b9eec8a7fbdaac1ee0d8c1b8dc202404e13`  
		Last Modified: Mon, 08 Sep 2025 22:20:08 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c310dea0d3df654eec86cb306c0c1ff9a644e4725397e26e273719db1226dfc`  
		Last Modified: Mon, 08 Sep 2025 22:20:09 GMT  
		Size: 6.9 KB (6887 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a6e4919645a45819b9710fa952e198e5dc474568ebf2f19c9ad87c79796d0c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70959483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f5756c56133240bd133fb377310042531029f7358ca0c63adc4ae9cb27c6f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0956db1fbb0de06709cacad88eee1a92edcd3eb326031290d4f6e321e68d7c6d`  
		Last Modified: Mon, 08 Sep 2025 21:55:16 GMT  
		Size: 16.3 MB (16268970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5bff24929f5c0f106b79824137dd9667d28986bdb29321f94e23090e2ccc5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dc005c03a6b8d8fba80b440158e93f78748cb1d699a7deb77ca675707781a8`

```dockerfile
```

-	Layers:
	-	`sha256:8e8e1de778b1d700ded0b6a16f662045c76d16fcf5ca8399c05cf11d85a07bff`  
		Last Modified: Mon, 08 Sep 2025 22:20:15 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a41b695f44b9b87308b21795ee6af5ef5f4b2eb1354542237cf1157d7f29b74`  
		Last Modified: Mon, 08 Sep 2025 22:20:16 GMT  
		Size: 6.8 KB (6783 bytes)  
		MIME: application/vnd.in-toto+json
