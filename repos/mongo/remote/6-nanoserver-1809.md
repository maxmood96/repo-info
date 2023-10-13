## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:08ee1187fc500fadba2e70b745be1810ad69a1df07a12959ff412fd9e1aea4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.4974; amd64

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
