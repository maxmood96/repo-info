## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:a4a4fbccf009b0642ff5c9ac695d9ea20120974859a6121890ca838b0cd64a71
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

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2845dfc7b80dc4d9fe46ac603618ea681758376f25a0e2a300c400805b813853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124276191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a98581b176c122f6f849a3658731f86e140aa9a4fffdecd2f2d6282fccd1242`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291bf09cec80aaf3d13eefc3fba3a6cb13a44cdce91da75e0e2c3d8b72348e79`  
		Last Modified: Mon, 08 Dec 2025 23:07:20 GMT  
		Size: 15.8 MB (15764219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17ff9cfdab33e1021de93428c7968b682c4bb6322df919b3c6622b8ac14ec0b`  
		Last Modified: Tue, 09 Dec 2025 00:06:29 GMT  
		Size: 54.8 MB (54755559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:331ee5fd792f5e37288c5d3d85a826354f4892f436806100470ae701eabe578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7919476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f2eb1f73a72e516d2475c882166746a62118452e45252dbf64c5ea00a18373`

```dockerfile
```

-	Layers:
	-	`sha256:fe3303d82ad266b695be25bd12fb5be101bffea8a3767f793e07fdb95e65171d`  
		Last Modified: Tue, 09 Dec 2025 02:21:17 GMT  
		Size: 7.9 MB (7912160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a2a850cf49337de50525d1519d7c8294945260f205c121f96000bc4d7c38e9`  
		Last Modified: Tue, 09 Dec 2025 02:21:17 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8ba4db3a34e3730b620f09a2259c54927d85186c6e2cfdc72dab32e14cb65211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114555958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9767ad908aeef38f69cde06d10f54f91721e2f0c73e7a13654933f777eb4b834`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:33:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b405dcfbbf208b50f83cb073fc2340dc0c1fad234dcbd26845122feadf5cc1f`  
		Last Modified: Mon, 08 Dec 2025 22:17:00 GMT  
		Size: 49.0 MB (49046374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bbf36f43e54145168310c9263866569faa887bc243d2f3bed9e99c1532e0cf`  
		Last Modified: Tue, 09 Dec 2025 00:05:40 GMT  
		Size: 14.9 MB (14879319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e406069dbcf32b42bae4ef9dc2c57f02332b4d3e3cfdd9f3d4277550d22e9`  
		Last Modified: Tue, 09 Dec 2025 01:33:36 GMT  
		Size: 50.6 MB (50630265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1ae8c7ba283da58a8eee50083f7d59e1b6e178e61ebd1a1cde8efa552623d1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7920942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82b71265eff3b7aa6e4e79071bf589d35e5402a4733e61f3eeda2aa099dced`

```dockerfile
```

-	Layers:
	-	`sha256:990ef80a7da18b75fcfd04d0e21c5e065c3e824bcc1128ab96d52c2d0be0a01d`  
		Last Modified: Tue, 09 Dec 2025 02:21:23 GMT  
		Size: 7.9 MB (7913562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1fc71389d810446f85bff15e6f7d71f234a0ec1ebe61848badd28fcf58888c2`  
		Last Modified: Tue, 09 Dec 2025 02:21:24 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6a401bf4b641e22e520a19090d9c1a6030f332e788960946782813a54dd9e965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122872410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3767701de2c13474cb80279397bcb95789ffa2cf049323057e5f13ee53d21a1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:23:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf5c6e26abbf2d346305acdea26f4c77227ae8be9882711816b29b75df95827`  
		Last Modified: Tue, 18 Nov 2025 06:23:37 GMT  
		Size: 15.7 MB (15749561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbea18607285d70f010e2ba402394373534fadffb00b880a34f03b4cba581f`  
		Last Modified: Tue, 18 Nov 2025 07:15:27 GMT  
		Size: 54.9 MB (54865154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0bf9ae62037b2cef297bb2df1a8ff626b25de7c06ddbcf65db81ea529e319333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7925290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7264c8438a593a5e4b3cc3c762e5c544554d55a8d536db62ffaa5dcd03a42d83`

```dockerfile
```

-	Layers:
	-	`sha256:131e7bbd66753faac369474d2905aa6c790ce612a47bb99556f512418bd47df3`  
		Last Modified: Tue, 18 Nov 2025 08:21:03 GMT  
		Size: 7.9 MB (7917894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d4810189770dade5d488b2ec8443840ba17d5798c74320862d6b3f6cdb81a4`  
		Last Modified: Tue, 18 Nov 2025 08:21:04 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:209b3bd1af71e2b13af4c9add5e1018cc78ef278001920f91e030f5b8f5e97d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127016274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ab76e680a6c0215e8ebf532bd89ab23c335f1e0d1e6fa057a79721959a1123`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b1d3bd8e8172de52ae5d3823cd522bc420b102de9f2d204bcdd0b93d98aeda`  
		Last Modified: Mon, 08 Dec 2025 23:14:29 GMT  
		Size: 16.3 MB (16267791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efca8130eda77d172d5308580d8be6986cfcc5e94679f7a976c73a11cc2f674b`  
		Last Modified: Tue, 09 Dec 2025 00:24:12 GMT  
		Size: 56.0 MB (56048951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4b6daca7683aca6240e2b3aeee13c5e9374ca001412f7b2974ebe7174ee2147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7915024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f33fdab539a596c9a0cf3523f86d8c601104d173c2cc4192106d8dde64dbfb`

```dockerfile
```

-	Layers:
	-	`sha256:486a33b1ab96c20f17a1c1d1b96d128b96e13b555c8d2c55f259c86dd81b7562`  
		Last Modified: Tue, 09 Dec 2025 02:21:35 GMT  
		Size: 7.9 MB (7907730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d851d7034f0a0259ef04582152dd01324e90568b0609d1514244f315f3227c2e`  
		Last Modified: Tue, 09 Dec 2025 02:21:36 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
