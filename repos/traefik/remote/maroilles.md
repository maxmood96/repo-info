## `traefik:maroilles`

```console
$ docker pull traefik@sha256:9caeeb4a78e3ed302a01e7d90c690a427f8266d73579935659a18de7b2550317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:9248f7f17d44a02872613d652aff91856f928ebc400d037cd3439731da4cecbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22605595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dd394242b858ec3a77eec6506ea614377091f1904f704d3412983c1be8c0cd`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 07 Oct 2022 04:21:34 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 07 Oct 2022 04:21:35 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Fri, 07 Oct 2022 04:21:35 GMT
EXPOSE 80
# Fri, 07 Oct 2022 04:21:35 GMT
VOLUME [/tmp]
# Fri, 07 Oct 2022 04:21:35 GMT
ENTRYPOINT ["/traefik"]
# Fri, 07 Oct 2022 04:21:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa79c7609bd35acb6baeec95c0534de9f28c053bb3b54b53c4831b70e4a2b6e2`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 320.1 KB (320103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b58027c881a56cde12f5ad6ba79f399d338b083423a96ae8fdb32a53f55af9`  
		Last Modified: Fri, 07 Oct 2022 04:22:44 GMT  
		Size: 22.2 MB (22161952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:84aae39edfd57a3d7eb7d5f3506e471031166e65d061c8be54fca77258b6140c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21066919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b13bdeaf794060f706e8061be10b71e7ef64882356982de89daec674fe698c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Sat, 08 Oct 2022 03:58:30 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Sat, 08 Oct 2022 03:58:31 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Sat, 08 Oct 2022 03:58:32 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Sat, 08 Oct 2022 03:58:33 GMT
EXPOSE 80
# Sat, 08 Oct 2022 03:58:33 GMT
VOLUME [/tmp]
# Sat, 08 Oct 2022 03:58:33 GMT
ENTRYPOINT ["/traefik"]
# Sat, 08 Oct 2022 03:58:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:480f18b6c0179f0ed54861403bbe3503ed26203a6307b30978f4edb95c7a1f03`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 123.5 KB (123539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892e3fa745c422a0bf87c538e124bc46e1c0a2c2fd0c50501c4e558da00084fc`  
		Last Modified: Sat, 08 Oct 2022 04:00:17 GMT  
		Size: 320.1 KB (320098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115198abd673e94528474879115112ca2bd769da4a9f7c9cce6302d59f3d456`  
		Last Modified: Sat, 08 Oct 2022 04:00:21 GMT  
		Size: 20.6 MB (20623282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:fa1d0bc12d9c099cef08d01b3a9eab66778aedf00fbef5b3da0d272333af80d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20574968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63349a030de8627c4abdf307b26a78e32c2a18bc376815ff5cbc07ae39722178`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 07:39:24 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Fri, 07 Oct 2022 07:39:25 GMT
COPY dir:c3f72545af4f290c8fc0a43693ea3334451b85d0dee09c519eb983a71a5a38fa in /usr/share/ 
# Fri, 07 Oct 2022 07:39:26 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Fri, 07 Oct 2022 07:39:26 GMT
EXPOSE 80
# Fri, 07 Oct 2022 07:39:27 GMT
VOLUME [/tmp]
# Fri, 07 Oct 2022 07:39:28 GMT
ENTRYPOINT ["/traefik"]
# Fri, 07 Oct 2022 07:39:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1151fb31968944320508e292407b79b28626a76d0af23bfcb76650fd6129b93f`  
		Last Modified: Fri, 07 Oct 2022 07:40:55 GMT  
		Size: 123.5 KB (123539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019c3a4ad05f22d384ae4ec9a37d144b01923d7a2a5241e8a510dd4d6b6ee5f9`  
		Last Modified: Fri, 07 Oct 2022 07:40:55 GMT  
		Size: 320.1 KB (320082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89d15d062829fe9582b412a41e0c33f0050d927582e9f13666017c4f6992017`  
		Last Modified: Fri, 07 Oct 2022 07:40:58 GMT  
		Size: 20.1 MB (20131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
