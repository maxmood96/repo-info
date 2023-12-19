## `buildpack-deps:buster-curl`

```console
$ docker pull buildpack-deps@sha256:4b78fe8d733201d1532dcc1722db24e29843d4c6ac97b4b1295429fb9cf2e24b
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
$ docker pull buildpack-deps@sha256:b431bcfe09085976ed782734c45004cea4c1ba75cca9998ecc31adc28da2b8aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66745242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a5b77a1e60a1b3b05653902263c2f74789ef79c518b44b64b86b6764c91935`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
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
