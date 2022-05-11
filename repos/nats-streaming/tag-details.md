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
$ docker pull nats-streaming@sha256:e0624a3db286bfb3b2d8e720265c18716b1acd6a4c794cf819f2051ec0c55882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

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

### `nats-streaming:0.24` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
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
$ docker pull nats-streaming@sha256:617a3e9e8eac6906f8f5a2f959cb9f79a7922bf64591b1fc581bf684f21e4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:617a3e9e8eac6906f8f5a2f959cb9f79a7922bf64591b1fc581bf684f21e4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
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
$ docker pull nats-streaming@sha256:d68ec26ab81994c8142ad8f24f5642b4c4398b61a9da446ccbffe53db6f110ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:0df66a3e69a3bf2e0a227f1fb870bde32badb04d3d11e62a78e7fb520cde69ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2512156670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db51f87e79820c2b2396793cf1b83e81e68ee0afad5f04f979211715ea2194b3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:30:32 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 11 May 2022 16:30:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 11 May 2022 16:30:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 11 May 2022 16:31:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 16:32:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 16:32:59 GMT
EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414182f3892da8f7d095665f62200d67f6f8d2e246b130708b2b88a21687c3b`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164dca4c618438c46a2dc1963e12b45c2f8d43eef1d1fe7fae7e1c8c4e05ff0`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40e75ccc6601c1be113a440f55f08afdecc037cdac48a489fdb828a760e8a8`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c46d136ed5db00b4518191e335ea48c04342ffbc2c41da9beeabc326232cb0d`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 482.5 KB (482509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9183e4d25dff6451cdfedc68317c4dd57922535f5d6aa35c5fb21dac3734fef`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 7.6 MB (7607166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bec91034c767639b4ccbb6a280e45a12dd83565d0f24400b5bb5a291c40cb7`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7dc716bc45aacd9709e081731dbf3715f48204651675a9177cafd8253f5dd`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b5bf987b96cb6c0b09277a5ba367b7ce2f6c83dd0412319b03eb875d90030`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:d68ec26ab81994c8142ad8f24f5642b4c4398b61a9da446ccbffe53db6f110ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:0df66a3e69a3bf2e0a227f1fb870bde32badb04d3d11e62a78e7fb520cde69ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2512156670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db51f87e79820c2b2396793cf1b83e81e68ee0afad5f04f979211715ea2194b3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:30:32 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 11 May 2022 16:30:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 11 May 2022 16:30:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 11 May 2022 16:31:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 16:32:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 16:32:59 GMT
EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414182f3892da8f7d095665f62200d67f6f8d2e246b130708b2b88a21687c3b`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164dca4c618438c46a2dc1963e12b45c2f8d43eef1d1fe7fae7e1c8c4e05ff0`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40e75ccc6601c1be113a440f55f08afdecc037cdac48a489fdb828a760e8a8`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c46d136ed5db00b4518191e335ea48c04342ffbc2c41da9beeabc326232cb0d`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 482.5 KB (482509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9183e4d25dff6451cdfedc68317c4dd57922535f5d6aa35c5fb21dac3734fef`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 7.6 MB (7607166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bec91034c767639b4ccbb6a280e45a12dd83565d0f24400b5bb5a291c40cb7`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7dc716bc45aacd9709e081731dbf3715f48204651675a9177cafd8253f5dd`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b5bf987b96cb6c0b09277a5ba367b7ce2f6c83dd0412319b03eb875d90030`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6`

```console
$ docker pull nats-streaming@sha256:e0624a3db286bfb3b2d8e720265c18716b1acd6a4c794cf819f2051ec0c55882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

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

### `nats-streaming:0.24.6` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
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
$ docker pull nats-streaming@sha256:617a3e9e8eac6906f8f5a2f959cb9f79a7922bf64591b1fc581bf684f21e4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24.6-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:617a3e9e8eac6906f8f5a2f959cb9f79a7922bf64591b1fc581bf684f21e4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24.6-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
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
$ docker pull nats-streaming@sha256:d68ec26ab81994c8142ad8f24f5642b4c4398b61a9da446ccbffe53db6f110ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24.6-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:0df66a3e69a3bf2e0a227f1fb870bde32badb04d3d11e62a78e7fb520cde69ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2512156670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db51f87e79820c2b2396793cf1b83e81e68ee0afad5f04f979211715ea2194b3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:30:32 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 11 May 2022 16:30:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 11 May 2022 16:30:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 11 May 2022 16:31:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 16:32:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 16:32:59 GMT
EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414182f3892da8f7d095665f62200d67f6f8d2e246b130708b2b88a21687c3b`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164dca4c618438c46a2dc1963e12b45c2f8d43eef1d1fe7fae7e1c8c4e05ff0`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40e75ccc6601c1be113a440f55f08afdecc037cdac48a489fdb828a760e8a8`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c46d136ed5db00b4518191e335ea48c04342ffbc2c41da9beeabc326232cb0d`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 482.5 KB (482509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9183e4d25dff6451cdfedc68317c4dd57922535f5d6aa35c5fb21dac3734fef`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 7.6 MB (7607166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bec91034c767639b4ccbb6a280e45a12dd83565d0f24400b5bb5a291c40cb7`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7dc716bc45aacd9709e081731dbf3715f48204651675a9177cafd8253f5dd`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b5bf987b96cb6c0b09277a5ba367b7ce2f6c83dd0412319b03eb875d90030`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:d68ec26ab81994c8142ad8f24f5642b4c4398b61a9da446ccbffe53db6f110ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:0.24.6-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:0df66a3e69a3bf2e0a227f1fb870bde32badb04d3d11e62a78e7fb520cde69ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2512156670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db51f87e79820c2b2396793cf1b83e81e68ee0afad5f04f979211715ea2194b3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:30:32 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 11 May 2022 16:30:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 11 May 2022 16:30:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 11 May 2022 16:31:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 16:32:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 16:32:59 GMT
EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414182f3892da8f7d095665f62200d67f6f8d2e246b130708b2b88a21687c3b`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164dca4c618438c46a2dc1963e12b45c2f8d43eef1d1fe7fae7e1c8c4e05ff0`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40e75ccc6601c1be113a440f55f08afdecc037cdac48a489fdb828a760e8a8`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c46d136ed5db00b4518191e335ea48c04342ffbc2c41da9beeabc326232cb0d`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 482.5 KB (482509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9183e4d25dff6451cdfedc68317c4dd57922535f5d6aa35c5fb21dac3734fef`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 7.6 MB (7607166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bec91034c767639b4ccbb6a280e45a12dd83565d0f24400b5bb5a291c40cb7`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7dc716bc45aacd9709e081731dbf3715f48204651675a9177cafd8253f5dd`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b5bf987b96cb6c0b09277a5ba367b7ce2f6c83dd0412319b03eb875d90030`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1424 bytes)  
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
$ docker pull nats-streaming@sha256:e0624a3db286bfb3b2d8e720265c18716b1acd6a4c794cf819f2051ec0c55882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

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

### `nats-streaming:latest` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
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
$ docker pull nats-streaming@sha256:617a3e9e8eac6906f8f5a2f959cb9f79a7922bf64591b1fc581bf684f21e4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:617a3e9e8eac6906f8f5a2f959cb9f79a7922bf64591b1fc581bf684f21e4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:ba50a69c7a44ba4ec85a16785541cebaace7f6383f74222bb6012754b36de907
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110414318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb8a4bc550c1a47ab79924ff30e2fef56d61bc941135ffcb45fda547c1ee63d`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:33:19 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 11 May 2022 16:33:20 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:21 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:22 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dc00a610dcad8dfb524042bf96fa3fbb72854be566327f8ffef9898e59efa6`  
		Last Modified: Wed, 11 May 2022 16:34:11 GMT  
		Size: 7.3 MB (7275853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3db9d9c09fe3bf99a3f05ed4d46b3f4d6989ea139fe444972491d53a5de46f`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8919b36682efc38a12c7069d4478a6fb35c3c3b07c291d70f30f2d309dfd1ea`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bea12eedf00a682a8ebb4c0bf03481106e01461e72d06804458286d9792ab7`  
		Last Modified: Wed, 11 May 2022 16:34:04 GMT  
		Size: 1.2 KB (1158 bytes)  
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
$ docker pull nats-streaming@sha256:d68ec26ab81994c8142ad8f24f5642b4c4398b61a9da446ccbffe53db6f110ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:0df66a3e69a3bf2e0a227f1fb870bde32badb04d3d11e62a78e7fb520cde69ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2512156670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db51f87e79820c2b2396793cf1b83e81e68ee0afad5f04f979211715ea2194b3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:30:32 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 11 May 2022 16:30:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 11 May 2022 16:30:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 11 May 2022 16:31:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 16:32:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 16:32:59 GMT
EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414182f3892da8f7d095665f62200d67f6f8d2e246b130708b2b88a21687c3b`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164dca4c618438c46a2dc1963e12b45c2f8d43eef1d1fe7fae7e1c8c4e05ff0`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40e75ccc6601c1be113a440f55f08afdecc037cdac48a489fdb828a760e8a8`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c46d136ed5db00b4518191e335ea48c04342ffbc2c41da9beeabc326232cb0d`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 482.5 KB (482509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9183e4d25dff6451cdfedc68317c4dd57922535f5d6aa35c5fb21dac3734fef`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 7.6 MB (7607166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bec91034c767639b4ccbb6a280e45a12dd83565d0f24400b5bb5a291c40cb7`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7dc716bc45aacd9709e081731dbf3715f48204651675a9177cafd8253f5dd`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b5bf987b96cb6c0b09277a5ba367b7ce2f6c83dd0412319b03eb875d90030`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:d68ec26ab81994c8142ad8f24f5642b4c4398b61a9da446ccbffe53db6f110ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats-streaming@sha256:0df66a3e69a3bf2e0a227f1fb870bde32badb04d3d11e62a78e7fb520cde69ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2512156670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db51f87e79820c2b2396793cf1b83e81e68ee0afad5f04f979211715ea2194b3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 16:30:32 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 11 May 2022 16:30:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 11 May 2022 16:30:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 11 May 2022 16:31:21 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 16:32:58 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 16:32:59 GMT
EXPOSE 4222 8222
# Wed, 11 May 2022 16:33:00 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 May 2022 16:33:00 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414182f3892da8f7d095665f62200d67f6f8d2e246b130708b2b88a21687c3b`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164dca4c618438c46a2dc1963e12b45c2f8d43eef1d1fe7fae7e1c8c4e05ff0`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e40e75ccc6601c1be113a440f55f08afdecc037cdac48a489fdb828a760e8a8`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c46d136ed5db00b4518191e335ea48c04342ffbc2c41da9beeabc326232cb0d`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 482.5 KB (482509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9183e4d25dff6451cdfedc68317c4dd57922535f5d6aa35c5fb21dac3734fef`  
		Last Modified: Wed, 11 May 2022 16:33:50 GMT  
		Size: 7.6 MB (7607166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bec91034c767639b4ccbb6a280e45a12dd83565d0f24400b5bb5a291c40cb7`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea7dc716bc45aacd9709e081731dbf3715f48204651675a9177cafd8253f5dd`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6b5bf987b96cb6c0b09277a5ba367b7ce2f6c83dd0412319b03eb875d90030`  
		Last Modified: Wed, 11 May 2022 16:33:48 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
