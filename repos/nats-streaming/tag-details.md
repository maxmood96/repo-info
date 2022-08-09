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
$ docker pull nats-streaming@sha256:4a984df29db7ee2ada2a793b91fbea63c6fd2281268a7eb113ce731a6343d36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3165; amd64

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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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

### `nats-streaming:0.24` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine`

```console
$ docker pull nats-streaming@sha256:44ba3be0872d529c11ef538d333e721c8577d0b912f9235ce4129c85ac89b4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:2a4a4663b66920393b0422d0b34ad5b3f219374f51ca9af6e33d3bf8dad24a16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdc5fe5f8ac50f5726084676fd97c1202bf05aa26dce1f70d9bf321005401c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:57:37 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:57:39 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:57:39 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:57:39 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa7a43f0a6e9263ec9b5eba88db4161dde3d7df72468bb02151f72f504f3934`  
		Last Modified: Tue, 09 Aug 2022 20:58:13 GMT  
		Size: 7.5 MB (7453376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a7bc01ec03acbd02ca4881865115087ac6c4888d3c8f8f1b80b20acd717b84`  
		Last Modified: Tue, 09 Aug 2022 20:58:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7777dd6b8f4a35ec5ab53cb65cb2dfeb5911f445bdc9f8bf92d783f17da6e6b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b33da3667d27728acc8cca4d0a4129a1f7bbdbf9c0accfdbb53621aff4c11b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:26:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 19:26:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 19:26:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 19:26:15 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:26:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61200a93432f8e3ae1658c3206beb5181e790ea07cbb6ffa4b954148280848c`  
		Last Modified: Tue, 09 Aug 2022 19:27:13 GMT  
		Size: 7.0 MB (6959339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8c46256f1ee7c5447ba7b5af470c1a68074aa2f9ab145669e85fe98593a07`  
		Last Modified: Tue, 09 Aug 2022 19:27:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ef83df35aec12b230a70b2f60196a1d1219e041418ddd2866f7d47e1b940e175
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9384562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb36a93f30a5d146c0364e16c35ec655617228a3b3e6b01a4c99ee0b7b9240a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 22:38:59 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 22:39:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 22:39:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 22:39:03 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 22:39:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863d9dcc7331217c9c5456f249b11f6d7ebafff3e4ef9f81683f95b8a26dadfc`  
		Last Modified: Tue, 09 Aug 2022 22:40:13 GMT  
		Size: 6.9 MB (6949050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb422d8b731308bb36996f1224ae36b4ca3ed283afca3798822da5b2e75d294`  
		Last Modified: Tue, 09 Aug 2022 22:40:11 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:21295d7e34e88aea3514e03f9face7c12b46904f3768681bf0ab304bf117e0af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9586396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078e1384f4d13216989155dc9711d92b7b042bdec8af15735a2adfc691e82355`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:54:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:54:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:54:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:54:16 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:54:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:54:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb747aea2649d48e41c4c4281e4a6e4e98099c290c6cce1dae84380c9e64ca`  
		Last Modified: Tue, 09 Aug 2022 20:55:06 GMT  
		Size: 6.9 MB (6867537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994854509ba2d9847b7bb814dc14bccaf00350240e5a74232ede55ea08d65446`  
		Last Modified: Tue, 09 Aug 2022 20:55:05 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-alpine3.15`

```console
$ docker pull nats-streaming@sha256:44ba3be0872d529c11ef538d333e721c8577d0b912f9235ce4129c85ac89b4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:2a4a4663b66920393b0422d0b34ad5b3f219374f51ca9af6e33d3bf8dad24a16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdc5fe5f8ac50f5726084676fd97c1202bf05aa26dce1f70d9bf321005401c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:57:37 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:57:39 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:57:39 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:57:39 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa7a43f0a6e9263ec9b5eba88db4161dde3d7df72468bb02151f72f504f3934`  
		Last Modified: Tue, 09 Aug 2022 20:58:13 GMT  
		Size: 7.5 MB (7453376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a7bc01ec03acbd02ca4881865115087ac6c4888d3c8f8f1b80b20acd717b84`  
		Last Modified: Tue, 09 Aug 2022 20:58:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7777dd6b8f4a35ec5ab53cb65cb2dfeb5911f445bdc9f8bf92d783f17da6e6b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b33da3667d27728acc8cca4d0a4129a1f7bbdbf9c0accfdbb53621aff4c11b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:26:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 19:26:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 19:26:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 19:26:15 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:26:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61200a93432f8e3ae1658c3206beb5181e790ea07cbb6ffa4b954148280848c`  
		Last Modified: Tue, 09 Aug 2022 19:27:13 GMT  
		Size: 7.0 MB (6959339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8c46256f1ee7c5447ba7b5af470c1a68074aa2f9ab145669e85fe98593a07`  
		Last Modified: Tue, 09 Aug 2022 19:27:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ef83df35aec12b230a70b2f60196a1d1219e041418ddd2866f7d47e1b940e175
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9384562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb36a93f30a5d146c0364e16c35ec655617228a3b3e6b01a4c99ee0b7b9240a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 22:38:59 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 22:39:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 22:39:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 22:39:03 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 22:39:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863d9dcc7331217c9c5456f249b11f6d7ebafff3e4ef9f81683f95b8a26dadfc`  
		Last Modified: Tue, 09 Aug 2022 22:40:13 GMT  
		Size: 6.9 MB (6949050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb422d8b731308bb36996f1224ae36b4ca3ed283afca3798822da5b2e75d294`  
		Last Modified: Tue, 09 Aug 2022 22:40:11 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:21295d7e34e88aea3514e03f9face7c12b46904f3768681bf0ab304bf117e0af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9586396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078e1384f4d13216989155dc9711d92b7b042bdec8af15735a2adfc691e82355`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:54:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:54:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:54:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:54:16 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:54:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:54:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb747aea2649d48e41c4c4281e4a6e4e98099c290c6cce1dae84380c9e64ca`  
		Last Modified: Tue, 09 Aug 2022 20:55:06 GMT  
		Size: 6.9 MB (6867537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994854509ba2d9847b7bb814dc14bccaf00350240e5a74232ede55ea08d65446`  
		Last Modified: Tue, 09 Aug 2022 20:55:05 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-linux`

```console
$ docker pull nats-streaming@sha256:d22051826b6f0adb5ab36dd2380fd2ed2d3c02bc2ec6bb13a246230f099d4088
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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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
$ docker pull nats-streaming@sha256:7f761af192f68a1028e85ab7ff781de3110f737beec3ac75119a1835eefec479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:7f761af192f68a1028e85ab7ff781de3110f737beec3ac75119a1835eefec479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-scratch`

```console
$ docker pull nats-streaming@sha256:d22051826b6f0adb5ab36dd2380fd2ed2d3c02bc2ec6bb13a246230f099d4088
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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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
$ docker pull nats-streaming@sha256:72f37bd73f010013685254cf654505f3b5e5da9df7151b81a3001f4e428d3487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:54f05f43ce9903dcbaf8296407314aa0e256cb92f7d3507dae27c87e317926fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2680006267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74a5b6d2cab83f0f2823bdc860576c99e7df3bf5e28f48fa408a9a9ce021708`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Wed, 13 Jul 2022 12:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jul 2022 14:40:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:19:17 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 13 Jul 2022 16:19:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 13 Jul 2022 16:19:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 13 Jul 2022 16:20:20 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jul 2022 16:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jul 2022 16:22:09 GMT
EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:49b5d162039eae4fe1f7d6cc0d4b3be061cabb5d1d89950262e1b010e7ed67bb`  
		Last Modified: Wed, 13 Jul 2022 14:16:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2b176476aa48539273d15d106f9687175e98ae9c9a718eb29874b4890126f`  
		Last Modified: Wed, 13 Jul 2022 14:43:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683a85502dc2fdd66898d1b9756637bcfd98752c9cf3552499c85f2076a70fe`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c219c9b35a367721aced7f976db1159367c7192326bb5739fbcd1527bc39f70`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4350b1b959d0271fc768d3476b9fff0a8b91a1c31cb7a27a5361fb77a4aaf4`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e84646183e053545c1d7b7f82163ac6826d50ab4d3358baa44c32c4549173b`  
		Last Modified: Wed, 13 Jul 2022 16:22:59 GMT  
		Size: 347.1 KB (347099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f36cbb6a58f785f640bb0783e6f8c7c77627cbcba03578178cc8aeee16b8e0`  
		Last Modified: Wed, 13 Jul 2022 16:23:00 GMT  
		Size: 7.6 MB (7604049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a7ac8dd253366436ce20f266a16b34772de8df759827191e7d5b9cab22e85`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe10489c4dd14519aa909e4f118518a84995db60495ce027bfdfe4bbdc015f`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7dca8bc0acc5d41382d40a11b3e5b566a569388edbb4a1e15c9f8ab9ab1da`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:72f37bd73f010013685254cf654505f3b5e5da9df7151b81a3001f4e428d3487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:54f05f43ce9903dcbaf8296407314aa0e256cb92f7d3507dae27c87e317926fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2680006267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74a5b6d2cab83f0f2823bdc860576c99e7df3bf5e28f48fa408a9a9ce021708`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Wed, 13 Jul 2022 12:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jul 2022 14:40:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:19:17 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 13 Jul 2022 16:19:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 13 Jul 2022 16:19:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 13 Jul 2022 16:20:20 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jul 2022 16:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jul 2022 16:22:09 GMT
EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:49b5d162039eae4fe1f7d6cc0d4b3be061cabb5d1d89950262e1b010e7ed67bb`  
		Last Modified: Wed, 13 Jul 2022 14:16:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2b176476aa48539273d15d106f9687175e98ae9c9a718eb29874b4890126f`  
		Last Modified: Wed, 13 Jul 2022 14:43:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683a85502dc2fdd66898d1b9756637bcfd98752c9cf3552499c85f2076a70fe`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c219c9b35a367721aced7f976db1159367c7192326bb5739fbcd1527bc39f70`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4350b1b959d0271fc768d3476b9fff0a8b91a1c31cb7a27a5361fb77a4aaf4`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e84646183e053545c1d7b7f82163ac6826d50ab4d3358baa44c32c4549173b`  
		Last Modified: Wed, 13 Jul 2022 16:22:59 GMT  
		Size: 347.1 KB (347099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f36cbb6a58f785f640bb0783e6f8c7c77627cbcba03578178cc8aeee16b8e0`  
		Last Modified: Wed, 13 Jul 2022 16:23:00 GMT  
		Size: 7.6 MB (7604049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a7ac8dd253366436ce20f266a16b34772de8df759827191e7d5b9cab22e85`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe10489c4dd14519aa909e4f118518a84995db60495ce027bfdfe4bbdc015f`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7dca8bc0acc5d41382d40a11b3e5b566a569388edbb4a1e15c9f8ab9ab1da`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6`

```console
$ docker pull nats-streaming@sha256:4a984df29db7ee2ada2a793b91fbea63c6fd2281268a7eb113ce731a6343d36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3165; amd64

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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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

### `nats-streaming:0.24.6` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-alpine`

```console
$ docker pull nats-streaming@sha256:44ba3be0872d529c11ef538d333e721c8577d0b912f9235ce4129c85ac89b4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.6-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:2a4a4663b66920393b0422d0b34ad5b3f219374f51ca9af6e33d3bf8dad24a16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdc5fe5f8ac50f5726084676fd97c1202bf05aa26dce1f70d9bf321005401c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:57:37 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:57:39 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:57:39 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:57:39 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa7a43f0a6e9263ec9b5eba88db4161dde3d7df72468bb02151f72f504f3934`  
		Last Modified: Tue, 09 Aug 2022 20:58:13 GMT  
		Size: 7.5 MB (7453376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a7bc01ec03acbd02ca4881865115087ac6c4888d3c8f8f1b80b20acd717b84`  
		Last Modified: Tue, 09 Aug 2022 20:58:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7777dd6b8f4a35ec5ab53cb65cb2dfeb5911f445bdc9f8bf92d783f17da6e6b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b33da3667d27728acc8cca4d0a4129a1f7bbdbf9c0accfdbb53621aff4c11b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:26:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 19:26:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 19:26:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 19:26:15 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:26:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61200a93432f8e3ae1658c3206beb5181e790ea07cbb6ffa4b954148280848c`  
		Last Modified: Tue, 09 Aug 2022 19:27:13 GMT  
		Size: 7.0 MB (6959339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8c46256f1ee7c5447ba7b5af470c1a68074aa2f9ab145669e85fe98593a07`  
		Last Modified: Tue, 09 Aug 2022 19:27:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ef83df35aec12b230a70b2f60196a1d1219e041418ddd2866f7d47e1b940e175
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9384562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb36a93f30a5d146c0364e16c35ec655617228a3b3e6b01a4c99ee0b7b9240a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 22:38:59 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 22:39:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 22:39:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 22:39:03 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 22:39:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863d9dcc7331217c9c5456f249b11f6d7ebafff3e4ef9f81683f95b8a26dadfc`  
		Last Modified: Tue, 09 Aug 2022 22:40:13 GMT  
		Size: 6.9 MB (6949050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb422d8b731308bb36996f1224ae36b4ca3ed283afca3798822da5b2e75d294`  
		Last Modified: Tue, 09 Aug 2022 22:40:11 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:21295d7e34e88aea3514e03f9face7c12b46904f3768681bf0ab304bf117e0af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9586396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078e1384f4d13216989155dc9711d92b7b042bdec8af15735a2adfc691e82355`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:54:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:54:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:54:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:54:16 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:54:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:54:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb747aea2649d48e41c4c4281e4a6e4e98099c290c6cce1dae84380c9e64ca`  
		Last Modified: Tue, 09 Aug 2022 20:55:06 GMT  
		Size: 6.9 MB (6867537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994854509ba2d9847b7bb814dc14bccaf00350240e5a74232ede55ea08d65446`  
		Last Modified: Tue, 09 Aug 2022 20:55:05 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-alpine3.15`

```console
$ docker pull nats-streaming@sha256:44ba3be0872d529c11ef538d333e721c8577d0b912f9235ce4129c85ac89b4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.24.6-alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:2a4a4663b66920393b0422d0b34ad5b3f219374f51ca9af6e33d3bf8dad24a16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdc5fe5f8ac50f5726084676fd97c1202bf05aa26dce1f70d9bf321005401c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:57:37 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:57:39 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:57:39 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:57:39 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa7a43f0a6e9263ec9b5eba88db4161dde3d7df72468bb02151f72f504f3934`  
		Last Modified: Tue, 09 Aug 2022 20:58:13 GMT  
		Size: 7.5 MB (7453376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a7bc01ec03acbd02ca4881865115087ac6c4888d3c8f8f1b80b20acd717b84`  
		Last Modified: Tue, 09 Aug 2022 20:58:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7777dd6b8f4a35ec5ab53cb65cb2dfeb5911f445bdc9f8bf92d783f17da6e6b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b33da3667d27728acc8cca4d0a4129a1f7bbdbf9c0accfdbb53621aff4c11b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:26:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 19:26:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 19:26:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 19:26:15 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:26:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61200a93432f8e3ae1658c3206beb5181e790ea07cbb6ffa4b954148280848c`  
		Last Modified: Tue, 09 Aug 2022 19:27:13 GMT  
		Size: 7.0 MB (6959339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8c46256f1ee7c5447ba7b5af470c1a68074aa2f9ab145669e85fe98593a07`  
		Last Modified: Tue, 09 Aug 2022 19:27:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ef83df35aec12b230a70b2f60196a1d1219e041418ddd2866f7d47e1b940e175
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9384562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb36a93f30a5d146c0364e16c35ec655617228a3b3e6b01a4c99ee0b7b9240a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 22:38:59 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 22:39:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 22:39:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 22:39:03 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 22:39:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863d9dcc7331217c9c5456f249b11f6d7ebafff3e4ef9f81683f95b8a26dadfc`  
		Last Modified: Tue, 09 Aug 2022 22:40:13 GMT  
		Size: 6.9 MB (6949050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb422d8b731308bb36996f1224ae36b4ca3ed283afca3798822da5b2e75d294`  
		Last Modified: Tue, 09 Aug 2022 22:40:11 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:21295d7e34e88aea3514e03f9face7c12b46904f3768681bf0ab304bf117e0af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9586396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078e1384f4d13216989155dc9711d92b7b042bdec8af15735a2adfc691e82355`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:54:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:54:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:54:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:54:16 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:54:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:54:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb747aea2649d48e41c4c4281e4a6e4e98099c290c6cce1dae84380c9e64ca`  
		Last Modified: Tue, 09 Aug 2022 20:55:06 GMT  
		Size: 6.9 MB (6867537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994854509ba2d9847b7bb814dc14bccaf00350240e5a74232ede55ea08d65446`  
		Last Modified: Tue, 09 Aug 2022 20:55:05 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-linux`

```console
$ docker pull nats-streaming@sha256:d22051826b6f0adb5ab36dd2380fd2ed2d3c02bc2ec6bb13a246230f099d4088
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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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
$ docker pull nats-streaming@sha256:7f761af192f68a1028e85ab7ff781de3110f737beec3ac75119a1835eefec479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24.6-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:7f761af192f68a1028e85ab7ff781de3110f737beec3ac75119a1835eefec479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24.6-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-scratch`

```console
$ docker pull nats-streaming@sha256:d22051826b6f0adb5ab36dd2380fd2ed2d3c02bc2ec6bb13a246230f099d4088
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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.24.6-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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
$ docker pull nats-streaming@sha256:72f37bd73f010013685254cf654505f3b5e5da9df7151b81a3001f4e428d3487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24.6-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:54f05f43ce9903dcbaf8296407314aa0e256cb92f7d3507dae27c87e317926fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2680006267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74a5b6d2cab83f0f2823bdc860576c99e7df3bf5e28f48fa408a9a9ce021708`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Wed, 13 Jul 2022 12:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jul 2022 14:40:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:19:17 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 13 Jul 2022 16:19:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 13 Jul 2022 16:19:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 13 Jul 2022 16:20:20 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jul 2022 16:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jul 2022 16:22:09 GMT
EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:49b5d162039eae4fe1f7d6cc0d4b3be061cabb5d1d89950262e1b010e7ed67bb`  
		Last Modified: Wed, 13 Jul 2022 14:16:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2b176476aa48539273d15d106f9687175e98ae9c9a718eb29874b4890126f`  
		Last Modified: Wed, 13 Jul 2022 14:43:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683a85502dc2fdd66898d1b9756637bcfd98752c9cf3552499c85f2076a70fe`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c219c9b35a367721aced7f976db1159367c7192326bb5739fbcd1527bc39f70`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4350b1b959d0271fc768d3476b9fff0a8b91a1c31cb7a27a5361fb77a4aaf4`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e84646183e053545c1d7b7f82163ac6826d50ab4d3358baa44c32c4549173b`  
		Last Modified: Wed, 13 Jul 2022 16:22:59 GMT  
		Size: 347.1 KB (347099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f36cbb6a58f785f640bb0783e6f8c7c77627cbcba03578178cc8aeee16b8e0`  
		Last Modified: Wed, 13 Jul 2022 16:23:00 GMT  
		Size: 7.6 MB (7604049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a7ac8dd253366436ce20f266a16b34772de8df759827191e7d5b9cab22e85`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe10489c4dd14519aa909e4f118518a84995db60495ce027bfdfe4bbdc015f`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7dca8bc0acc5d41382d40a11b3e5b566a569388edbb4a1e15c9f8ab9ab1da`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.24.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:72f37bd73f010013685254cf654505f3b5e5da9df7151b81a3001f4e428d3487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:0.24.6-windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:54f05f43ce9903dcbaf8296407314aa0e256cb92f7d3507dae27c87e317926fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2680006267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74a5b6d2cab83f0f2823bdc860576c99e7df3bf5e28f48fa408a9a9ce021708`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Wed, 13 Jul 2022 12:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jul 2022 14:40:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:19:17 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 13 Jul 2022 16:19:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 13 Jul 2022 16:19:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 13 Jul 2022 16:20:20 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jul 2022 16:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jul 2022 16:22:09 GMT
EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:49b5d162039eae4fe1f7d6cc0d4b3be061cabb5d1d89950262e1b010e7ed67bb`  
		Last Modified: Wed, 13 Jul 2022 14:16:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2b176476aa48539273d15d106f9687175e98ae9c9a718eb29874b4890126f`  
		Last Modified: Wed, 13 Jul 2022 14:43:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683a85502dc2fdd66898d1b9756637bcfd98752c9cf3552499c85f2076a70fe`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c219c9b35a367721aced7f976db1159367c7192326bb5739fbcd1527bc39f70`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4350b1b959d0271fc768d3476b9fff0a8b91a1c31cb7a27a5361fb77a4aaf4`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e84646183e053545c1d7b7f82163ac6826d50ab4d3358baa44c32c4549173b`  
		Last Modified: Wed, 13 Jul 2022 16:22:59 GMT  
		Size: 347.1 KB (347099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f36cbb6a58f785f640bb0783e6f8c7c77627cbcba03578178cc8aeee16b8e0`  
		Last Modified: Wed, 13 Jul 2022 16:23:00 GMT  
		Size: 7.6 MB (7604049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a7ac8dd253366436ce20f266a16b34772de8df759827191e7d5b9cab22e85`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe10489c4dd14519aa909e4f118518a84995db60495ce027bfdfe4bbdc015f`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7dca8bc0acc5d41382d40a11b3e5b566a569388edbb4a1e15c9f8ab9ab1da`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:44ba3be0872d529c11ef538d333e721c8577d0b912f9235ce4129c85ac89b4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:2a4a4663b66920393b0422d0b34ad5b3f219374f51ca9af6e33d3bf8dad24a16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdc5fe5f8ac50f5726084676fd97c1202bf05aa26dce1f70d9bf321005401c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:57:37 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:57:39 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:57:39 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:57:39 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa7a43f0a6e9263ec9b5eba88db4161dde3d7df72468bb02151f72f504f3934`  
		Last Modified: Tue, 09 Aug 2022 20:58:13 GMT  
		Size: 7.5 MB (7453376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a7bc01ec03acbd02ca4881865115087ac6c4888d3c8f8f1b80b20acd717b84`  
		Last Modified: Tue, 09 Aug 2022 20:58:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7777dd6b8f4a35ec5ab53cb65cb2dfeb5911f445bdc9f8bf92d783f17da6e6b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b33da3667d27728acc8cca4d0a4129a1f7bbdbf9c0accfdbb53621aff4c11b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:26:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 19:26:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 19:26:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 19:26:15 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:26:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61200a93432f8e3ae1658c3206beb5181e790ea07cbb6ffa4b954148280848c`  
		Last Modified: Tue, 09 Aug 2022 19:27:13 GMT  
		Size: 7.0 MB (6959339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8c46256f1ee7c5447ba7b5af470c1a68074aa2f9ab145669e85fe98593a07`  
		Last Modified: Tue, 09 Aug 2022 19:27:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ef83df35aec12b230a70b2f60196a1d1219e041418ddd2866f7d47e1b940e175
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9384562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb36a93f30a5d146c0364e16c35ec655617228a3b3e6b01a4c99ee0b7b9240a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 22:38:59 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 22:39:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 22:39:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 22:39:03 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 22:39:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863d9dcc7331217c9c5456f249b11f6d7ebafff3e4ef9f81683f95b8a26dadfc`  
		Last Modified: Tue, 09 Aug 2022 22:40:13 GMT  
		Size: 6.9 MB (6949050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb422d8b731308bb36996f1224ae36b4ca3ed283afca3798822da5b2e75d294`  
		Last Modified: Tue, 09 Aug 2022 22:40:11 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:21295d7e34e88aea3514e03f9face7c12b46904f3768681bf0ab304bf117e0af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9586396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078e1384f4d13216989155dc9711d92b7b042bdec8af15735a2adfc691e82355`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:54:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:54:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:54:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:54:16 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:54:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:54:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb747aea2649d48e41c4c4281e4a6e4e98099c290c6cce1dae84380c9e64ca`  
		Last Modified: Tue, 09 Aug 2022 20:55:06 GMT  
		Size: 6.9 MB (6867537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994854509ba2d9847b7bb814dc14bccaf00350240e5a74232ede55ea08d65446`  
		Last Modified: Tue, 09 Aug 2022 20:55:05 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.15`

```console
$ docker pull nats-streaming@sha256:44ba3be0872d529c11ef538d333e721c8577d0b912f9235ce4129c85ac89b4c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.15` - linux; amd64

```console
$ docker pull nats-streaming@sha256:2a4a4663b66920393b0422d0b34ad5b3f219374f51ca9af6e33d3bf8dad24a16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10277308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdc5fe5f8ac50f5726084676fd97c1202bf05aa26dce1f70d9bf321005401c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:57:37 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:57:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:57:39 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:57:39 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:57:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:57:39 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa7a43f0a6e9263ec9b5eba88db4161dde3d7df72468bb02151f72f504f3934`  
		Last Modified: Tue, 09 Aug 2022 20:58:13 GMT  
		Size: 7.5 MB (7453376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a7bc01ec03acbd02ca4881865115087ac6c4888d3c8f8f1b80b20acd717b84`  
		Last Modified: Tue, 09 Aug 2022 20:58:07 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7777dd6b8f4a35ec5ab53cb65cb2dfeb5911f445bdc9f8bf92d783f17da6e6b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9590887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b33da3667d27728acc8cca4d0a4129a1f7bbdbf9c0accfdbb53621aff4c11b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 19:26:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 19:26:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 19:26:15 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 19:26:15 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 19:26:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61200a93432f8e3ae1658c3206beb5181e790ea07cbb6ffa4b954148280848c`  
		Last Modified: Tue, 09 Aug 2022 19:27:13 GMT  
		Size: 7.0 MB (6959339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8c46256f1ee7c5447ba7b5af470c1a68074aa2f9ab145669e85fe98593a07`  
		Last Modified: Tue, 09 Aug 2022 19:27:12 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:ef83df35aec12b230a70b2f60196a1d1219e041418ddd2866f7d47e1b940e175
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9384562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb36a93f30a5d146c0364e16c35ec655617228a3b3e6b01a4c99ee0b7b9240a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:52 GMT
ADD file:0bd18306f21937a9572e68c768f05f4a9d8341b40c2379a7bfcb857c77734a14 in / 
# Tue, 09 Aug 2022 16:57:52 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 22:38:59 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 22:39:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 22:39:03 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 22:39:03 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 22:39:04 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:59775c20a906b1a49edcdc41a700a795998979d6ecf8f8d9cd7cbdf45e686d81`  
		Last Modified: Tue, 09 Aug 2022 16:59:12 GMT  
		Size: 2.4 MB (2435092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863d9dcc7331217c9c5456f249b11f6d7ebafff3e4ef9f81683f95b8a26dadfc`  
		Last Modified: Tue, 09 Aug 2022 22:40:13 GMT  
		Size: 6.9 MB (6949050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb422d8b731308bb36996f1224ae36b4ca3ed283afca3798822da5b2e75d294`  
		Last Modified: Tue, 09 Aug 2022 22:40:11 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:21295d7e34e88aea3514e03f9face7c12b46904f3768681bf0ab304bf117e0af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9586396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078e1384f4d13216989155dc9711d92b7b042bdec8af15735a2adfc691e82355`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:54:13 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Tue, 09 Aug 2022 20:54:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='efe2e10fa2159a9c97ae39b92409bed61c168d571a7a447d6a9299a3e8451194' ;; 		armhf) natsArch='arm6'; sha256='caf1c4fa5f3d460b11a7206fb6efadf6b00db5bf764e89c964f7faeb64d5093e' ;; 		armv7) natsArch='arm7'; sha256='f2d511979cbb2013c6f880e68fc6d3b1efde376851caa4575a0477cc084acf2f' ;; 		x86_64) natsArch='amd64'; sha256='726b22ead027d6a9a1de24015445d6a130d91f29faa7fafebd53dcb73aa7a667' ;; 		x86) natsArch='386'; sha256='df0309db02699697b87f28583e1762f7b837b4acca0a2dde805d67ff51b81baf' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Tue, 09 Aug 2022 20:54:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Tue, 09 Aug 2022 20:54:16 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 20:54:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 20:54:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bb747aea2649d48e41c4c4281e4a6e4e98099c290c6cce1dae84380c9e64ca`  
		Last Modified: Tue, 09 Aug 2022 20:55:06 GMT  
		Size: 6.9 MB (6867537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994854509ba2d9847b7bb814dc14bccaf00350240e5a74232ede55ea08d65446`  
		Last Modified: Tue, 09 Aug 2022 20:55:05 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:4a984df29db7ee2ada2a793b91fbea63c6fd2281268a7eb113ce731a6343d36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.3165; amd64

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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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

### `nats-streaming:latest` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:d22051826b6f0adb5ab36dd2380fd2ed2d3c02bc2ec6bb13a246230f099d4088
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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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
$ docker pull nats-streaming@sha256:7f761af192f68a1028e85ab7ff781de3110f737beec3ac75119a1835eefec479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:7f761af192f68a1028e85ab7ff781de3110f737beec3ac75119a1835eefec479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:7a5e856a2abfeee32a2cf0b91ef052dcfcb47acfbb367336a8d7eabf8429108d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110435538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0907821c7fe38dd21bcd6e588fe0871c40ab5e3a848ae14c54226f7417de183a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:43:20 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:22:31 GMT
RUN cmd /S /C #(nop) COPY file:49c1adc21bf08da66368295e2745e859ae25816630df6bbe041852e77bf31e1a in C:\nats-streaming-server.exe 
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:32 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:33 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:426914f8f9a4bf93afd51c902139b25ee4faa60707c7fe5f889f66f8f73c9078`  
		Last Modified: Wed, 13 Jul 2022 14:44:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e83e56899997aa39b01c426f2bcc05e956238b3d20e1a949a15fbdc39883a7b`  
		Last Modified: Wed, 13 Jul 2022 16:23:16 GMT  
		Size: 7.3 MB (7275885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092d8c6f78734ab3125d90ff8ca0d137bc2758dad02e8c6840516c5dad89174`  
		Last Modified: Wed, 13 Jul 2022 16:23:15 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c1dcb048d103681194460743471df8b142889dc63f8d8073b32b3e61d5d412`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b701c70f70fe8219411d0e072ccf5ae9668e0de9d90e7518629fbb8621e8958`  
		Last Modified: Wed, 13 Jul 2022 16:23:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:d22051826b6f0adb5ab36dd2380fd2ed2d3c02bc2ec6bb13a246230f099d4088
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
$ docker pull nats-streaming@sha256:01b1e6b1844269a3244839a7e783f5636257112bc4ea31ec292c30a867d48ae2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70144c73cb5394e4554f992f11ed714cad02f59e927edcd1f397ff78050b3e8f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 19:26:26 GMT
COPY file:e97502b8a5ae65f8937a0a1aeb1aa614b9bb861a96043a968de2c0cf17a937f1 in /nats-streaming-server 
# Tue, 09 Aug 2022 19:26:26 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 19:26:26 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 19:26:26 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:16c6d893da0b39837328c8e6679a442b2c4e6ab4980d2335b231e7212f997740`  
		Last Modified: Thu, 05 May 2022 00:52:04 GMT  
		Size: 6.7 MB (6671918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:685f06e91d8dd756ef96594ac3652fae96a0dafb3b7d3d29bb28714615dbc23c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b43a1af2b7f86dd2a1fd67805d1826d67edc1e5fac64381e8b7415410c0930c`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 09 Aug 2022 22:39:19 GMT
COPY file:5aa2d0e9a52771b5ee1128b0476967aca957bc49665dfa220f9fada895777349 in /nats-streaming-server 
# Tue, 09 Aug 2022 22:39:20 GMT
EXPOSE 4222 8222
# Tue, 09 Aug 2022 22:39:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Tue, 09 Aug 2022 22:39:20 GMT
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
$ docker pull nats-streaming@sha256:72f37bd73f010013685254cf654505f3b5e5da9df7151b81a3001f4e428d3487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:54f05f43ce9903dcbaf8296407314aa0e256cb92f7d3507dae27c87e317926fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2680006267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74a5b6d2cab83f0f2823bdc860576c99e7df3bf5e28f48fa408a9a9ce021708`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Wed, 13 Jul 2022 12:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jul 2022 14:40:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:19:17 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 13 Jul 2022 16:19:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 13 Jul 2022 16:19:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 13 Jul 2022 16:20:20 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jul 2022 16:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jul 2022 16:22:09 GMT
EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:49b5d162039eae4fe1f7d6cc0d4b3be061cabb5d1d89950262e1b010e7ed67bb`  
		Last Modified: Wed, 13 Jul 2022 14:16:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2b176476aa48539273d15d106f9687175e98ae9c9a718eb29874b4890126f`  
		Last Modified: Wed, 13 Jul 2022 14:43:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683a85502dc2fdd66898d1b9756637bcfd98752c9cf3552499c85f2076a70fe`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c219c9b35a367721aced7f976db1159367c7192326bb5739fbcd1527bc39f70`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4350b1b959d0271fc768d3476b9fff0a8b91a1c31cb7a27a5361fb77a4aaf4`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e84646183e053545c1d7b7f82163ac6826d50ab4d3358baa44c32c4549173b`  
		Last Modified: Wed, 13 Jul 2022 16:22:59 GMT  
		Size: 347.1 KB (347099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f36cbb6a58f785f640bb0783e6f8c7c77627cbcba03578178cc8aeee16b8e0`  
		Last Modified: Wed, 13 Jul 2022 16:23:00 GMT  
		Size: 7.6 MB (7604049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a7ac8dd253366436ce20f266a16b34772de8df759827191e7d5b9cab22e85`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe10489c4dd14519aa909e4f118518a84995db60495ce027bfdfe4bbdc015f`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7dca8bc0acc5d41382d40a11b3e5b566a569388edbb4a1e15c9f8ab9ab1da`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:72f37bd73f010013685254cf654505f3b5e5da9df7151b81a3001f4e428d3487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull nats-streaming@sha256:54f05f43ce9903dcbaf8296407314aa0e256cb92f7d3507dae27c87e317926fd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2680006267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74a5b6d2cab83f0f2823bdc860576c99e7df3bf5e28f48fa408a9a9ce021708`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Wed, 13 Jul 2022 12:49:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Jul 2022 14:40:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Jul 2022 16:19:17 GMT
ENV NATS_STREAMING_SERVER=0.24.6
# Wed, 13 Jul 2022 16:19:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.24.6/nats-streaming-server-v0.24.6-windows-amd64.zip
# Wed, 13 Jul 2022 16:19:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=86e1e573706b41a109baf84e93d00cfa7e3f4e47d59068bda18e972a7d3768f4
# Wed, 13 Jul 2022 16:20:20 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Jul 2022 16:22:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Jul 2022 16:22:09 GMT
EXPOSE 4222 8222
# Wed, 13 Jul 2022 16:22:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Jul 2022 16:22:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:49b5d162039eae4fe1f7d6cc0d4b3be061cabb5d1d89950262e1b010e7ed67bb`  
		Last Modified: Wed, 13 Jul 2022 14:16:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a2b176476aa48539273d15d106f9687175e98ae9c9a718eb29874b4890126f`  
		Last Modified: Wed, 13 Jul 2022 14:43:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683a85502dc2fdd66898d1b9756637bcfd98752c9cf3552499c85f2076a70fe`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c219c9b35a367721aced7f976db1159367c7192326bb5739fbcd1527bc39f70`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4350b1b959d0271fc768d3476b9fff0a8b91a1c31cb7a27a5361fb77a4aaf4`  
		Last Modified: Wed, 13 Jul 2022 16:23:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e84646183e053545c1d7b7f82163ac6826d50ab4d3358baa44c32c4549173b`  
		Last Modified: Wed, 13 Jul 2022 16:22:59 GMT  
		Size: 347.1 KB (347099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f36cbb6a58f785f640bb0783e6f8c7c77627cbcba03578178cc8aeee16b8e0`  
		Last Modified: Wed, 13 Jul 2022 16:23:00 GMT  
		Size: 7.6 MB (7604049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4a7ac8dd253366436ce20f266a16b34772de8df759827191e7d5b9cab22e85`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbe10489c4dd14519aa909e4f118518a84995db60495ce027bfdfe4bbdc015f`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b7dca8bc0acc5d41382d40a11b3e5b566a569388edbb4a1e15c9f8ab9ab1da`  
		Last Modified: Wed, 13 Jul 2022 16:22:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
