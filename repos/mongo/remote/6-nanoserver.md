## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:5bed6d9e6c2761010c336e22b99c8c5b8254c7d84907ae3b9c91cbabe18da121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:ba12f9af3ef817ecc9587fd4f422920830046453e6bb6a0d819dd7ff8ddbfb80
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.1 MB (638055787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf1d361648a5af2539a1cb02d8b7c2cd64a6e43202b6af7fbaf593a921c6367`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Oct 2023 21:30:39 GMT
RUN Apply image 10.0.20348.2031
# Wed, 11 Oct 2023 02:28:41 GMT
SHELL [cmd /S /C]
# Wed, 11 Oct 2023 03:03:40 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:04:28 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Oct 2023 03:04:29 GMT
USER ContainerUser
# Wed, 11 Oct 2023 03:04:30 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Fri, 13 Oct 2023 00:22:43 GMT
ENV MONGO_VERSION=6.0.11
# Fri, 13 Oct 2023 00:23:17 GMT
COPY dir:f3ee5b35d4b8c33fd7a357b54ffd9e57781c0e7af1f85fa13aee2a982d4f7982 in C:\mongodb 
# Fri, 13 Oct 2023 00:23:36 GMT
RUN mongod --version
# Fri, 13 Oct 2023 00:23:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 13 Oct 2023 00:23:37 GMT
EXPOSE 27017
# Fri, 13 Oct 2023 00:23:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fff54800e03713ba81736f43d985319592fc643a1a32b62dbd5c0ec36549de00`  
		Last Modified: Tue, 10 Oct 2023 17:30:43 GMT  
		Size: 120.6 MB (120604344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cd425f94dc5addd6f49003c495c9acbf2a61ab29ca68946c6cd056ed33c5f6`  
		Last Modified: Wed, 11 Oct 2023 02:48:05 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c5d8a4d1b8dd712544f618c2e6ee6be0146ea27a9e28326d8d91f8bd6fa8a0`  
		Last Modified: Wed, 11 Oct 2023 07:41:29 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2c9710a873f77c9b8cdf8f8359453db5ea2693415cdcd182e0478772b06b5f`  
		Last Modified: Wed, 11 Oct 2023 07:41:28 GMT  
		Size: 87.1 KB (87090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e705c53faad5aaf4367e374cfed21b9e0b718d308280d68adb51337227f65b`  
		Last Modified: Wed, 11 Oct 2023 07:41:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d5b2d3c7888d6f3686a12fd05ea8addf1740213bcf2aea7dfd0a6000b8d5e1`  
		Last Modified: Wed, 11 Oct 2023 07:41:28 GMT  
		Size: 267.2 KB (267168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a58b32d5e2569373f3af9eab9dc44586b675c00fb968859f713ed031f2b3a3`  
		Last Modified: Fri, 13 Oct 2023 00:29:41 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055cbdf6c251369413aad14bad22ebb87cbe855d45fd2c725e12f197cafdb558`  
		Last Modified: Fri, 13 Oct 2023 00:30:47 GMT  
		Size: 517.0 MB (517039214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e73a64ac73c41c6a45a1831867e23c130e30cd078733c4cbe316dc9bda1bf4`  
		Last Modified: Fri, 13 Oct 2023 00:29:39 GMT  
		Size: 49.9 KB (49943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc7bd5199dc730e38d242b367d66d31e41502b594c9de78e396aa0a98994e02`  
		Last Modified: Fri, 13 Oct 2023 00:29:39 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3337bf1e75b3b453b25d73473d7f30fafe48c99862b58a1b4cf8cbbe9f58f8`  
		Last Modified: Fri, 13 Oct 2023 00:29:39 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de0467506f103b3b1d9053f12bc8fe29128c51aa7f536ec52fe8bb1ac30013b`  
		Last Modified: Fri, 13 Oct 2023 00:29:39 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:c5755ba17911d5cc7952dbc5a9c0d5189ec8b412fe87ee07e07e1e6981a58e27
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.9 MB (621926709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f29c2ce92ca5f3093703a4a46002f5b48d298f73a403dfd82ae5f5a4c66d83c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 02:31:25 GMT
SHELL [cmd /S /C]
# Wed, 11 Oct 2023 03:06:25 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:06:58 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Oct 2023 03:06:59 GMT
USER ContainerUser
# Wed, 11 Oct 2023 03:07:00 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Fri, 13 Oct 2023 00:23:45 GMT
ENV MONGO_VERSION=6.0.11
# Fri, 13 Oct 2023 00:24:23 GMT
COPY dir:f3ee5b35d4b8c33fd7a357b54ffd9e57781c0e7af1f85fa13aee2a982d4f7982 in C:\mongodb 
# Fri, 13 Oct 2023 00:24:39 GMT
RUN mongod --version
# Fri, 13 Oct 2023 00:24:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 13 Oct 2023 00:24:40 GMT
EXPOSE 27017
# Fri, 13 Oct 2023 00:24:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1d090bf86f6024502bc8f94ffdf6082818dc40adde892065acecc65617301f`  
		Last Modified: Wed, 11 Oct 2023 02:48:49 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884f2cb9b5edcbbf4b0b83f11a2ca9e93da04c86243865ff1f331445db9abcf3`  
		Last Modified: Wed, 11 Oct 2023 07:43:05 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7c6a1f7c9281c4d2be3cef0ad78603721509d8a2a8f6bc3411192f8112c273`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 69.0 KB (69002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3529e287318b8e986a6ed2518bcd876b733f1577a5c44c2528bbc77778272a`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7282f0ce93e521c5382bb7a008ed67429bd97f092d002c5cbcda26eb63e6708`  
		Last Modified: Wed, 11 Oct 2023 07:43:04 GMT  
		Size: 267.2 KB (267195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c14513d4396e7e18ff9d2bb1e7a59d236cde397e2e630b7e71c0751517f552`  
		Last Modified: Fri, 13 Oct 2023 00:31:02 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d02a36beede45001664de02ec295c893e6784477bd188ef061ecd90b580246`  
		Last Modified: Fri, 13 Oct 2023 00:32:16 GMT  
		Size: 517.0 MB (517039229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44af3224e9e570a6d4a67fad404ec04b979127bb2e8daf18af948fb89866180`  
		Last Modified: Fri, 13 Oct 2023 00:31:00 GMT  
		Size: 78.6 KB (78590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b66bc5f7ff896e82bcab9db0fef1bd0f30f72aab521edab3a50e5981a32a67f`  
		Last Modified: Fri, 13 Oct 2023 00:31:00 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf47cdfe247e156bce651af52ace9589d71b90906a8d1bb5e91a5fe40a0cd73`  
		Last Modified: Fri, 13 Oct 2023 00:31:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6f793d95f52181bdc847d71ce10c31ac040a66efc8555a81e90653487c8ee5`  
		Last Modified: Fri, 13 Oct 2023 00:31:00 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
