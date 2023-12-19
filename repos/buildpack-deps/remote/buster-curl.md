## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:04f3ad7af72f01a9f053c3d84824f30063c075277472d37011b012e28f95a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:64876dded9825a6cf7b8a31e2c33d7900a3733d9a0c1767b715543b5ea62d8de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68084286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e658e7fb09464559edfc915b40eaf72ba8aed754782b07343595478086c90b23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:00 GMT
ADD file:e5e3f2fedf4fa6382f3bbf6203060ba68df1aadc7ebfa3350df20bf31b102f0e in / 
# Tue, 19 Dec 2023 01:21:01 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:30b73a2ffaab3c39355a8bcc5eae8ba1465bd7d9467f197b91f7635816b16bc9`  
		Last Modified: Tue, 19 Dec 2023 01:25:58 GMT  
		Size: 50.5 MB (50500409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38726aed64a0804777af4106983e9686ea639add75dae8538ecaad0c0e6a58`  
		Last Modified: Tue, 19 Dec 2023 04:43:15 GMT  
		Size: 17.6 MB (17583877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:28bce109ec1920feefa8c8624ec75b21f9d08038a920ee5d0f164c60f492d440
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31cd1943d0d3a37b481cf2e66990aad5a341e4659275c3d0c0af77f2116c858f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 02:08:17 GMT
ADD file:1d1e5697e5dba574e9d2a2d1e89b8c760c4f3e51a2ba9869f8a00e198b92d00e in / 
# Tue, 19 Dec 2023 02:08:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e0103098dcfb4ed7f616fb2a6d97e98aeecd754d0057e833086dc5bc532b8b89`  
		Last Modified: Tue, 19 Dec 2023 02:12:52 GMT  
		Size: 46.0 MB (45967631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619ba75f890a03acdcec6c22d1592be3055d06472e856d24cad8542114ec19f3`  
		Last Modified: Tue, 19 Dec 2023 08:08:28 GMT  
		Size: 16.2 MB (16216356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:46a92fc11214a3d9c3d70b7dcd8abfca65d771e0dcc70504ba498b382c4d06c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66744311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c362f11787fe8b4a783c57604c5ea5601866a5400deee55372367ab2e6d0889e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:31 GMT
ADD file:df5e5dd39efc6ae3cc9132f6ca6bb569731f7a37cf4b41f87bcb7aa1ba9771e8 in / 
# Tue, 19 Dec 2023 01:41:32 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:36:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93507f9712ced9fbfd0d0f689cf7b55fb245cef88530c07ac5dc5cad20fa889d`  
		Last Modified: Tue, 19 Dec 2023 01:45:40 GMT  
		Size: 49.3 MB (49289026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d548003bf6042e58cd00488bd9dec02acb1fd956797b04f2aacc5f11f2e1a6eb`  
		Last Modified: Tue, 19 Dec 2023 11:44:06 GMT  
		Size: 17.5 MB (17455285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:72446ef67a7efe80796d54f800f82d918f5167ad4b8a0ea1beed984c5611e045
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69354848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54846806879701cd710b18d0336f7e6bdb603682a7457520002605f150cf5a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:40 GMT
ADD file:4c009b0d408e3df297246382d87b0be68c34886e13ed79ba47feb8ff51acb863 in / 
# Tue, 19 Dec 2023 01:39:41 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d351f5ab6958b8ca5f2b8e463c49cba65be4285ead8bdbc1378b5ce2c8cd736`  
		Last Modified: Tue, 19 Dec 2023 01:44:53 GMT  
		Size: 51.3 MB (51255444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92ef590e153dccaba28c33feb3c21c9c8fd8e2f421a31659859531d5368bad9`  
		Last Modified: Tue, 19 Dec 2023 03:38:54 GMT  
		Size: 18.1 MB (18099404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
