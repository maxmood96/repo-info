<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats-streaming`

-	[`nats-streaming:0.25`](#nats-streaming025)
-	[`nats-streaming:0.25-alpine`](#nats-streaming025-alpine)
-	[`nats-streaming:0.25-alpine3.18`](#nats-streaming025-alpine318)
-	[`nats-streaming:0.25-linux`](#nats-streaming025-linux)
-	[`nats-streaming:0.25-nanoserver`](#nats-streaming025-nanoserver)
-	[`nats-streaming:0.25-nanoserver-1809`](#nats-streaming025-nanoserver-1809)
-	[`nats-streaming:0.25-scratch`](#nats-streaming025-scratch)
-	[`nats-streaming:0.25-windowsservercore`](#nats-streaming025-windowsservercore)
-	[`nats-streaming:0.25-windowsservercore-1809`](#nats-streaming025-windowsservercore-1809)
-	[`nats-streaming:0.25.6`](#nats-streaming0256)
-	[`nats-streaming:0.25.6-alpine`](#nats-streaming0256-alpine)
-	[`nats-streaming:0.25.6-alpine3.18`](#nats-streaming0256-alpine318)
-	[`nats-streaming:0.25.6-linux`](#nats-streaming0256-linux)
-	[`nats-streaming:0.25.6-nanoserver`](#nats-streaming0256-nanoserver)
-	[`nats-streaming:0.25.6-nanoserver-1809`](#nats-streaming0256-nanoserver-1809)
-	[`nats-streaming:0.25.6-scratch`](#nats-streaming0256-scratch)
-	[`nats-streaming:0.25.6-windowsservercore`](#nats-streaming0256-windowsservercore)
-	[`nats-streaming:0.25.6-windowsservercore-1809`](#nats-streaming0256-windowsservercore-1809)
-	[`nats-streaming:alpine`](#nats-streamingalpine)
-	[`nats-streaming:alpine3.18`](#nats-streamingalpine318)
-	[`nats-streaming:latest`](#nats-streaminglatest)
-	[`nats-streaming:linux`](#nats-streaminglinux)
-	[`nats-streaming:nanoserver`](#nats-streamingnanoserver)
-	[`nats-streaming:nanoserver-1809`](#nats-streamingnanoserver-1809)
-	[`nats-streaming:scratch`](#nats-streamingscratch)
-	[`nats-streaming:windowsservercore`](#nats-streamingwindowsservercore)
-	[`nats-streaming:windowsservercore-1809`](#nats-streamingwindowsservercore-1809)

## `nats-streaming:0.25`

```console
$ docker pull nats-streaming@sha256:d3175589326bc542cdc97ec4900237e1b603492994037e2e0451fb86de40bfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:6e851c855d73cd1b5a82d7f97902276f92db9e4292ea494393c04a7ab5c5c8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d30fe82631f494b987479925af667ef45d90aa558e9382b0562de1dbc4506fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0967b77103d36801616352e9dd5095d2643efddea33ae3f17decaa4173b9aad2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:44:21 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 05:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 05:44:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 05:44:24 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 05:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 05:44:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051f87cffccdf4fbe1a90776658618b57180fce176ee9bb3cbd3395d9e4d253e`  
		Last Modified: Sat, 27 Jan 2024 05:44:44 GMT  
		Size: 8.1 MB (8065442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72378ed20c9f3302bcc39fa44b53028f820d640b981b48e8925bee35901cc573`  
		Last Modified: Sat, 27 Jan 2024 05:44:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3515d0b22fc24e6326557eeef983b71e0e79ef01de7248a31fdbda1076505315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01ac66f4ad49a362e865ff0cd64fbc6fe3bd5285801196dad2c7e6e9c28186`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:17:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:17:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:17:16 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:17:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:17:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc1417e242952eafa8945163bc8dc5655660d53b1c181774b3b3f0d3a57a3c`  
		Last Modified: Sat, 27 Jan 2024 00:17:44 GMT  
		Size: 7.7 MB (7683865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8f9dd70bb23d2f71b6d3a42d2a76e949167a79dfcb206e70b3961b11537b1`  
		Last Modified: Sat, 27 Jan 2024 00:17:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:e957f1f8c676db64ee3c5ccab427b465710b07dc68554c2b89ecb0c8f3f7733d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46650abce4a7529ca6e7e2c5c2d61f94c79943a4650cc6082d3eb273d511ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:17:58 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 01:18:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 01:18:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 01:18:01 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 01:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:18:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175d2f4269d43d5998f2114d4ea5cbc4d046ba44b79505566c01af45bdf4a27`  
		Last Modified: Sat, 27 Jan 2024 01:18:22 GMT  
		Size: 7.7 MB (7677345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718bd229c3a1354a4e359597856845aa6686c2b03fe8e1cecd7a213a4bccc22`  
		Last Modified: Sat, 27 Jan 2024 01:18:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:e472e8705b1475861a000cf1843db95825cb1d77e726269f0b7dca6fef430ada
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd63828fd18149ac4313c4214e50bf58ac6ebb0b46dbc91eda8032ab4c7a41b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:44:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:44:51 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:44:52 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:44:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e25adb5e1d79a1d0925d45e9c915e8e04b5be9669f15d99b87b65dbdac359`  
		Last Modified: Sat, 27 Jan 2024 00:45:09 GMT  
		Size: 7.4 MB (7384196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe3b347142aa6e063c7bad5378f82312940c683faa69b36527f66fa7267e97`  
		Last Modified: Sat, 27 Jan 2024 00:45:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.18`

```console
$ docker pull nats-streaming@sha256:6e851c855d73cd1b5a82d7f97902276f92db9e4292ea494393c04a7ab5c5c8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d30fe82631f494b987479925af667ef45d90aa558e9382b0562de1dbc4506fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0967b77103d36801616352e9dd5095d2643efddea33ae3f17decaa4173b9aad2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:44:21 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 05:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 05:44:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 05:44:24 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 05:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 05:44:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051f87cffccdf4fbe1a90776658618b57180fce176ee9bb3cbd3395d9e4d253e`  
		Last Modified: Sat, 27 Jan 2024 05:44:44 GMT  
		Size: 8.1 MB (8065442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72378ed20c9f3302bcc39fa44b53028f820d640b981b48e8925bee35901cc573`  
		Last Modified: Sat, 27 Jan 2024 05:44:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3515d0b22fc24e6326557eeef983b71e0e79ef01de7248a31fdbda1076505315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01ac66f4ad49a362e865ff0cd64fbc6fe3bd5285801196dad2c7e6e9c28186`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:17:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:17:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:17:16 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:17:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:17:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc1417e242952eafa8945163bc8dc5655660d53b1c181774b3b3f0d3a57a3c`  
		Last Modified: Sat, 27 Jan 2024 00:17:44 GMT  
		Size: 7.7 MB (7683865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8f9dd70bb23d2f71b6d3a42d2a76e949167a79dfcb206e70b3961b11537b1`  
		Last Modified: Sat, 27 Jan 2024 00:17:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:e957f1f8c676db64ee3c5ccab427b465710b07dc68554c2b89ecb0c8f3f7733d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46650abce4a7529ca6e7e2c5c2d61f94c79943a4650cc6082d3eb273d511ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:17:58 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 01:18:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 01:18:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 01:18:01 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 01:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:18:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175d2f4269d43d5998f2114d4ea5cbc4d046ba44b79505566c01af45bdf4a27`  
		Last Modified: Sat, 27 Jan 2024 01:18:22 GMT  
		Size: 7.7 MB (7677345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718bd229c3a1354a4e359597856845aa6686c2b03fe8e1cecd7a213a4bccc22`  
		Last Modified: Sat, 27 Jan 2024 01:18:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:e472e8705b1475861a000cf1843db95825cb1d77e726269f0b7dca6fef430ada
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd63828fd18149ac4313c4214e50bf58ac6ebb0b46dbc91eda8032ab4c7a41b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:44:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:44:51 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:44:52 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:44:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e25adb5e1d79a1d0925d45e9c915e8e04b5be9669f15d99b87b65dbdac359`  
		Last Modified: Sat, 27 Jan 2024 00:45:09 GMT  
		Size: 7.4 MB (7384196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe3b347142aa6e063c7bad5378f82312940c683faa69b36527f66fa7267e97`  
		Last Modified: Sat, 27 Jan 2024 00:45:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-linux`

```console
$ docker pull nats-streaming@sha256:6cfbe46b8f764cd35a24db7ffe7ae9e0f748b4b040a0001e545e6660e2c742d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver`

```console
$ docker pull nats-streaming@sha256:0d3a445a8537b829d0ac495550172bc8bcbda974fed6fd3b410797582339a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:0d3a445a8537b829d0ac495550172bc8bcbda974fed6fd3b410797582339a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:6cfbe46b8f764cd35a24db7ffe7ae9e0f748b4b040a0001e545e6660e2c742d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore`

```console
$ docker pull nats-streaming@sha256:b5d4fe3f6ce89e3bcf22da05af606fd96758e494479efb60164c96fa902f6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:302e53126d9b9b2338ce8da329cba1b502614202b841d472aad239ea6df81ffd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089125234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc974b41ee9acf444c77c43307544e9974fdc65c67c07b138f2b1579da78178f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 14 Feb 2024 21:12:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 14 Feb 2024 21:13:54 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:15:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:15:50 GMT
EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:15:51 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:15:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b3259e00f84e65b0d749ecdb1c509cfaefbab41e8cb1f6543ed1330430502`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61718a6e18dbd65ddf3f59fa04789e1f9acaec2f5cf25ce8cb26a3dd44c3282a`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a5ffeba7098ea453e541f16fce989d9bf9443e53b4a7da19cb16428f4d786`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab53e0e6ef70ca249e6e56bdd06de3a5697dd6cd838002e9be78c4e619e93d`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 444.5 KB (444454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86bd8e6e200eb4bd3eff9524dd7128bfb365522a7df4a2171325010624067c`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 8.2 MB (8221053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992357c2fc0a12399ad77caf56b874e927614befdc2b3f238971b92a4134141f`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd057cca0f909355ef1eaa7ea42b060645a1ebe3af92ea98a4fd2c16dffb9be9`  
		Last Modified: Wed, 14 Feb 2024 21:16:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765553db67243ec6679030d92c818bc160158ea025ce173c15d19bcdb0f0baa`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b5d4fe3f6ce89e3bcf22da05af606fd96758e494479efb60164c96fa902f6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:302e53126d9b9b2338ce8da329cba1b502614202b841d472aad239ea6df81ffd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089125234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc974b41ee9acf444c77c43307544e9974fdc65c67c07b138f2b1579da78178f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 14 Feb 2024 21:12:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 14 Feb 2024 21:13:54 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:15:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:15:50 GMT
EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:15:51 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:15:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b3259e00f84e65b0d749ecdb1c509cfaefbab41e8cb1f6543ed1330430502`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61718a6e18dbd65ddf3f59fa04789e1f9acaec2f5cf25ce8cb26a3dd44c3282a`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a5ffeba7098ea453e541f16fce989d9bf9443e53b4a7da19cb16428f4d786`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab53e0e6ef70ca249e6e56bdd06de3a5697dd6cd838002e9be78c4e619e93d`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 444.5 KB (444454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86bd8e6e200eb4bd3eff9524dd7128bfb365522a7df4a2171325010624067c`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 8.2 MB (8221053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992357c2fc0a12399ad77caf56b874e927614befdc2b3f238971b92a4134141f`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd057cca0f909355ef1eaa7ea42b060645a1ebe3af92ea98a4fd2c16dffb9be9`  
		Last Modified: Wed, 14 Feb 2024 21:16:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765553db67243ec6679030d92c818bc160158ea025ce173c15d19bcdb0f0baa`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6`

```console
$ docker pull nats-streaming@sha256:d3175589326bc542cdc97ec4900237e1b603492994037e2e0451fb86de40bfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25.6` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine`

```console
$ docker pull nats-streaming@sha256:6e851c855d73cd1b5a82d7f97902276f92db9e4292ea494393c04a7ab5c5c8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d30fe82631f494b987479925af667ef45d90aa558e9382b0562de1dbc4506fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0967b77103d36801616352e9dd5095d2643efddea33ae3f17decaa4173b9aad2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:44:21 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 05:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 05:44:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 05:44:24 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 05:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 05:44:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051f87cffccdf4fbe1a90776658618b57180fce176ee9bb3cbd3395d9e4d253e`  
		Last Modified: Sat, 27 Jan 2024 05:44:44 GMT  
		Size: 8.1 MB (8065442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72378ed20c9f3302bcc39fa44b53028f820d640b981b48e8925bee35901cc573`  
		Last Modified: Sat, 27 Jan 2024 05:44:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3515d0b22fc24e6326557eeef983b71e0e79ef01de7248a31fdbda1076505315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01ac66f4ad49a362e865ff0cd64fbc6fe3bd5285801196dad2c7e6e9c28186`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:17:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:17:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:17:16 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:17:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:17:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc1417e242952eafa8945163bc8dc5655660d53b1c181774b3b3f0d3a57a3c`  
		Last Modified: Sat, 27 Jan 2024 00:17:44 GMT  
		Size: 7.7 MB (7683865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8f9dd70bb23d2f71b6d3a42d2a76e949167a79dfcb206e70b3961b11537b1`  
		Last Modified: Sat, 27 Jan 2024 00:17:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:e957f1f8c676db64ee3c5ccab427b465710b07dc68554c2b89ecb0c8f3f7733d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46650abce4a7529ca6e7e2c5c2d61f94c79943a4650cc6082d3eb273d511ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:17:58 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 01:18:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 01:18:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 01:18:01 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 01:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:18:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175d2f4269d43d5998f2114d4ea5cbc4d046ba44b79505566c01af45bdf4a27`  
		Last Modified: Sat, 27 Jan 2024 01:18:22 GMT  
		Size: 7.7 MB (7677345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718bd229c3a1354a4e359597856845aa6686c2b03fe8e1cecd7a213a4bccc22`  
		Last Modified: Sat, 27 Jan 2024 01:18:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:e472e8705b1475861a000cf1843db95825cb1d77e726269f0b7dca6fef430ada
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd63828fd18149ac4313c4214e50bf58ac6ebb0b46dbc91eda8032ab4c7a41b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:44:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:44:51 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:44:52 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:44:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e25adb5e1d79a1d0925d45e9c915e8e04b5be9669f15d99b87b65dbdac359`  
		Last Modified: Sat, 27 Jan 2024 00:45:09 GMT  
		Size: 7.4 MB (7384196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe3b347142aa6e063c7bad5378f82312940c683faa69b36527f66fa7267e97`  
		Last Modified: Sat, 27 Jan 2024 00:45:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine3.18`

```console
$ docker pull nats-streaming@sha256:6e851c855d73cd1b5a82d7f97902276f92db9e4292ea494393c04a7ab5c5c8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d30fe82631f494b987479925af667ef45d90aa558e9382b0562de1dbc4506fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0967b77103d36801616352e9dd5095d2643efddea33ae3f17decaa4173b9aad2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:44:21 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 05:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 05:44:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 05:44:24 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 05:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 05:44:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051f87cffccdf4fbe1a90776658618b57180fce176ee9bb3cbd3395d9e4d253e`  
		Last Modified: Sat, 27 Jan 2024 05:44:44 GMT  
		Size: 8.1 MB (8065442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72378ed20c9f3302bcc39fa44b53028f820d640b981b48e8925bee35901cc573`  
		Last Modified: Sat, 27 Jan 2024 05:44:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3515d0b22fc24e6326557eeef983b71e0e79ef01de7248a31fdbda1076505315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01ac66f4ad49a362e865ff0cd64fbc6fe3bd5285801196dad2c7e6e9c28186`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:17:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:17:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:17:16 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:17:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:17:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc1417e242952eafa8945163bc8dc5655660d53b1c181774b3b3f0d3a57a3c`  
		Last Modified: Sat, 27 Jan 2024 00:17:44 GMT  
		Size: 7.7 MB (7683865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8f9dd70bb23d2f71b6d3a42d2a76e949167a79dfcb206e70b3961b11537b1`  
		Last Modified: Sat, 27 Jan 2024 00:17:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:e957f1f8c676db64ee3c5ccab427b465710b07dc68554c2b89ecb0c8f3f7733d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46650abce4a7529ca6e7e2c5c2d61f94c79943a4650cc6082d3eb273d511ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:17:58 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 01:18:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 01:18:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 01:18:01 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 01:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:18:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175d2f4269d43d5998f2114d4ea5cbc4d046ba44b79505566c01af45bdf4a27`  
		Last Modified: Sat, 27 Jan 2024 01:18:22 GMT  
		Size: 7.7 MB (7677345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718bd229c3a1354a4e359597856845aa6686c2b03fe8e1cecd7a213a4bccc22`  
		Last Modified: Sat, 27 Jan 2024 01:18:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:e472e8705b1475861a000cf1843db95825cb1d77e726269f0b7dca6fef430ada
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd63828fd18149ac4313c4214e50bf58ac6ebb0b46dbc91eda8032ab4c7a41b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:44:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:44:51 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:44:52 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:44:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e25adb5e1d79a1d0925d45e9c915e8e04b5be9669f15d99b87b65dbdac359`  
		Last Modified: Sat, 27 Jan 2024 00:45:09 GMT  
		Size: 7.4 MB (7384196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe3b347142aa6e063c7bad5378f82312940c683faa69b36527f66fa7267e97`  
		Last Modified: Sat, 27 Jan 2024 00:45:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-linux`

```console
$ docker pull nats-streaming@sha256:6cfbe46b8f764cd35a24db7ffe7ae9e0f748b4b040a0001e545e6660e2c742d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-nanoserver`

```console
$ docker pull nats-streaming@sha256:0d3a445a8537b829d0ac495550172bc8bcbda974fed6fd3b410797582339a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25.6-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:0d3a445a8537b829d0ac495550172bc8bcbda974fed6fd3b410797582339a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25.6-nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-scratch`

```console
$ docker pull nats-streaming@sha256:6cfbe46b8f764cd35a24db7ffe7ae9e0f748b4b040a0001e545e6660e2c742d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-windowsservercore`

```console
$ docker pull nats-streaming@sha256:b5d4fe3f6ce89e3bcf22da05af606fd96758e494479efb60164c96fa902f6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25.6-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:302e53126d9b9b2338ce8da329cba1b502614202b841d472aad239ea6df81ffd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089125234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc974b41ee9acf444c77c43307544e9974fdc65c67c07b138f2b1579da78178f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 14 Feb 2024 21:12:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 14 Feb 2024 21:13:54 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:15:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:15:50 GMT
EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:15:51 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:15:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b3259e00f84e65b0d749ecdb1c509cfaefbab41e8cb1f6543ed1330430502`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61718a6e18dbd65ddf3f59fa04789e1f9acaec2f5cf25ce8cb26a3dd44c3282a`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a5ffeba7098ea453e541f16fce989d9bf9443e53b4a7da19cb16428f4d786`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab53e0e6ef70ca249e6e56bdd06de3a5697dd6cd838002e9be78c4e619e93d`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 444.5 KB (444454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86bd8e6e200eb4bd3eff9524dd7128bfb365522a7df4a2171325010624067c`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 8.2 MB (8221053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992357c2fc0a12399ad77caf56b874e927614befdc2b3f238971b92a4134141f`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd057cca0f909355ef1eaa7ea42b060645a1ebe3af92ea98a4fd2c16dffb9be9`  
		Last Modified: Wed, 14 Feb 2024 21:16:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765553db67243ec6679030d92c818bc160158ea025ce173c15d19bcdb0f0baa`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b5d4fe3f6ce89e3bcf22da05af606fd96758e494479efb60164c96fa902f6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:0.25.6-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:302e53126d9b9b2338ce8da329cba1b502614202b841d472aad239ea6df81ffd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089125234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc974b41ee9acf444c77c43307544e9974fdc65c67c07b138f2b1579da78178f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 14 Feb 2024 21:12:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 14 Feb 2024 21:13:54 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:15:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:15:50 GMT
EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:15:51 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:15:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b3259e00f84e65b0d749ecdb1c509cfaefbab41e8cb1f6543ed1330430502`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61718a6e18dbd65ddf3f59fa04789e1f9acaec2f5cf25ce8cb26a3dd44c3282a`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a5ffeba7098ea453e541f16fce989d9bf9443e53b4a7da19cb16428f4d786`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab53e0e6ef70ca249e6e56bdd06de3a5697dd6cd838002e9be78c4e619e93d`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 444.5 KB (444454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86bd8e6e200eb4bd3eff9524dd7128bfb365522a7df4a2171325010624067c`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 8.2 MB (8221053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992357c2fc0a12399ad77caf56b874e927614befdc2b3f238971b92a4134141f`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd057cca0f909355ef1eaa7ea42b060645a1ebe3af92ea98a4fd2c16dffb9be9`  
		Last Modified: Wed, 14 Feb 2024 21:16:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765553db67243ec6679030d92c818bc160158ea025ce173c15d19bcdb0f0baa`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:6e851c855d73cd1b5a82d7f97902276f92db9e4292ea494393c04a7ab5c5c8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d30fe82631f494b987479925af667ef45d90aa558e9382b0562de1dbc4506fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0967b77103d36801616352e9dd5095d2643efddea33ae3f17decaa4173b9aad2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:44:21 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 05:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 05:44:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 05:44:24 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 05:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 05:44:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051f87cffccdf4fbe1a90776658618b57180fce176ee9bb3cbd3395d9e4d253e`  
		Last Modified: Sat, 27 Jan 2024 05:44:44 GMT  
		Size: 8.1 MB (8065442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72378ed20c9f3302bcc39fa44b53028f820d640b981b48e8925bee35901cc573`  
		Last Modified: Sat, 27 Jan 2024 05:44:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3515d0b22fc24e6326557eeef983b71e0e79ef01de7248a31fdbda1076505315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01ac66f4ad49a362e865ff0cd64fbc6fe3bd5285801196dad2c7e6e9c28186`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:17:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:17:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:17:16 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:17:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:17:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc1417e242952eafa8945163bc8dc5655660d53b1c181774b3b3f0d3a57a3c`  
		Last Modified: Sat, 27 Jan 2024 00:17:44 GMT  
		Size: 7.7 MB (7683865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8f9dd70bb23d2f71b6d3a42d2a76e949167a79dfcb206e70b3961b11537b1`  
		Last Modified: Sat, 27 Jan 2024 00:17:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:e957f1f8c676db64ee3c5ccab427b465710b07dc68554c2b89ecb0c8f3f7733d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46650abce4a7529ca6e7e2c5c2d61f94c79943a4650cc6082d3eb273d511ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:17:58 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 01:18:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 01:18:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 01:18:01 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 01:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:18:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175d2f4269d43d5998f2114d4ea5cbc4d046ba44b79505566c01af45bdf4a27`  
		Last Modified: Sat, 27 Jan 2024 01:18:22 GMT  
		Size: 7.7 MB (7677345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718bd229c3a1354a4e359597856845aa6686c2b03fe8e1cecd7a213a4bccc22`  
		Last Modified: Sat, 27 Jan 2024 01:18:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:e472e8705b1475861a000cf1843db95825cb1d77e726269f0b7dca6fef430ada
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd63828fd18149ac4313c4214e50bf58ac6ebb0b46dbc91eda8032ab4c7a41b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:44:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:44:51 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:44:52 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:44:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e25adb5e1d79a1d0925d45e9c915e8e04b5be9669f15d99b87b65dbdac359`  
		Last Modified: Sat, 27 Jan 2024 00:45:09 GMT  
		Size: 7.4 MB (7384196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe3b347142aa6e063c7bad5378f82312940c683faa69b36527f66fa7267e97`  
		Last Modified: Sat, 27 Jan 2024 00:45:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.18`

```console
$ docker pull nats-streaming@sha256:6e851c855d73cd1b5a82d7f97902276f92db9e4292ea494393c04a7ab5c5c8f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d30fe82631f494b987479925af667ef45d90aa558e9382b0562de1dbc4506fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0967b77103d36801616352e9dd5095d2643efddea33ae3f17decaa4173b9aad2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:44:21 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 05:44:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 05:44:24 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 05:44:24 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 05:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 05:44:24 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051f87cffccdf4fbe1a90776658618b57180fce176ee9bb3cbd3395d9e4d253e`  
		Last Modified: Sat, 27 Jan 2024 05:44:44 GMT  
		Size: 8.1 MB (8065442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72378ed20c9f3302bcc39fa44b53028f820d640b981b48e8925bee35901cc573`  
		Last Modified: Sat, 27 Jan 2024 05:44:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:3515d0b22fc24e6326557eeef983b71e0e79ef01de7248a31fdbda1076505315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb01ac66f4ad49a362e865ff0cd64fbc6fe3bd5285801196dad2c7e6e9c28186`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:17:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:17:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:17:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:17:16 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:17:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:17:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bc1417e242952eafa8945163bc8dc5655660d53b1c181774b3b3f0d3a57a3c`  
		Last Modified: Sat, 27 Jan 2024 00:17:44 GMT  
		Size: 7.7 MB (7683865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8f9dd70bb23d2f71b6d3a42d2a76e949167a79dfcb206e70b3961b11537b1`  
		Last Modified: Sat, 27 Jan 2024 00:17:43 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:e957f1f8c676db64ee3c5ccab427b465710b07dc68554c2b89ecb0c8f3f7733d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d46650abce4a7529ca6e7e2c5c2d61f94c79943a4650cc6082d3eb273d511ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 01:17:58 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 01:18:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 01:18:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 01:18:01 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 01:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 01:18:01 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d175d2f4269d43d5998f2114d4ea5cbc4d046ba44b79505566c01af45bdf4a27`  
		Last Modified: Sat, 27 Jan 2024 01:18:22 GMT  
		Size: 7.7 MB (7677345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2718bd229c3a1354a4e359597856845aa6686c2b03fe8e1cecd7a213a4bccc22`  
		Last Modified: Sat, 27 Jan 2024 01:18:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:e472e8705b1475861a000cf1843db95825cb1d77e726269f0b7dca6fef430ada
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd63828fd18149ac4313c4214e50bf58ac6ebb0b46dbc91eda8032ab4c7a41b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 00:44:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 27 Jan 2024 00:44:51 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 27 Jan 2024 00:44:51 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 27 Jan 2024 00:44:52 GMT
EXPOSE 4222 8222
# Sat, 27 Jan 2024 00:44:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 00:44:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e25adb5e1d79a1d0925d45e9c915e8e04b5be9669f15d99b87b65dbdac359`  
		Last Modified: Sat, 27 Jan 2024 00:45:09 GMT  
		Size: 7.4 MB (7384196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe3b347142aa6e063c7bad5378f82312940c683faa69b36527f66fa7267e97`  
		Last Modified: Sat, 27 Jan 2024 00:45:08 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:d3175589326bc542cdc97ec4900237e1b603492994037e2e0451fb86de40bfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:6cfbe46b8f764cd35a24db7ffe7ae9e0f748b4b040a0001e545e6660e2c742d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:0d3a445a8537b829d0ac495550172bc8bcbda974fed6fd3b410797582339a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:0d3a445a8537b829d0ac495550172bc8bcbda974fed6fd3b410797582339a20c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:551bcc9afd52b4194000e7695525f12c02ab119ff9c520d647af80f63fad122e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112565520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7054fba02d7b07de67fab6900276b943495e5f361f8fc3dcb43948136de5d293`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 21:06:46 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:16:01 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 14 Feb 2024 21:16:02 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:16:03 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:16:04 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd7eae74de22c761805354bcde7e03fded48aeac3d87dc1c591f021397e89c3`  
		Last Modified: Wed, 14 Feb 2024 21:11:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f410c705fff81eec11ff9e4aa4a3f47ae85cff9a3338e862411f7638a4ee6cc`  
		Last Modified: Wed, 14 Feb 2024 21:16:40 GMT  
		Size: 7.9 MB (7939755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf66d9caf340fb5bf6125b279cfa499771d028a19e1483f54cced105d25304c`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da2be19a2ade86b484c7b2ab33fc862a1a311db2a585676d2d8d3941e84c7e1`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefb6a475923fba850e3f3593a10d7cab841730546250127f0b01aef7bc82529`  
		Last Modified: Wed, 14 Feb 2024 21:16:38 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:6cfbe46b8f764cd35a24db7ffe7ae9e0f748b4b040a0001e545e6660e2c742d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8d6f005926893c273b653c3df62d2fb4410865e75871f1d0a4009a4d1ffa705c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53a1183bda78c565c1bab8c7245b4fbd5d067585d4aa4f7058664944008aebe`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:29:01 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 18 Nov 2023 02:29:01 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:29:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:29:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:e5cad46933f27aa2ff957405100a10cb0380c4061c5e16917667dd8464abe292`  
		Last Modified: Sat, 18 Nov 2023 02:29:36 GMT  
		Size: 7.8 MB (7777354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:7c0df6b56800d90dc6702f47f13f23ffbc547d4940f5aae02065b6d2db2ab837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85ebd595a588f3973bc327448cfe9daa15b4ee2365c5d12e8e7c6b25bd8e1d`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:49:29 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 18 Nov 2023 02:49:30 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:49:30 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:49:30 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:64c568a9f16fd9cdb0de8ebe636484136fff965895eaaa1105d4fa97962a0789
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b26a17e490fa4e89a3e60275fc0517264a6b004a248e1433100b70b12d9312`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 01:57:50 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 18 Nov 2023 01:57:50 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:50 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 01:57:50 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:a5418828b8887c09cad299a747b7cab5ac1c2c6cc9f98e380f7b57ef088e8f29`  
		Last Modified: Sat, 18 Nov 2023 01:58:24 GMT  
		Size: 7.4 MB (7388059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:a6c4ef3fb6c552793ca4a6653cfebdb1aaad73856edaaec9e56fae6d9f48a8ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90d4821836429386947d73a15aab27182431ca54d08c6ed46cf288be974e380`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 18 Nov 2023 02:44:31 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 18 Nov 2023 02:44:32 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:44:32 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 18 Nov 2023 02:44:32 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:b5d4fe3f6ce89e3bcf22da05af606fd96758e494479efb60164c96fa902f6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:302e53126d9b9b2338ce8da329cba1b502614202b841d472aad239ea6df81ffd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089125234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc974b41ee9acf444c77c43307544e9974fdc65c67c07b138f2b1579da78178f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 14 Feb 2024 21:12:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 14 Feb 2024 21:13:54 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:15:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:15:50 GMT
EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:15:51 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:15:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b3259e00f84e65b0d749ecdb1c509cfaefbab41e8cb1f6543ed1330430502`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61718a6e18dbd65ddf3f59fa04789e1f9acaec2f5cf25ce8cb26a3dd44c3282a`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a5ffeba7098ea453e541f16fce989d9bf9443e53b4a7da19cb16428f4d786`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab53e0e6ef70ca249e6e56bdd06de3a5697dd6cd838002e9be78c4e619e93d`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 444.5 KB (444454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86bd8e6e200eb4bd3eff9524dd7128bfb365522a7df4a2171325010624067c`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 8.2 MB (8221053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992357c2fc0a12399ad77caf56b874e927614befdc2b3f238971b92a4134141f`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd057cca0f909355ef1eaa7ea42b060645a1ebe3af92ea98a4fd2c16dffb9be9`  
		Last Modified: Wed, 14 Feb 2024 21:16:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765553db67243ec6679030d92c818bc160158ea025ce173c15d19bcdb0f0baa`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:b5d4fe3f6ce89e3bcf22da05af606fd96758e494479efb60164c96fa902f6c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull nats-streaming@sha256:302e53126d9b9b2338ce8da329cba1b502614202b841d472aad239ea6df81ffd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089125234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc974b41ee9acf444c77c43307544e9974fdc65c67c07b138f2b1579da78178f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:03:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 14 Feb 2024 21:12:33 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 14 Feb 2024 21:12:34 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 14 Feb 2024 21:13:54 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Feb 2024 21:15:49 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Feb 2024 21:15:50 GMT
EXPOSE 4222 8222
# Wed, 14 Feb 2024 21:15:51 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Feb 2024 21:15:52 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9208e581b9c7283ab14481c804d0a464b4bbdac158f620660c16336ac0ebc5`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0b3259e00f84e65b0d749ecdb1c509cfaefbab41e8cb1f6543ed1330430502`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61718a6e18dbd65ddf3f59fa04789e1f9acaec2f5cf25ce8cb26a3dd44c3282a`  
		Last Modified: Wed, 14 Feb 2024 21:16:26 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564a5ffeba7098ea453e541f16fce989d9bf9443e53b4a7da19cb16428f4d786`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab53e0e6ef70ca249e6e56bdd06de3a5697dd6cd838002e9be78c4e619e93d`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 444.5 KB (444454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d86bd8e6e200eb4bd3eff9524dd7128bfb365522a7df4a2171325010624067c`  
		Last Modified: Wed, 14 Feb 2024 21:16:25 GMT  
		Size: 8.2 MB (8221053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992357c2fc0a12399ad77caf56b874e927614befdc2b3f238971b92a4134141f`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd057cca0f909355ef1eaa7ea42b060645a1ebe3af92ea98a4fd2c16dffb9be9`  
		Last Modified: Wed, 14 Feb 2024 21:16:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7765553db67243ec6679030d92c818bc160158ea025ce173c15d19bcdb0f0baa`  
		Last Modified: Wed, 14 Feb 2024 21:16:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
