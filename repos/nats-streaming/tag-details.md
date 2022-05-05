<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.24`](#nats-streaming024)
-	[`nats-streaming:0.24-alpine`](#nats-streaming024-alpine)
-	[`nats-streaming:0.24-alpine3.15`](#nats-streaming024-alpine315)
-	[`nats-streaming:0.24-linux`](#nats-streaming024-linux)
-	[`nats-streaming:0.24-nanoserver`](#nats-streaming024-nanoserver)
-	[`nats-streaming:0.24-nanoserver-1809`](#nats-streaming024-nanoserver-1809)
-	[`nats-streaming:0.24-scratch`](#nats-streaming024-scratch)
-	[`nats-streaming:0.24-windowsservercore`](#nats-streaming024-windowsservercore)
-	[`nats-streaming:0.24-windowsservercore-1809`](#nats-streaming024-windowsservercore-1809)
-	[`nats-streaming:0.24.6`](#nats-streaming0246)
-	[`nats-streaming:0.24.6-alpine`](#nats-streaming0246-alpine)
-	[`nats-streaming:0.24.6-alpine3.15`](#nats-streaming0246-alpine315)
-	[`nats-streaming:0.24.6-linux`](#nats-streaming0246-linux)
-	[`nats-streaming:0.24.6-nanoserver`](#nats-streaming0246-nanoserver)
-	[`nats-streaming:0.24.6-nanoserver-1809`](#nats-streaming0246-nanoserver-1809)
-	[`nats-streaming:0.24.6-scratch`](#nats-streaming0246-scratch)
-	[`nats-streaming:0.24.6-windowsservercore`](#nats-streaming0246-windowsservercore)
-	[`nats-streaming:0.24.6-windowsservercore-1809`](#nats-streaming0246-windowsservercore-1809)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.15`](#nats-streamingalpine315)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)

## `nats-streaming:0.24`

```console
$ docker pull nats-streaming@sha256:64416f6cf82f4a0a316d0adf7fa8b7ee0680f33be2ddd858cb889f413bd1a71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine`

```console
$ docker pull nats-streaming@sha256:04f4227088cfccc5691c9de73e554d80b66e6190de39a39dc250164ae190c8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:0660cbe996af57149da2381c98eaa166d0548f9e98ade19d53844e5f56c8e89a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10251257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d13821d6e7a8a7dc69aafc616b434ef2e7acd90f3a4089dc3816c9e108f7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:29:41 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:29:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:29:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:29:44 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:29:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a1992fea02bc44b618e38765ed86a483f3e2f94014a3bad3d57e9eedce604`  
		Last Modified: Thu, 05 May 2022 01:30:11 GMT  
		Size: 7.4 MB (7436276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778cd6a2cabd080005e41bb7e0747efa310f0e1ea2d556a93e61e6540082a5b`  
		Last Modified: Thu, 05 May 2022 01:30:10 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9512d4a877ae78e8ed7afd062ee3f8627be93755159a8cdeb53a28452504213a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1ff20325cbf85ef8dfcc6f0af5583221d0454b2a7ae08280272796f1909d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:49:44 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:49:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:49:49 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:49:50 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0445b3d700dbdb47962609fb012bb9bf1903f2fe9d12fae0e80c6638cddca40`  
		Last Modified: Thu, 05 May 2022 00:51:33 GMT  
		Size: 6.9 MB (6944770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63ca9c208a437f674ac54425eebd9238b56f40df6b6644c20a0ddef31eb0e65`  
		Last Modified: Thu, 05 May 2022 00:51:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6449d0a95882d8698eeb7486adcc26d71b05da93bc97f120d299dfd9c556d901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9358928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddbf90d7d7fac47b5121aee447a581653d849453c4cefae9c8d287bd0af418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:14:51 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:14:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:14:55 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:14:56 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:14:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46402e0b221673d4aa98646cfed995a7aa41ca6df279f9b6a415cdc69ef5ffae`  
		Last Modified: Thu, 05 May 2022 01:16:41 GMT  
		Size: 6.9 MB (6934183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ec792c2275f373f20e94387765ed4782aa61862ddf0d346e579d0b516d5f`  
		Last Modified: Thu, 05 May 2022 01:16:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:70607fa197c24a83842fd943e3542f51ccdf7530f87fce924901d7b2a917bb18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66865361ba144c7aa2d58b3709ebd68b05f5f789923cffe065d696933980129b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:47:18 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:47:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:47:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:47:22 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:47:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a80b45f00cc9f993dd606fd644c625c4aba5f55591c67beb63b8a38cae65af`  
		Last Modified: Thu, 05 May 2022 00:48:12 GMT  
		Size: 6.9 MB (6854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fb995f385a5071f1344432048378156b3f420b49e014e77a860ab36ae42a70`  
		Last Modified: Thu, 05 May 2022 00:48:11 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine3.15`

```console
$ docker pull nats-streaming@sha256:04f4227088cfccc5691c9de73e554d80b66e6190de39a39dc250164ae190c8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:0660cbe996af57149da2381c98eaa166d0548f9e98ade19d53844e5f56c8e89a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10251257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d13821d6e7a8a7dc69aafc616b434ef2e7acd90f3a4089dc3816c9e108f7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:29:41 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:29:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:29:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:29:44 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:29:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a1992fea02bc44b618e38765ed86a483f3e2f94014a3bad3d57e9eedce604`  
		Last Modified: Thu, 05 May 2022 01:30:11 GMT  
		Size: 7.4 MB (7436276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778cd6a2cabd080005e41bb7e0747efa310f0e1ea2d556a93e61e6540082a5b`  
		Last Modified: Thu, 05 May 2022 01:30:10 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9512d4a877ae78e8ed7afd062ee3f8627be93755159a8cdeb53a28452504213a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1ff20325cbf85ef8dfcc6f0af5583221d0454b2a7ae08280272796f1909d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:49:44 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:49:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:49:49 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:49:50 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0445b3d700dbdb47962609fb012bb9bf1903f2fe9d12fae0e80c6638cddca40`  
		Last Modified: Thu, 05 May 2022 00:51:33 GMT  
		Size: 6.9 MB (6944770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63ca9c208a437f674ac54425eebd9238b56f40df6b6644c20a0ddef31eb0e65`  
		Last Modified: Thu, 05 May 2022 00:51:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6449d0a95882d8698eeb7486adcc26d71b05da93bc97f120d299dfd9c556d901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9358928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddbf90d7d7fac47b5121aee447a581653d849453c4cefae9c8d287bd0af418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:14:51 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:14:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:14:55 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:14:56 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:14:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46402e0b221673d4aa98646cfed995a7aa41ca6df279f9b6a415cdc69ef5ffae`  
		Last Modified: Thu, 05 May 2022 01:16:41 GMT  
		Size: 6.9 MB (6934183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ec792c2275f373f20e94387765ed4782aa61862ddf0d346e579d0b516d5f`  
		Last Modified: Thu, 05 May 2022 01:16:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:70607fa197c24a83842fd943e3542f51ccdf7530f87fce924901d7b2a917bb18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66865361ba144c7aa2d58b3709ebd68b05f5f789923cffe065d696933980129b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:47:18 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:47:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:47:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:47:22 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:47:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a80b45f00cc9f993dd606fd644c625c4aba5f55591c67beb63b8a38cae65af`  
		Last Modified: Thu, 05 May 2022 00:48:12 GMT  
		Size: 6.9 MB (6854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fb995f385a5071f1344432048378156b3f420b49e014e77a860ab36ae42a70`  
		Last Modified: Thu, 05 May 2022 00:48:11 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-linux`

```console
$ docker pull nats-streaming@sha256:33caf6415a6bccf5d7cb28a520ea38b6c028ca88b2837a0a2d8a5c484263f26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver`

```console
$ docker pull nats-streaming@sha256:4de80fbfeb8277288ff367518b4c7c5eb4e13ceb10eda02f84719b6695fc2716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:4de80fbfeb8277288ff367518b4c7c5eb4e13ceb10eda02f84719b6695fc2716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-scratch`

```console
$ docker pull nats-streaming@sha256:33caf6415a6bccf5d7cb28a520ea38b6c028ca88b2837a0a2d8a5c484263f26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore`

```console
$ docker pull nats-streaming@sha256:a4af7e56a104e9aaa1aaa5af48c1f44dea34b88d4f721aaff2428bfe4b182bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:ef676b47cf3ffa3d4e2cd340fb5d9584d66bdf76a8d9f40e73617a86399a4a05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723903668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2c70d1db40f8b24ad373ccbc9535bcd5bfe8a14a589735e28e1cbacbfbc98`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:15:53 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:15:54 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Thu, 05 May 2022 01:15:55 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Thu, 05 May 2022 01:17:25 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 May 2022 01:19:22 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 05 May 2022 01:19:23 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:24 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40bd9a224642115164a0346ead8070287baa4f672cfdf04f8683b75c126de8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511fedb99d6888da119ca4089fa37944c32881b1b5fb338e858967de8c7b49f8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133e393f94ad5bf4f20b8c9f3b623f8454ec5ba0bbf658e546c1976530133eb1`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4d89b1091ddd66fb4a4e56f5caee4b5f1b5363df4c075b689f35bfe447722`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 359.7 KB (359652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b61f58aca01d789e30e65d786c2a83bb27c4acd1a19e6b35afc41f3f83d9e`  
		Last Modified: Thu, 05 May 2022 01:20:16 GMT  
		Size: 7.6 MB (7612442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36a852a6236903097a663fed5948ee32316ce62181c4ded0c58ed0f1f844a6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc52d18293739301bf2cee591645363390e23b756e697404ca34469a604ffe6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5771987c3cc39a43b1ea0f2afa718b2ca29125f0d284e1c57530a00ce91ff`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:a4af7e56a104e9aaa1aaa5af48c1f44dea34b88d4f721aaff2428bfe4b182bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:ef676b47cf3ffa3d4e2cd340fb5d9584d66bdf76a8d9f40e73617a86399a4a05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723903668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2c70d1db40f8b24ad373ccbc9535bcd5bfe8a14a589735e28e1cbacbfbc98`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:15:53 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:15:54 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Thu, 05 May 2022 01:15:55 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Thu, 05 May 2022 01:17:25 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 May 2022 01:19:22 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 05 May 2022 01:19:23 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:24 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40bd9a224642115164a0346ead8070287baa4f672cfdf04f8683b75c126de8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511fedb99d6888da119ca4089fa37944c32881b1b5fb338e858967de8c7b49f8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133e393f94ad5bf4f20b8c9f3b623f8454ec5ba0bbf658e546c1976530133eb1`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4d89b1091ddd66fb4a4e56f5caee4b5f1b5363df4c075b689f35bfe447722`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 359.7 KB (359652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b61f58aca01d789e30e65d786c2a83bb27c4acd1a19e6b35afc41f3f83d9e`  
		Last Modified: Thu, 05 May 2022 01:20:16 GMT  
		Size: 7.6 MB (7612442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36a852a6236903097a663fed5948ee32316ce62181c4ded0c58ed0f1f844a6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc52d18293739301bf2cee591645363390e23b756e697404ca34469a604ffe6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5771987c3cc39a43b1ea0f2afa718b2ca29125f0d284e1c57530a00ce91ff`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6`

```console
$ docker pull nats-streaming@sha256:64416f6cf82f4a0a316d0adf7fa8b7ee0680f33be2ddd858cb889f413bd1a71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24.6` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-alpine`

```console
$ docker pull nats-streaming@sha256:04f4227088cfccc5691c9de73e554d80b66e6190de39a39dc250164ae190c8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.6-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:0660cbe996af57149da2381c98eaa166d0548f9e98ade19d53844e5f56c8e89a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10251257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d13821d6e7a8a7dc69aafc616b434ef2e7acd90f3a4089dc3816c9e108f7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:29:41 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:29:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:29:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:29:44 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:29:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a1992fea02bc44b618e38765ed86a483f3e2f94014a3bad3d57e9eedce604`  
		Last Modified: Thu, 05 May 2022 01:30:11 GMT  
		Size: 7.4 MB (7436276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778cd6a2cabd080005e41bb7e0747efa310f0e1ea2d556a93e61e6540082a5b`  
		Last Modified: Thu, 05 May 2022 01:30:10 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9512d4a877ae78e8ed7afd062ee3f8627be93755159a8cdeb53a28452504213a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1ff20325cbf85ef8dfcc6f0af5583221d0454b2a7ae08280272796f1909d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:49:44 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:49:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:49:49 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:49:50 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0445b3d700dbdb47962609fb012bb9bf1903f2fe9d12fae0e80c6638cddca40`  
		Last Modified: Thu, 05 May 2022 00:51:33 GMT  
		Size: 6.9 MB (6944770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63ca9c208a437f674ac54425eebd9238b56f40df6b6644c20a0ddef31eb0e65`  
		Last Modified: Thu, 05 May 2022 00:51:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6449d0a95882d8698eeb7486adcc26d71b05da93bc97f120d299dfd9c556d901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9358928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddbf90d7d7fac47b5121aee447a581653d849453c4cefae9c8d287bd0af418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:14:51 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:14:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:14:55 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:14:56 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:14:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46402e0b221673d4aa98646cfed995a7aa41ca6df279f9b6a415cdc69ef5ffae`  
		Last Modified: Thu, 05 May 2022 01:16:41 GMT  
		Size: 6.9 MB (6934183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ec792c2275f373f20e94387765ed4782aa61862ddf0d346e579d0b516d5f`  
		Last Modified: Thu, 05 May 2022 01:16:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:70607fa197c24a83842fd943e3542f51ccdf7530f87fce924901d7b2a917bb18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66865361ba144c7aa2d58b3709ebd68b05f5f789923cffe065d696933980129b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:47:18 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:47:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:47:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:47:22 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:47:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a80b45f00cc9f993dd606fd644c625c4aba5f55591c67beb63b8a38cae65af`  
		Last Modified: Thu, 05 May 2022 00:48:12 GMT  
		Size: 6.9 MB (6854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fb995f385a5071f1344432048378156b3f420b49e014e77a860ab36ae42a70`  
		Last Modified: Thu, 05 May 2022 00:48:11 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-alpine3.15`

```console
$ docker pull nats-streaming@sha256:04f4227088cfccc5691c9de73e554d80b66e6190de39a39dc250164ae190c8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.6-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:0660cbe996af57149da2381c98eaa166d0548f9e98ade19d53844e5f56c8e89a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10251257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d13821d6e7a8a7dc69aafc616b434ef2e7acd90f3a4089dc3816c9e108f7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:29:41 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:29:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:29:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:29:44 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:29:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a1992fea02bc44b618e38765ed86a483f3e2f94014a3bad3d57e9eedce604`  
		Last Modified: Thu, 05 May 2022 01:30:11 GMT  
		Size: 7.4 MB (7436276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778cd6a2cabd080005e41bb7e0747efa310f0e1ea2d556a93e61e6540082a5b`  
		Last Modified: Thu, 05 May 2022 01:30:10 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9512d4a877ae78e8ed7afd062ee3f8627be93755159a8cdeb53a28452504213a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1ff20325cbf85ef8dfcc6f0af5583221d0454b2a7ae08280272796f1909d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:49:44 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:49:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:49:49 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:49:50 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0445b3d700dbdb47962609fb012bb9bf1903f2fe9d12fae0e80c6638cddca40`  
		Last Modified: Thu, 05 May 2022 00:51:33 GMT  
		Size: 6.9 MB (6944770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63ca9c208a437f674ac54425eebd9238b56f40df6b6644c20a0ddef31eb0e65`  
		Last Modified: Thu, 05 May 2022 00:51:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6449d0a95882d8698eeb7486adcc26d71b05da93bc97f120d299dfd9c556d901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9358928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddbf90d7d7fac47b5121aee447a581653d849453c4cefae9c8d287bd0af418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:14:51 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:14:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:14:55 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:14:56 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:14:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46402e0b221673d4aa98646cfed995a7aa41ca6df279f9b6a415cdc69ef5ffae`  
		Last Modified: Thu, 05 May 2022 01:16:41 GMT  
		Size: 6.9 MB (6934183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ec792c2275f373f20e94387765ed4782aa61862ddf0d346e579d0b516d5f`  
		Last Modified: Thu, 05 May 2022 01:16:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:70607fa197c24a83842fd943e3542f51ccdf7530f87fce924901d7b2a917bb18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66865361ba144c7aa2d58b3709ebd68b05f5f789923cffe065d696933980129b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:47:18 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:47:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:47:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:47:22 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:47:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a80b45f00cc9f993dd606fd644c625c4aba5f55591c67beb63b8a38cae65af`  
		Last Modified: Thu, 05 May 2022 00:48:12 GMT  
		Size: 6.9 MB (6854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fb995f385a5071f1344432048378156b3f420b49e014e77a860ab36ae42a70`  
		Last Modified: Thu, 05 May 2022 00:48:11 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-linux`

```console
$ docker pull nats-streaming@sha256:33caf6415a6bccf5d7cb28a520ea38b6c028ca88b2837a0a2d8a5c484263f26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.6-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-nanoserver`

```console
$ docker pull nats-streaming@sha256:4de80fbfeb8277288ff367518b4c7c5eb4e13ceb10eda02f84719b6695fc2716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24.6-nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:4de80fbfeb8277288ff367518b4c7c5eb4e13ceb10eda02f84719b6695fc2716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24.6-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-scratch`

```console
$ docker pull nats-streaming@sha256:33caf6415a6bccf5d7cb28a520ea38b6c028ca88b2837a0a2d8a5c484263f26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.6-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-windowsservercore`

```console
$ docker pull nats-streaming@sha256:a4af7e56a104e9aaa1aaa5af48c1f44dea34b88d4f721aaff2428bfe4b182bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24.6-windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:ef676b47cf3ffa3d4e2cd340fb5d9584d66bdf76a8d9f40e73617a86399a4a05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723903668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2c70d1db40f8b24ad373ccbc9535bcd5bfe8a14a589735e28e1cbacbfbc98`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:15:53 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:15:54 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Thu, 05 May 2022 01:15:55 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Thu, 05 May 2022 01:17:25 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 May 2022 01:19:22 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 05 May 2022 01:19:23 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:24 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40bd9a224642115164a0346ead8070287baa4f672cfdf04f8683b75c126de8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511fedb99d6888da119ca4089fa37944c32881b1b5fb338e858967de8c7b49f8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133e393f94ad5bf4f20b8c9f3b623f8454ec5ba0bbf658e546c1976530133eb1`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4d89b1091ddd66fb4a4e56f5caee4b5f1b5363df4c075b689f35bfe447722`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 359.7 KB (359652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b61f58aca01d789e30e65d786c2a83bb27c4acd1a19e6b35afc41f3f83d9e`  
		Last Modified: Thu, 05 May 2022 01:20:16 GMT  
		Size: 7.6 MB (7612442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36a852a6236903097a663fed5948ee32316ce62181c4ded0c58ed0f1f844a6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc52d18293739301bf2cee591645363390e23b756e697404ca34469a604ffe6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5771987c3cc39a43b1ea0f2afa718b2ca29125f0d284e1c57530a00ce91ff`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:a4af7e56a104e9aaa1aaa5af48c1f44dea34b88d4f721aaff2428bfe4b182bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:0.24.6-windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:ef676b47cf3ffa3d4e2cd340fb5d9584d66bdf76a8d9f40e73617a86399a4a05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723903668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2c70d1db40f8b24ad373ccbc9535bcd5bfe8a14a589735e28e1cbacbfbc98`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:15:53 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:15:54 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Thu, 05 May 2022 01:15:55 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Thu, 05 May 2022 01:17:25 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 May 2022 01:19:22 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 05 May 2022 01:19:23 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:24 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40bd9a224642115164a0346ead8070287baa4f672cfdf04f8683b75c126de8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511fedb99d6888da119ca4089fa37944c32881b1b5fb338e858967de8c7b49f8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133e393f94ad5bf4f20b8c9f3b623f8454ec5ba0bbf658e546c1976530133eb1`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4d89b1091ddd66fb4a4e56f5caee4b5f1b5363df4c075b689f35bfe447722`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 359.7 KB (359652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b61f58aca01d789e30e65d786c2a83bb27c4acd1a19e6b35afc41f3f83d9e`  
		Last Modified: Thu, 05 May 2022 01:20:16 GMT  
		Size: 7.6 MB (7612442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36a852a6236903097a663fed5948ee32316ce62181c4ded0c58ed0f1f844a6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc52d18293739301bf2cee591645363390e23b756e697404ca34469a604ffe6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5771987c3cc39a43b1ea0f2afa718b2ca29125f0d284e1c57530a00ce91ff`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:04f4227088cfccc5691c9de73e554d80b66e6190de39a39dc250164ae190c8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:0660cbe996af57149da2381c98eaa166d0548f9e98ade19d53844e5f56c8e89a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10251257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d13821d6e7a8a7dc69aafc616b434ef2e7acd90f3a4089dc3816c9e108f7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:29:41 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:29:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:29:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:29:44 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:29:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a1992fea02bc44b618e38765ed86a483f3e2f94014a3bad3d57e9eedce604`  
		Last Modified: Thu, 05 May 2022 01:30:11 GMT  
		Size: 7.4 MB (7436276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778cd6a2cabd080005e41bb7e0747efa310f0e1ea2d556a93e61e6540082a5b`  
		Last Modified: Thu, 05 May 2022 01:30:10 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9512d4a877ae78e8ed7afd062ee3f8627be93755159a8cdeb53a28452504213a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1ff20325cbf85ef8dfcc6f0af5583221d0454b2a7ae08280272796f1909d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:49:44 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:49:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:49:49 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:49:50 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0445b3d700dbdb47962609fb012bb9bf1903f2fe9d12fae0e80c6638cddca40`  
		Last Modified: Thu, 05 May 2022 00:51:33 GMT  
		Size: 6.9 MB (6944770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63ca9c208a437f674ac54425eebd9238b56f40df6b6644c20a0ddef31eb0e65`  
		Last Modified: Thu, 05 May 2022 00:51:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6449d0a95882d8698eeb7486adcc26d71b05da93bc97f120d299dfd9c556d901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9358928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddbf90d7d7fac47b5121aee447a581653d849453c4cefae9c8d287bd0af418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:14:51 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:14:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:14:55 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:14:56 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:14:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46402e0b221673d4aa98646cfed995a7aa41ca6df279f9b6a415cdc69ef5ffae`  
		Last Modified: Thu, 05 May 2022 01:16:41 GMT  
		Size: 6.9 MB (6934183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ec792c2275f373f20e94387765ed4782aa61862ddf0d346e579d0b516d5f`  
		Last Modified: Thu, 05 May 2022 01:16:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:70607fa197c24a83842fd943e3542f51ccdf7530f87fce924901d7b2a917bb18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66865361ba144c7aa2d58b3709ebd68b05f5f789923cffe065d696933980129b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:47:18 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:47:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:47:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:47:22 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:47:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a80b45f00cc9f993dd606fd644c625c4aba5f55591c67beb63b8a38cae65af`  
		Last Modified: Thu, 05 May 2022 00:48:12 GMT  
		Size: 6.9 MB (6854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fb995f385a5071f1344432048378156b3f420b49e014e77a860ab36ae42a70`  
		Last Modified: Thu, 05 May 2022 00:48:11 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.15`

```console
$ docker pull nats-streaming@sha256:04f4227088cfccc5691c9de73e554d80b66e6190de39a39dc250164ae190c8fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:0660cbe996af57149da2381c98eaa166d0548f9e98ade19d53844e5f56c8e89a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10251257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d13821d6e7a8a7dc69aafc616b434ef2e7acd90f3a4089dc3816c9e108f7f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:29:41 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:29:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:29:44 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:29:44 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:29:44 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4a1992fea02bc44b618e38765ed86a483f3e2f94014a3bad3d57e9eedce604`  
		Last Modified: Thu, 05 May 2022 01:30:11 GMT  
		Size: 7.4 MB (7436276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778cd6a2cabd080005e41bb7e0747efa310f0e1ea2d556a93e61e6540082a5b`  
		Last Modified: Thu, 05 May 2022 01:30:10 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:9512d4a877ae78e8ed7afd062ee3f8627be93755159a8cdeb53a28452504213a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9567164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1ff20325cbf85ef8dfcc6f0af5583221d0454b2a7ae08280272796f1909d5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:49:44 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:49:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:49:49 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:49:49 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:49:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:49:50 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0445b3d700dbdb47962609fb012bb9bf1903f2fe9d12fae0e80c6638cddca40`  
		Last Modified: Thu, 05 May 2022 00:51:33 GMT  
		Size: 6.9 MB (6944770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63ca9c208a437f674ac54425eebd9238b56f40df6b6644c20a0ddef31eb0e65`  
		Last Modified: Thu, 05 May 2022 00:51:28 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:6449d0a95882d8698eeb7486adcc26d71b05da93bc97f120d299dfd9c556d901
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9358928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ddbf90d7d7fac47b5121aee447a581653d849453c4cefae9c8d287bd0af418`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 01:14:51 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:14:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 01:14:55 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 01:14:56 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 01:14:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46402e0b221673d4aa98646cfed995a7aa41ca6df279f9b6a415cdc69ef5ffae`  
		Last Modified: Thu, 05 May 2022 01:16:41 GMT  
		Size: 6.9 MB (6934183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b9ec792c2275f373f20e94387765ed4782aa61862ddf0d346e579d0b516d5f`  
		Last Modified: Thu, 05 May 2022 01:16:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:70607fa197c24a83842fd943e3542f51ccdf7530f87fce924901d7b2a917bb18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9571223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66865361ba144c7aa2d58b3709ebd68b05f5f789923cffe065d696933980129b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 05 May 2022 00:47:18 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 00:47:20 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 05 May 2022 00:47:22 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 05 May 2022 00:47:22 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 May 2022 00:47:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a80b45f00cc9f993dd606fd644c625c4aba5f55591c67beb63b8a38cae65af`  
		Last Modified: Thu, 05 May 2022 00:48:12 GMT  
		Size: 6.9 MB (6854323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fb995f385a5071f1344432048378156b3f420b49e014e77a860ab36ae42a70`  
		Last Modified: Thu, 05 May 2022 00:48:11 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:64416f6cf82f4a0a316d0adf7fa8b7ee0680f33be2ddd858cb889f413bd1a71f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:33caf6415a6bccf5d7cb28a520ea38b6c028ca88b2837a0a2d8a5c484263f26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:4de80fbfeb8277288ff367518b4c7c5eb4e13ceb10eda02f84719b6695fc2716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:4de80fbfeb8277288ff367518b4c7c5eb4e13ceb10eda02f84719b6695fc2716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:70457d59bf8f641124aa7b3c848841338ee28f012260a0f6458186aed0ccb5d3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110376627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f0f50108112053bde00c6f878cdbf5c09cc7e463174a06e20bc5ee3b2b09b8`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 14:45:42 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:19:37 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Thu, 05 May 2022 01:19:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:39 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:40 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a6063f744e542c21ce471bdd7ff0dd6063d8d2a9670afbbc64d086813afd6385`  
		Last Modified: Wed, 13 Apr 2022 14:46:35 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ed23ac1eee671c5c89470fe85f192d11e27753dbd11a1247ff5dd42789274`  
		Last Modified: Thu, 05 May 2022 01:20:36 GMT  
		Size: 7.3 MB (7275843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19d983b61231bf40f681d8042f2acfca8443e1639df10ce95d575f5a02d7d5`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e73853c427db84509c80e49720d7689e966d235b52a8a9b19cd39aad28568b`  
		Last Modified: Thu, 05 May 2022 01:20:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73881baa094fec2fd243f7ad489585665de0fab78678f7953b88f2234e863093`  
		Last Modified: Thu, 05 May 2022 01:20:29 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:33caf6415a6bccf5d7cb28a520ea38b6c028ca88b2837a0a2d8a5c484263f26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:87746b2f927452b109461f56e64e379041225cd9c1835458ea1a629343d8b2d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7163528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c92c14c5eef9b01a2331fda3d92f13323aad939cfa97d06664b3f7c76f10fe8`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:29:51 GMT
COPY file:af99aecf0be2bf06fd4ff3bdc596084c5f5b9148b321dce7ba96abc44cef84e4 in /nats-streaming-server 
# Thu, 05 May 2022 01:29:51 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:29:51 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:29:51 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:86332753e6d2e6b137051bf8ad5c8d26bd40197ba63a859e7bb995b16e64d585`  
		Last Modified: Thu, 05 May 2022 01:30:31 GMT  
		Size: 7.2 MB (7163528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:216b5f0964cd7471ebf0037fa3126f199e1292ff46d4069b9f3cece4c475dfc9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e22671d6d6f173c32a87a982bf9342f90f9857aec21e12fb5d0d8c3415671e5`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:50:08 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Thu, 05 May 2022 00:50:09 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:50:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:50:10 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:483473a69686f36fbe35dd927da6e8dc5c3cf6289eb693f4a2a1053e34857b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb2ec92fe256d5a1b10c9a5af6a5dbc95050f2087623c2e5073a8e0c055dc14`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 01:15:17 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Thu, 05 May 2022 01:15:18 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:15:18 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 01:15:18 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7a2960da85bfc4ed3ab05fd7f800679b3d8b9fb0109e72928f073e22b189272`  
		Last Modified: Thu, 05 May 2022 01:17:11 GMT  
		Size: 6.7 MB (6662010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:afcafb3e5a8f8fad8d3d0a932cf124d89506aae3145fbc129312396e7151fce2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6581373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b922cbf06d107410a6830e6d08ae5cf567c9d820d17d35d9f677141e81a7697`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 00:47:33 GMT
COPY file:8c668f30364968805c5e68fa1df8dd1896541062cbb6f11a30bc0f7b4f154f91 in /nats-streaming-server 
# Thu, 05 May 2022 00:47:33 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 00:47:34 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Thu, 05 May 2022 00:47:35 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f3a5ffa8526605d52a17c89ac2550f3d06ebb996569a816e8a2faab246f37f1b`  
		Last Modified: Thu, 05 May 2022 00:48:35 GMT  
		Size: 6.6 MB (6581373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:a4af7e56a104e9aaa1aaa5af48c1f44dea34b88d4f721aaff2428bfe4b182bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:ef676b47cf3ffa3d4e2cd340fb5d9584d66bdf76a8d9f40e73617a86399a4a05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723903668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2c70d1db40f8b24ad373ccbc9535bcd5bfe8a14a589735e28e1cbacbfbc98`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:15:53 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:15:54 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Thu, 05 May 2022 01:15:55 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Thu, 05 May 2022 01:17:25 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 May 2022 01:19:22 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 05 May 2022 01:19:23 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:24 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40bd9a224642115164a0346ead8070287baa4f672cfdf04f8683b75c126de8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511fedb99d6888da119ca4089fa37944c32881b1b5fb338e858967de8c7b49f8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133e393f94ad5bf4f20b8c9f3b623f8454ec5ba0bbf658e546c1976530133eb1`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4d89b1091ddd66fb4a4e56f5caee4b5f1b5363df4c075b689f35bfe447722`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 359.7 KB (359652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b61f58aca01d789e30e65d786c2a83bb27c4acd1a19e6b35afc41f3f83d9e`  
		Last Modified: Thu, 05 May 2022 01:20:16 GMT  
		Size: 7.6 MB (7612442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36a852a6236903097a663fed5948ee32316ce62181c4ded0c58ed0f1f844a6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc52d18293739301bf2cee591645363390e23b756e697404ca34469a604ffe6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5771987c3cc39a43b1ea0f2afa718b2ca29125f0d284e1c57530a00ce91ff`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:a4af7e56a104e9aaa1aaa5af48c1f44dea34b88d4f721aaff2428bfe4b182bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull nats-streaming@sha256:ef676b47cf3ffa3d4e2cd340fb5d9584d66bdf76a8d9f40e73617a86399a4a05
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2723903668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae2c70d1db40f8b24ad373ccbc9535bcd5bfe8a14a589735e28e1cbacbfbc98`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 12:43:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Apr 2022 14:42:30 GMT
ENV NATS_DOCKERIZED=1
# Thu, 05 May 2022 01:15:53 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Thu, 05 May 2022 01:15:54 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Thu, 05 May 2022 01:15:55 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Thu, 05 May 2022 01:17:25 GMT
RUN Set-PSDebug -Trace 2
# Thu, 05 May 2022 01:19:22 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 05 May 2022 01:19:23 GMT
EXPOSE 4222 8222
# Thu, 05 May 2022 01:19:24 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 05 May 2022 01:19:25 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ebb23aa64bff633cfa3c62b190d84f0e870b04fecb1910f65d0870b5c7f8981`  
		Last Modified: Wed, 13 Apr 2022 14:12:24 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d838c7a98a95bee63894bac798124e8c8572bcacc23e22d85332d453a03a7d7c`  
		Last Modified: Wed, 13 Apr 2022 14:46:17 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd40bd9a224642115164a0346ead8070287baa4f672cfdf04f8683b75c126de8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511fedb99d6888da119ca4089fa37944c32881b1b5fb338e858967de8c7b49f8`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133e393f94ad5bf4f20b8c9f3b623f8454ec5ba0bbf658e546c1976530133eb1`  
		Last Modified: Thu, 05 May 2022 01:20:10 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c4d89b1091ddd66fb4a4e56f5caee4b5f1b5363df4c075b689f35bfe447722`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 359.7 KB (359652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73b61f58aca01d789e30e65d786c2a83bb27c4acd1a19e6b35afc41f3f83d9e`  
		Last Modified: Thu, 05 May 2022 01:20:16 GMT  
		Size: 7.6 MB (7612442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af36a852a6236903097a663fed5948ee32316ce62181c4ded0c58ed0f1f844a6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc52d18293739301bf2cee591645363390e23b756e697404ca34469a604ffe6`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec5771987c3cc39a43b1ea0f2afa718b2ca29125f0d284e1c57530a00ce91ff`  
		Last Modified: Thu, 05 May 2022 01:20:08 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
