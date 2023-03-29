<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.25`](#nats-streaming025)
-	[`nats-streaming:0.25-alpine`](#nats-streaming025-alpine)
-	[`nats-streaming:0.25-alpine3.17`](#nats-streaming025-alpine317)
-	[`nats-streaming:0.25-linux`](#nats-streaming025-linux)
-	[`nats-streaming:0.25-nanoserver`](#nats-streaming025-nanoserver)
-	[`nats-streaming:0.25-nanoserver-1809`](#nats-streaming025-nanoserver-1809)
-	[`nats-streaming:0.25-scratch`](#nats-streaming025-scratch)
-	[`nats-streaming:0.25-windowsservercore`](#nats-streaming025-windowsservercore)
-	[`nats-streaming:0.25-windowsservercore-1809`](#nats-streaming025-windowsservercore-1809)
-	[`nats-streaming:0.25.3`](#nats-streaming0253)
-	[`nats-streaming:0.25.3-alpine`](#nats-streaming0253-alpine)
-	[`nats-streaming:0.25.3-alpine3.17`](#nats-streaming0253-alpine317)
-	[`nats-streaming:0.25.3-linux`](#nats-streaming0253-linux)
-	[`nats-streaming:0.25.3-nanoserver`](#nats-streaming0253-nanoserver)
-	[`nats-streaming:0.25.3-nanoserver-1809`](#nats-streaming0253-nanoserver-1809)
-	[`nats-streaming:0.25.3-scratch`](#nats-streaming0253-scratch)
-	[`nats-streaming:0.25.3-windowsservercore`](#nats-streaming0253-windowsservercore)
-	[`nats-streaming:0.25.3-windowsservercore-1809`](#nats-streaming0253-windowsservercore-1809)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.17`](#nats-streamingalpine317)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)

## `nats-streaming:0.25`

```console
$ docker pull nats-streaming@sha256:07031192d0940a2f9299bd3606738ef381e139dc840a0ee68a7e2542cdd053d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:54929ad2dec3eecece17506d726c8b92eebb1aa02882e93575ed0074e84b50bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33ab0f0d21265a786135545d46035f7a4c315ea0ca84d652295bec764c2d88a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccfcbad20611d1aa935b9ad0352190a45aa38d8a89a3c87895ea8b42502ec0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:34:42 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 22:34:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 22:34:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 22:34:45 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 22:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:34:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d37fb7cb119872af61de93adacff08235e50a90ffea52f6daa9f9e318a45b`  
		Last Modified: Wed, 29 Mar 2023 22:35:02 GMT  
		Size: 8.0 MB (7951572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051177506124f7e3e7e3ee69487686f7ef4b0e98ce0756b40cdff883f8ad221`  
		Last Modified: Wed, 29 Mar 2023 22:35:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2b872c9f38fbaa8ccd86aae99ff49be7ca0081947ff402419b4908daf58019e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10725973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf282fbb53d74f70eb62b53a208af332a235cc98c5c913b9c2ce328695079c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:27:45 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:27:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:27:48 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:27:48 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:27:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99adc85b7a7f0c407e58670682e492d2ed4d84e3ab1bb7027956969d00ebfc71`  
		Last Modified: Wed, 29 Mar 2023 19:28:01 GMT  
		Size: 7.6 MB (7614751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4909158433ab6374c50735598fc1b8ced59a9783484d5d81b17f79e340f51`  
		Last Modified: Wed, 29 Mar 2023 19:28:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:3dd42a0204775da869e619716598df034fdc2dc745fe54733e05283be46959a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10475540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc61fa844612cd4e06d2f86ec59df937bb440d8bf4d9136d8e6f31c9e6af6b60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:29 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:25:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:25:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:25:32 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:25:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff327778aa8c8454a9938f941121fa97bd7b586285cb6a129c21cd04d644d6`  
		Last Modified: Wed, 29 Mar 2023 19:26:04 GMT  
		Size: 7.6 MB (7606603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c1e330b4e950e4a13732095c4ed8bc3229d2036ab640e7211a90fc501e80a`  
		Last Modified: Wed, 29 Mar 2023 19:26:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0991c0c32b4fbb8d20465613b726c4622735accfc4233ff74da6c519d7322d1f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10569273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd3e7b4045f60d83279ac66e4598fc69748776e5eef9c5e6399193136d3f784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:09:27 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Fri, 10 Feb 2023 23:09:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 10 Feb 2023 23:09:30 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 10 Feb 2023 23:09:30 GMT
EXPOSE 4222 8222
# Fri, 10 Feb 2023 23:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 23:09:30 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0ea37a8f15a246683d21e808dad12d5fbd0f43c8d9b4c729b1a726d23dde9`  
		Last Modified: Fri, 10 Feb 2023 23:09:54 GMT  
		Size: 7.3 MB (7306894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1992f5b04c200b5fa7c595d620a4413f4705afbbf1e1273205e2648cfc95fa`  
		Last Modified: Fri, 10 Feb 2023 23:09:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.17`

```console
$ docker pull nats-streaming@sha256:54929ad2dec3eecece17506d726c8b92eebb1aa02882e93575ed0074e84b50bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.17` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33ab0f0d21265a786135545d46035f7a4c315ea0ca84d652295bec764c2d88a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccfcbad20611d1aa935b9ad0352190a45aa38d8a89a3c87895ea8b42502ec0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:34:42 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 22:34:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 22:34:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 22:34:45 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 22:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:34:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d37fb7cb119872af61de93adacff08235e50a90ffea52f6daa9f9e318a45b`  
		Last Modified: Wed, 29 Mar 2023 22:35:02 GMT  
		Size: 8.0 MB (7951572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051177506124f7e3e7e3ee69487686f7ef4b0e98ce0756b40cdff883f8ad221`  
		Last Modified: Wed, 29 Mar 2023 22:35:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2b872c9f38fbaa8ccd86aae99ff49be7ca0081947ff402419b4908daf58019e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10725973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf282fbb53d74f70eb62b53a208af332a235cc98c5c913b9c2ce328695079c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:27:45 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:27:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:27:48 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:27:48 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:27:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99adc85b7a7f0c407e58670682e492d2ed4d84e3ab1bb7027956969d00ebfc71`  
		Last Modified: Wed, 29 Mar 2023 19:28:01 GMT  
		Size: 7.6 MB (7614751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4909158433ab6374c50735598fc1b8ced59a9783484d5d81b17f79e340f51`  
		Last Modified: Wed, 29 Mar 2023 19:28:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:3dd42a0204775da869e619716598df034fdc2dc745fe54733e05283be46959a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10475540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc61fa844612cd4e06d2f86ec59df937bb440d8bf4d9136d8e6f31c9e6af6b60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:29 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:25:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:25:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:25:32 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:25:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff327778aa8c8454a9938f941121fa97bd7b586285cb6a129c21cd04d644d6`  
		Last Modified: Wed, 29 Mar 2023 19:26:04 GMT  
		Size: 7.6 MB (7606603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c1e330b4e950e4a13732095c4ed8bc3229d2036ab640e7211a90fc501e80a`  
		Last Modified: Wed, 29 Mar 2023 19:26:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0991c0c32b4fbb8d20465613b726c4622735accfc4233ff74da6c519d7322d1f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10569273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd3e7b4045f60d83279ac66e4598fc69748776e5eef9c5e6399193136d3f784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:09:27 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Fri, 10 Feb 2023 23:09:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 10 Feb 2023 23:09:30 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 10 Feb 2023 23:09:30 GMT
EXPOSE 4222 8222
# Fri, 10 Feb 2023 23:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 23:09:30 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0ea37a8f15a246683d21e808dad12d5fbd0f43c8d9b4c729b1a726d23dde9`  
		Last Modified: Fri, 10 Feb 2023 23:09:54 GMT  
		Size: 7.3 MB (7306894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1992f5b04c200b5fa7c595d620a4413f4705afbbf1e1273205e2648cfc95fa`  
		Last Modified: Fri, 10 Feb 2023 23:09:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-linux`

```console
$ docker pull nats-streaming@sha256:73f07f50ce952ce448048e75d494ee6ed95eae0ad7275b712e8214552113960a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver`

```console
$ docker pull nats-streaming@sha256:d6049fac048e55a8e4f6c8ed4cb716d06bc558feea57b76f5081d24322f38b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d6049fac048e55a8e4f6c8ed4cb716d06bc558feea57b76f5081d24322f38b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:73f07f50ce952ce448048e75d494ee6ed95eae0ad7275b712e8214552113960a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore`

```console
$ docker pull nats-streaming@sha256:67ecc474de4458dfff78cbddeea1c0505eec8c353d83d6d0346ef5e6332366a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:8d4771f8e1a5a0de3646def6dd9b6d7d2493e56de5984e668fd86153ebe56736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022130897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58b989bd8c98566448b87d746a8d9121e16906eb07b293bcb8d89c06ff848f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 04:05:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:05:13 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Mar 2023 04:05:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Mar 2023 04:05:15 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Mar 2023 04:06:40 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Mar 2023 04:08:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Mar 2023 04:08:56 GMT
EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:08:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:08:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c46bc18b88e816c6caaf34206ccb18a5b7f6665a73ae9a4678525d49fcb1f2`  
		Last Modified: Thu, 16 Mar 2023 09:07:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2879bcc35018c5e8a267f8042c62dd0c05fe41b234e85d986fee9c819cf65c18`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90235cb5c6d3898b39e2f35eb44a986ded127a99bbc8ec28e3f8cfcc4d29ed4`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01ba9a614aa82b0f534bfeb5dac8b1319b3d65cb6cf165e646a50c34d2961d0`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fc30400d336dfe957c7e151e9e7597f85f02daea9f164b26daa5eb6404952`  
		Last Modified: Thu, 16 Mar 2023 09:08:58 GMT  
		Size: 460.5 KB (460503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae978079933163805999ecc5807a9fce77bd9d6d4fb4bf408031613caba29f`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 8.2 MB (8150067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a68f46d1ea3ac895fe1af1b7a28b090b4ab3a03309a6f26ab5a6ae3bfe6c88`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901346ca0aa9486c1efe86f106c0a7bc67599332aed0a8d530d7092b136b2914`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6f2b6008f08f579439aa82acbdfe4319a182e42be05f9f6cf768a62ffba65`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:67ecc474de4458dfff78cbddeea1c0505eec8c353d83d6d0346ef5e6332366a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:8d4771f8e1a5a0de3646def6dd9b6d7d2493e56de5984e668fd86153ebe56736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022130897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58b989bd8c98566448b87d746a8d9121e16906eb07b293bcb8d89c06ff848f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 04:05:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:05:13 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Mar 2023 04:05:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Mar 2023 04:05:15 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Mar 2023 04:06:40 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Mar 2023 04:08:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Mar 2023 04:08:56 GMT
EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:08:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:08:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c46bc18b88e816c6caaf34206ccb18a5b7f6665a73ae9a4678525d49fcb1f2`  
		Last Modified: Thu, 16 Mar 2023 09:07:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2879bcc35018c5e8a267f8042c62dd0c05fe41b234e85d986fee9c819cf65c18`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90235cb5c6d3898b39e2f35eb44a986ded127a99bbc8ec28e3f8cfcc4d29ed4`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01ba9a614aa82b0f534bfeb5dac8b1319b3d65cb6cf165e646a50c34d2961d0`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fc30400d336dfe957c7e151e9e7597f85f02daea9f164b26daa5eb6404952`  
		Last Modified: Thu, 16 Mar 2023 09:08:58 GMT  
		Size: 460.5 KB (460503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae978079933163805999ecc5807a9fce77bd9d6d4fb4bf408031613caba29f`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 8.2 MB (8150067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a68f46d1ea3ac895fe1af1b7a28b090b4ab3a03309a6f26ab5a6ae3bfe6c88`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901346ca0aa9486c1efe86f106c0a7bc67599332aed0a8d530d7092b136b2914`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6f2b6008f08f579439aa82acbdfe4319a182e42be05f9f6cf768a62ffba65`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3`

```console
$ docker pull nats-streaming@sha256:07031192d0940a2f9299bd3606738ef381e139dc840a0ee68a7e2542cdd053d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25.3` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-alpine`

```console
$ docker pull nats-streaming@sha256:54929ad2dec3eecece17506d726c8b92eebb1aa02882e93575ed0074e84b50bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.3-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33ab0f0d21265a786135545d46035f7a4c315ea0ca84d652295bec764c2d88a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccfcbad20611d1aa935b9ad0352190a45aa38d8a89a3c87895ea8b42502ec0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:34:42 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 22:34:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 22:34:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 22:34:45 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 22:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:34:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d37fb7cb119872af61de93adacff08235e50a90ffea52f6daa9f9e318a45b`  
		Last Modified: Wed, 29 Mar 2023 22:35:02 GMT  
		Size: 8.0 MB (7951572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051177506124f7e3e7e3ee69487686f7ef4b0e98ce0756b40cdff883f8ad221`  
		Last Modified: Wed, 29 Mar 2023 22:35:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2b872c9f38fbaa8ccd86aae99ff49be7ca0081947ff402419b4908daf58019e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10725973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf282fbb53d74f70eb62b53a208af332a235cc98c5c913b9c2ce328695079c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:27:45 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:27:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:27:48 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:27:48 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:27:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99adc85b7a7f0c407e58670682e492d2ed4d84e3ab1bb7027956969d00ebfc71`  
		Last Modified: Wed, 29 Mar 2023 19:28:01 GMT  
		Size: 7.6 MB (7614751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4909158433ab6374c50735598fc1b8ced59a9783484d5d81b17f79e340f51`  
		Last Modified: Wed, 29 Mar 2023 19:28:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:3dd42a0204775da869e619716598df034fdc2dc745fe54733e05283be46959a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10475540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc61fa844612cd4e06d2f86ec59df937bb440d8bf4d9136d8e6f31c9e6af6b60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:29 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:25:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:25:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:25:32 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:25:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff327778aa8c8454a9938f941121fa97bd7b586285cb6a129c21cd04d644d6`  
		Last Modified: Wed, 29 Mar 2023 19:26:04 GMT  
		Size: 7.6 MB (7606603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c1e330b4e950e4a13732095c4ed8bc3229d2036ab640e7211a90fc501e80a`  
		Last Modified: Wed, 29 Mar 2023 19:26:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0991c0c32b4fbb8d20465613b726c4622735accfc4233ff74da6c519d7322d1f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10569273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd3e7b4045f60d83279ac66e4598fc69748776e5eef9c5e6399193136d3f784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:09:27 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Fri, 10 Feb 2023 23:09:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 10 Feb 2023 23:09:30 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 10 Feb 2023 23:09:30 GMT
EXPOSE 4222 8222
# Fri, 10 Feb 2023 23:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 23:09:30 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0ea37a8f15a246683d21e808dad12d5fbd0f43c8d9b4c729b1a726d23dde9`  
		Last Modified: Fri, 10 Feb 2023 23:09:54 GMT  
		Size: 7.3 MB (7306894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1992f5b04c200b5fa7c595d620a4413f4705afbbf1e1273205e2648cfc95fa`  
		Last Modified: Fri, 10 Feb 2023 23:09:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-alpine3.17`

```console
$ docker pull nats-streaming@sha256:54929ad2dec3eecece17506d726c8b92eebb1aa02882e93575ed0074e84b50bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.3-alpine3.17` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33ab0f0d21265a786135545d46035f7a4c315ea0ca84d652295bec764c2d88a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccfcbad20611d1aa935b9ad0352190a45aa38d8a89a3c87895ea8b42502ec0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:34:42 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 22:34:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 22:34:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 22:34:45 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 22:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:34:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d37fb7cb119872af61de93adacff08235e50a90ffea52f6daa9f9e318a45b`  
		Last Modified: Wed, 29 Mar 2023 22:35:02 GMT  
		Size: 8.0 MB (7951572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051177506124f7e3e7e3ee69487686f7ef4b0e98ce0756b40cdff883f8ad221`  
		Last Modified: Wed, 29 Mar 2023 22:35:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2b872c9f38fbaa8ccd86aae99ff49be7ca0081947ff402419b4908daf58019e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10725973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf282fbb53d74f70eb62b53a208af332a235cc98c5c913b9c2ce328695079c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:27:45 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:27:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:27:48 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:27:48 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:27:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99adc85b7a7f0c407e58670682e492d2ed4d84e3ab1bb7027956969d00ebfc71`  
		Last Modified: Wed, 29 Mar 2023 19:28:01 GMT  
		Size: 7.6 MB (7614751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4909158433ab6374c50735598fc1b8ced59a9783484d5d81b17f79e340f51`  
		Last Modified: Wed, 29 Mar 2023 19:28:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:3dd42a0204775da869e619716598df034fdc2dc745fe54733e05283be46959a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10475540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc61fa844612cd4e06d2f86ec59df937bb440d8bf4d9136d8e6f31c9e6af6b60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:29 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:25:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:25:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:25:32 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:25:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff327778aa8c8454a9938f941121fa97bd7b586285cb6a129c21cd04d644d6`  
		Last Modified: Wed, 29 Mar 2023 19:26:04 GMT  
		Size: 7.6 MB (7606603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c1e330b4e950e4a13732095c4ed8bc3229d2036ab640e7211a90fc501e80a`  
		Last Modified: Wed, 29 Mar 2023 19:26:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0991c0c32b4fbb8d20465613b726c4622735accfc4233ff74da6c519d7322d1f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10569273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd3e7b4045f60d83279ac66e4598fc69748776e5eef9c5e6399193136d3f784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:09:27 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Fri, 10 Feb 2023 23:09:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 10 Feb 2023 23:09:30 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 10 Feb 2023 23:09:30 GMT
EXPOSE 4222 8222
# Fri, 10 Feb 2023 23:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 23:09:30 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0ea37a8f15a246683d21e808dad12d5fbd0f43c8d9b4c729b1a726d23dde9`  
		Last Modified: Fri, 10 Feb 2023 23:09:54 GMT  
		Size: 7.3 MB (7306894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1992f5b04c200b5fa7c595d620a4413f4705afbbf1e1273205e2648cfc95fa`  
		Last Modified: Fri, 10 Feb 2023 23:09:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-linux`

```console
$ docker pull nats-streaming@sha256:73f07f50ce952ce448048e75d494ee6ed95eae0ad7275b712e8214552113960a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.3-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-nanoserver`

```console
$ docker pull nats-streaming@sha256:d6049fac048e55a8e4f6c8ed4cb716d06bc558feea57b76f5081d24322f38b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25.3-nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d6049fac048e55a8e4f6c8ed4cb716d06bc558feea57b76f5081d24322f38b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25.3-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-scratch`

```console
$ docker pull nats-streaming@sha256:73f07f50ce952ce448048e75d494ee6ed95eae0ad7275b712e8214552113960a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.3-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.3-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-windowsservercore`

```console
$ docker pull nats-streaming@sha256:67ecc474de4458dfff78cbddeea1c0505eec8c353d83d6d0346ef5e6332366a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25.3-windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:8d4771f8e1a5a0de3646def6dd9b6d7d2493e56de5984e668fd86153ebe56736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022130897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58b989bd8c98566448b87d746a8d9121e16906eb07b293bcb8d89c06ff848f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 04:05:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:05:13 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Mar 2023 04:05:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Mar 2023 04:05:15 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Mar 2023 04:06:40 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Mar 2023 04:08:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Mar 2023 04:08:56 GMT
EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:08:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:08:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c46bc18b88e816c6caaf34206ccb18a5b7f6665a73ae9a4678525d49fcb1f2`  
		Last Modified: Thu, 16 Mar 2023 09:07:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2879bcc35018c5e8a267f8042c62dd0c05fe41b234e85d986fee9c819cf65c18`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90235cb5c6d3898b39e2f35eb44a986ded127a99bbc8ec28e3f8cfcc4d29ed4`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01ba9a614aa82b0f534bfeb5dac8b1319b3d65cb6cf165e646a50c34d2961d0`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fc30400d336dfe957c7e151e9e7597f85f02daea9f164b26daa5eb6404952`  
		Last Modified: Thu, 16 Mar 2023 09:08:58 GMT  
		Size: 460.5 KB (460503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae978079933163805999ecc5807a9fce77bd9d6d4fb4bf408031613caba29f`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 8.2 MB (8150067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a68f46d1ea3ac895fe1af1b7a28b090b4ab3a03309a6f26ab5a6ae3bfe6c88`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901346ca0aa9486c1efe86f106c0a7bc67599332aed0a8d530d7092b136b2914`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6f2b6008f08f579439aa82acbdfe4319a182e42be05f9f6cf768a62ffba65`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.3-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:67ecc474de4458dfff78cbddeea1c0505eec8c353d83d6d0346ef5e6332366a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:0.25.3-windowsservercore-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:8d4771f8e1a5a0de3646def6dd9b6d7d2493e56de5984e668fd86153ebe56736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022130897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58b989bd8c98566448b87d746a8d9121e16906eb07b293bcb8d89c06ff848f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 04:05:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:05:13 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Mar 2023 04:05:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Mar 2023 04:05:15 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Mar 2023 04:06:40 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Mar 2023 04:08:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Mar 2023 04:08:56 GMT
EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:08:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:08:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c46bc18b88e816c6caaf34206ccb18a5b7f6665a73ae9a4678525d49fcb1f2`  
		Last Modified: Thu, 16 Mar 2023 09:07:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2879bcc35018c5e8a267f8042c62dd0c05fe41b234e85d986fee9c819cf65c18`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90235cb5c6d3898b39e2f35eb44a986ded127a99bbc8ec28e3f8cfcc4d29ed4`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01ba9a614aa82b0f534bfeb5dac8b1319b3d65cb6cf165e646a50c34d2961d0`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fc30400d336dfe957c7e151e9e7597f85f02daea9f164b26daa5eb6404952`  
		Last Modified: Thu, 16 Mar 2023 09:08:58 GMT  
		Size: 460.5 KB (460503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae978079933163805999ecc5807a9fce77bd9d6d4fb4bf408031613caba29f`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 8.2 MB (8150067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a68f46d1ea3ac895fe1af1b7a28b090b4ab3a03309a6f26ab5a6ae3bfe6c88`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901346ca0aa9486c1efe86f106c0a7bc67599332aed0a8d530d7092b136b2914`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6f2b6008f08f579439aa82acbdfe4319a182e42be05f9f6cf768a62ffba65`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:54929ad2dec3eecece17506d726c8b92eebb1aa02882e93575ed0074e84b50bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33ab0f0d21265a786135545d46035f7a4c315ea0ca84d652295bec764c2d88a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccfcbad20611d1aa935b9ad0352190a45aa38d8a89a3c87895ea8b42502ec0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:34:42 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 22:34:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 22:34:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 22:34:45 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 22:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:34:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d37fb7cb119872af61de93adacff08235e50a90ffea52f6daa9f9e318a45b`  
		Last Modified: Wed, 29 Mar 2023 22:35:02 GMT  
		Size: 8.0 MB (7951572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051177506124f7e3e7e3ee69487686f7ef4b0e98ce0756b40cdff883f8ad221`  
		Last Modified: Wed, 29 Mar 2023 22:35:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2b872c9f38fbaa8ccd86aae99ff49be7ca0081947ff402419b4908daf58019e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10725973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf282fbb53d74f70eb62b53a208af332a235cc98c5c913b9c2ce328695079c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:27:45 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:27:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:27:48 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:27:48 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:27:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99adc85b7a7f0c407e58670682e492d2ed4d84e3ab1bb7027956969d00ebfc71`  
		Last Modified: Wed, 29 Mar 2023 19:28:01 GMT  
		Size: 7.6 MB (7614751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4909158433ab6374c50735598fc1b8ced59a9783484d5d81b17f79e340f51`  
		Last Modified: Wed, 29 Mar 2023 19:28:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:3dd42a0204775da869e619716598df034fdc2dc745fe54733e05283be46959a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10475540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc61fa844612cd4e06d2f86ec59df937bb440d8bf4d9136d8e6f31c9e6af6b60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:29 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:25:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:25:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:25:32 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:25:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff327778aa8c8454a9938f941121fa97bd7b586285cb6a129c21cd04d644d6`  
		Last Modified: Wed, 29 Mar 2023 19:26:04 GMT  
		Size: 7.6 MB (7606603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c1e330b4e950e4a13732095c4ed8bc3229d2036ab640e7211a90fc501e80a`  
		Last Modified: Wed, 29 Mar 2023 19:26:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0991c0c32b4fbb8d20465613b726c4622735accfc4233ff74da6c519d7322d1f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10569273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd3e7b4045f60d83279ac66e4598fc69748776e5eef9c5e6399193136d3f784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:09:27 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Fri, 10 Feb 2023 23:09:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 10 Feb 2023 23:09:30 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 10 Feb 2023 23:09:30 GMT
EXPOSE 4222 8222
# Fri, 10 Feb 2023 23:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 23:09:30 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0ea37a8f15a246683d21e808dad12d5fbd0f43c8d9b4c729b1a726d23dde9`  
		Last Modified: Fri, 10 Feb 2023 23:09:54 GMT  
		Size: 7.3 MB (7306894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1992f5b04c200b5fa7c595d620a4413f4705afbbf1e1273205e2648cfc95fa`  
		Last Modified: Fri, 10 Feb 2023 23:09:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.17`

```console
$ docker pull nats-streaming@sha256:54929ad2dec3eecece17506d726c8b92eebb1aa02882e93575ed0074e84b50bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.17` - linux; amd64

```console
$ docker pull nats-streaming@sha256:33ab0f0d21265a786135545d46035f7a4c315ea0ca84d652295bec764c2d88a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11326555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ccfcbad20611d1aa935b9ad0352190a45aa38d8a89a3c87895ea8b42502ec0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:34:42 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 22:34:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 22:34:45 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 22:34:45 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 22:34:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 22:34:45 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d37fb7cb119872af61de93adacff08235e50a90ffea52f6daa9f9e318a45b`  
		Last Modified: Wed, 29 Mar 2023 22:35:02 GMT  
		Size: 8.0 MB (7951572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051177506124f7e3e7e3ee69487686f7ef4b0e98ce0756b40cdff883f8ad221`  
		Last Modified: Wed, 29 Mar 2023 22:35:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.17` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:2b872c9f38fbaa8ccd86aae99ff49be7ca0081947ff402419b4908daf58019e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10725973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf282fbb53d74f70eb62b53a208af332a235cc98c5c913b9c2ce328695079c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:27:45 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:27:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:27:48 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:27:48 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:27:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:27:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99adc85b7a7f0c407e58670682e492d2ed4d84e3ab1bb7027956969d00ebfc71`  
		Last Modified: Wed, 29 Mar 2023 19:28:01 GMT  
		Size: 7.6 MB (7614751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4909158433ab6374c50735598fc1b8ced59a9783484d5d81b17f79e340f51`  
		Last Modified: Wed, 29 Mar 2023 19:28:00 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.17` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:3dd42a0204775da869e619716598df034fdc2dc745fe54733e05283be46959a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10475540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc61fa844612cd4e06d2f86ec59df937bb440d8bf4d9136d8e6f31c9e6af6b60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:25:29 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Wed, 29 Mar 2023 19:25:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 29 Mar 2023 19:25:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 29 Mar 2023 19:25:32 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Mar 2023 19:25:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ff327778aa8c8454a9938f941121fa97bd7b586285cb6a129c21cd04d644d6`  
		Last Modified: Wed, 29 Mar 2023 19:26:04 GMT  
		Size: 7.6 MB (7606603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c1e330b4e950e4a13732095c4ed8bc3229d2036ab640e7211a90fc501e80a`  
		Last Modified: Wed, 29 Mar 2023 19:26:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:0991c0c32b4fbb8d20465613b726c4622735accfc4233ff74da6c519d7322d1f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10569273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd3e7b4045f60d83279ac66e4598fc69748776e5eef9c5e6399193136d3f784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 23:09:27 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Fri, 10 Feb 2023 23:09:30 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='250dbab0595befb22a54804ec9be48537f22da0b6a5970e984d84c28d19f70d5' ;; 		armhf) natsArch='arm6'; sha256='27c74e261ccd1374da227e8c31184a8e98d0820bdd916e9a681be7fba12f7f09' ;; 		armv7) natsArch='arm7'; sha256='3db62df2019c947b54ea943ecaa5d1e34db6855247e53ec7c8ad46d0c206a6c4' ;; 		x86_64) natsArch='amd64'; sha256='ac5beb0e820af18e422bef12200012d86237b98872e0ed48c985426315b02cbb' ;; 		x86) natsArch='386'; sha256='887527bb48ab6029cbc1583cfd09e608148342e50e71851dbfa4c88aefb3fd39' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 10 Feb 2023 23:09:30 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 10 Feb 2023 23:09:30 GMT
EXPOSE 4222 8222
# Fri, 10 Feb 2023 23:09:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 23:09:30 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0ea37a8f15a246683d21e808dad12d5fbd0f43c8d9b4c729b1a726d23dde9`  
		Last Modified: Fri, 10 Feb 2023 23:09:54 GMT  
		Size: 7.3 MB (7306894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1992f5b04c200b5fa7c595d620a4413f4705afbbf1e1273205e2648cfc95fa`  
		Last Modified: Fri, 10 Feb 2023 23:09:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:07031192d0940a2f9299bd3606738ef381e139dc840a0ee68a7e2542cdd053d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:73f07f50ce952ce448048e75d494ee6ed95eae0ad7275b712e8214552113960a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:d6049fac048e55a8e4f6c8ed4cb716d06bc558feea57b76f5081d24322f38b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d6049fac048e55a8e4f6c8ed4cb716d06bc558feea57b76f5081d24322f38b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:e511f2ae625328c64c892642593ec9d9c206d14d141e268633dd9213c85bbe56
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114483381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893fd84c6008de778f111bdbd19033488e2106cb147a8146a0f7c0e434f46e38`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 04:09:13 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:09:15 GMT
RUN cmd /S /C #(nop) COPY file:849c881d7b0e5994559eaa48b9cc851618ba91f60a4b0e8cb48b89862fd563c8 in C:\nats-streaming-server.exe 
# Thu, 16 Mar 2023 04:09:16 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:09:17 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:09:18 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989bf40c40575727f8231d233b462fde8f135997008e29030565a868625bf08e`  
		Last Modified: Thu, 16 Mar 2023 09:07:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ee05deac408cd1c6e5352c9308c42a254ecfd269af0065543175f95f442471`  
		Last Modified: Thu, 16 Mar 2023 09:09:13 GMT  
		Size: 7.8 MB (7794487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6214afd420799685270ba1f02c5cb96cf06b3f8a2e13f3c5002d253e48d13ca5`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02b96a7d3d37fa2a81bc3e24d5884560bb35bff7db68bca9ab5b92d84ad2b1`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd601f76a39faafe339d371df649d74b269e19564914b5b9c124bdf3a97361b`  
		Last Modified: Thu, 16 Mar 2023 09:09:11 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:73f07f50ce952ce448048e75d494ee6ed95eae0ad7275b712e8214552113960a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:1a8745712d00a54265c8552863b8d15a568b138368f4fcb090c075e361124c14
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7666171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a48bccf54f8248bddd0509da6d1cc1fe8b97638f6120c98e4c9fb191f6f1723`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:31:40 GMT
COPY file:379a895964ce5e0c1d6e137ee5ee8f0cbfb7fdbb8cb20ace28a5de2e106737eb in /nats-streaming-server 
# Thu, 12 Jan 2023 19:31:40 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:31:41 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:31:41 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:27e278d5ae53768a5d47168e25eb6824c8445f2866af5ea11943739d93ce14dd`  
		Last Modified: Thu, 12 Jan 2023 19:32:24 GMT  
		Size: 7.7 MB (7666171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:01c1adc9b48bd0eaf83deed2c829ba46ca7e195e485c64b91dfe60155372b90d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2496f5e117da007615485710e84d73fc0a353a004d88ce6bd42efbb52c5d4b92`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 14 Mar 2023 01:40:38 GMT
COPY file:1214576567fc0305b3b6ac3e280bb8d103f74aee2edde4b083a56167e41f0ed6 in /nats-streaming-server 
# Tue, 14 Mar 2023 01:40:38 GMT
EXPOSE 4222 8222
# Tue, 14 Mar 2023 01:40:38 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 14 Mar 2023 01:40:38 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c76ebdda577d691c315b52196919494198f01e7e8a34dac185a83423d3954e4f`  
		Last Modified: Thu, 12 Jan 2023 18:58:31 GMT  
		Size: 7.3 MB (7329068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:bcefecfcb6986469865e3d3d3fbb31f8101c56a77b76a3c3cb076ae08ab06ae8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6202a592a6aad13e30bce4ac90570fe13d8f28740d9ca9b75958c204953b43bd`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 19:25:37 GMT
COPY file:58653f0fa67e6667e5ec024a8b7912bc01a12570dac2c7550d04c2e617252bf1 in /nats-streaming-server 
# Wed, 29 Mar 2023 19:25:37 GMT
EXPOSE 4222 8222
# Wed, 29 Mar 2023 19:25:37 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Wed, 29 Mar 2023 19:25:37 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:edc8f5310312ee44896e1639c9af8d17c77c9fc7cfad03f8c1268ab57def8348`  
		Last Modified: Thu, 12 Jan 2023 19:12:45 GMT  
		Size: 7.3 MB (7318728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:56dfb1bed3b56ea0b72be1b79a49422abdde1189777ebfb55eda7223819eb6d3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7533789a178d97f2445ccdb62e46c98a1cec7249342ad21b5c40f38ee0652bff`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 12 Jan 2023 19:49:56 GMT
COPY file:33b7386a5076cd63bc03cf5c4de0f89afe8fd8034e8fd3a792715c6cb567514b in /nats-streaming-server 
# Thu, 12 Jan 2023 19:49:56 GMT
EXPOSE 4222 8222
# Thu, 12 Jan 2023 19:49:56 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 12 Jan 2023 19:49:56 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7cbef42b1eb11c382f636b05c7fea54926364454d6b2727ea8e52f63785a536`  
		Last Modified: Thu, 12 Jan 2023 19:50:42 GMT  
		Size: 7.0 MB (7019428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:67ecc474de4458dfff78cbddeea1c0505eec8c353d83d6d0346ef5e6332366a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:8d4771f8e1a5a0de3646def6dd9b6d7d2493e56de5984e668fd86153ebe56736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022130897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58b989bd8c98566448b87d746a8d9121e16906eb07b293bcb8d89c06ff848f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 04:05:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:05:13 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Mar 2023 04:05:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Mar 2023 04:05:15 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Mar 2023 04:06:40 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Mar 2023 04:08:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Mar 2023 04:08:56 GMT
EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:08:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:08:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c46bc18b88e816c6caaf34206ccb18a5b7f6665a73ae9a4678525d49fcb1f2`  
		Last Modified: Thu, 16 Mar 2023 09:07:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2879bcc35018c5e8a267f8042c62dd0c05fe41b234e85d986fee9c819cf65c18`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90235cb5c6d3898b39e2f35eb44a986ded127a99bbc8ec28e3f8cfcc4d29ed4`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01ba9a614aa82b0f534bfeb5dac8b1319b3d65cb6cf165e646a50c34d2961d0`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fc30400d336dfe957c7e151e9e7597f85f02daea9f164b26daa5eb6404952`  
		Last Modified: Thu, 16 Mar 2023 09:08:58 GMT  
		Size: 460.5 KB (460503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae978079933163805999ecc5807a9fce77bd9d6d4fb4bf408031613caba29f`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 8.2 MB (8150067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a68f46d1ea3ac895fe1af1b7a28b090b4ab3a03309a6f26ab5a6ae3bfe6c88`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901346ca0aa9486c1efe86f106c0a7bc67599332aed0a8d530d7092b136b2914`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6f2b6008f08f579439aa82acbdfe4319a182e42be05f9f6cf768a62ffba65`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:67ecc474de4458dfff78cbddeea1c0505eec8c353d83d6d0346ef5e6332366a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull nats-streaming@sha256:8d4771f8e1a5a0de3646def6dd9b6d7d2493e56de5984e668fd86153ebe56736
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2022130897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58b989bd8c98566448b87d746a8d9121e16906eb07b293bcb8d89c06ff848f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 04:05:12 GMT
ENV NATS_DOCKERIZED=1
# Thu, 16 Mar 2023 04:05:13 GMT
ENV NATS_STREAMING_SERVER=0.25.3
# Thu, 16 Mar 2023 04:05:14 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.3/nats-streaming-server-v0.25.3-windows-amd64.zip
# Thu, 16 Mar 2023 04:05:15 GMT
ENV NATS_STREAMING_SERVER_SHASUM=b25aab68b84cba76e3edec5d524d2a792f460127d159ecb4d2e6168c7635c10c
# Thu, 16 Mar 2023 04:06:40 GMT
RUN Set-PSDebug -Trace 2
# Thu, 16 Mar 2023 04:08:55 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 16 Mar 2023 04:08:56 GMT
EXPOSE 4222 8222
# Thu, 16 Mar 2023 04:08:57 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 16 Mar 2023 04:08:58 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c46bc18b88e816c6caaf34206ccb18a5b7f6665a73ae9a4678525d49fcb1f2`  
		Last Modified: Thu, 16 Mar 2023 09:07:26 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2879bcc35018c5e8a267f8042c62dd0c05fe41b234e85d986fee9c819cf65c18`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90235cb5c6d3898b39e2f35eb44a986ded127a99bbc8ec28e3f8cfcc4d29ed4`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01ba9a614aa82b0f534bfeb5dac8b1319b3d65cb6cf165e646a50c34d2961d0`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981fc30400d336dfe957c7e151e9e7597f85f02daea9f164b26daa5eb6404952`  
		Last Modified: Thu, 16 Mar 2023 09:08:58 GMT  
		Size: 460.5 KB (460503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ae978079933163805999ecc5807a9fce77bd9d6d4fb4bf408031613caba29f`  
		Last Modified: Thu, 16 Mar 2023 09:08:59 GMT  
		Size: 8.2 MB (8150067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a68f46d1ea3ac895fe1af1b7a28b090b4ab3a03309a6f26ab5a6ae3bfe6c88`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901346ca0aa9486c1efe86f106c0a7bc67599332aed0a8d530d7092b136b2914`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f6f2b6008f08f579439aa82acbdfe4319a182e42be05f9f6cf768a62ffba65`  
		Last Modified: Thu, 16 Mar 2023 09:08:57 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
