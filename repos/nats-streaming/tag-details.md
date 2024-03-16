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
$ docker pull nats-streaming@sha256:ae51187bae9d37f9407f237a71f7d96d65769c643fda054db9d4fb833e536661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5576; amd64

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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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

### `nats-streaming:0.25` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:218a34373e65e68ab1d1ba46e734567b52aab87f8cc53e53bc7e79f77602a4eb
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
$ docker pull nats-streaming@sha256:d2ce10a9b14c9688e136149513b52f6e5212ea20057bc91b13f6538d5296a3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97c01900c3d29a1f30dd7839b5eb37714a5824896f2fd7c46e5ba4562527825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:28:43 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 01:28:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 01:28:47 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 01:28:47 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:28:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c467d0ede34b96cc613b0d85cfc844e40ef23eb1e070b85b51567b61899917`  
		Last Modified: Sat, 16 Mar 2024 01:29:13 GMT  
		Size: 7.7 MB (7683845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c6cd433b878b1b69633bbb2071e70419e1375e8085a73ce50841bed10c7768`  
		Last Modified: Sat, 16 Mar 2024 01:29:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d97902ef67ffeddc4a7b8c9eac212681dd7a6f85964610e407425c6163105a6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d30b6c04591961ebcfd07df6a2de4e4fe77e56f1ae03ca7779fddb6ea354a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:55:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 00:55:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 00:55:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 00:55:16 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:55:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bb86a270d12a041a04c3be2965765ea401b8386f4fd499326e20bc31b41d21`  
		Last Modified: Sat, 16 Mar 2024 00:55:33 GMT  
		Size: 7.7 MB (7677331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7753a8964894b186af5b86350df25917bbe0607a3a880e809fb1aa8173074aa9`  
		Last Modified: Sat, 16 Mar 2024 00:55:32 GMT  
		Size: 420.0 B  
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
$ docker pull nats-streaming@sha256:218a34373e65e68ab1d1ba46e734567b52aab87f8cc53e53bc7e79f77602a4eb
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
$ docker pull nats-streaming@sha256:d2ce10a9b14c9688e136149513b52f6e5212ea20057bc91b13f6538d5296a3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97c01900c3d29a1f30dd7839b5eb37714a5824896f2fd7c46e5ba4562527825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:28:43 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 01:28:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 01:28:47 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 01:28:47 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:28:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c467d0ede34b96cc613b0d85cfc844e40ef23eb1e070b85b51567b61899917`  
		Last Modified: Sat, 16 Mar 2024 01:29:13 GMT  
		Size: 7.7 MB (7683845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c6cd433b878b1b69633bbb2071e70419e1375e8085a73ce50841bed10c7768`  
		Last Modified: Sat, 16 Mar 2024 01:29:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d97902ef67ffeddc4a7b8c9eac212681dd7a6f85964610e407425c6163105a6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d30b6c04591961ebcfd07df6a2de4e4fe77e56f1ae03ca7779fddb6ea354a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:55:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 00:55:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 00:55:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 00:55:16 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:55:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bb86a270d12a041a04c3be2965765ea401b8386f4fd499326e20bc31b41d21`  
		Last Modified: Sat, 16 Mar 2024 00:55:33 GMT  
		Size: 7.7 MB (7677331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7753a8964894b186af5b86350df25917bbe0607a3a880e809fb1aa8173074aa9`  
		Last Modified: Sat, 16 Mar 2024 00:55:32 GMT  
		Size: 420.0 B  
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
$ docker pull nats-streaming@sha256:1c086a660940972ef487b4c7ddd5c3b75c5e4b6d922fa2fa1acf5aa7ddfd5af1
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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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
$ docker pull nats-streaming@sha256:4e6eeed3d41c3d874c29ab6e23921230466931ed9a475b7f2b86f30cb7c45e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:4e6eeed3d41c3d874c29ab6e23921230466931ed9a475b7f2b86f30cb7c45e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:1c086a660940972ef487b4c7ddd5c3b75c5e4b6d922fa2fa1acf5aa7ddfd5af1
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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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
$ docker pull nats-streaming@sha256:11922d28083d76646950c58b601c3a6a271531673742733bbfe4b6351e6181c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:9c4d983abf941a23f76a1c60beb3d0a1f45d52360c16d40ac6ac0a44e9f1ac91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2133791811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f77a096e9aceb8a32926cc759eeeded549f1d81ab8d5280934516e4e7bffd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:27:38 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 13 Mar 2024 02:28:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:31:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:31:09 GMT
EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4193a3f99b58d674c462ab8215619d97e7cd97466166fc2100016f5df992d8`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163526ee2ae223bf00dfbcea1259e738ae9622a08ba9fdbf57cd49dbdd14266c`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc4b2cf894281f795703ea9f8f2c8c0c17203e71208230ba193742426998da`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c077605ed526ee27a5b02e3296ef8e7642e8a33689c72e28eabc9465d19994`  
		Last Modified: Wed, 13 Mar 2024 02:31:50 GMT  
		Size: 449.4 KB (449361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb0c9e44e3c1e2859bd5e3eb90924fa0c61842beca952ed37050d6e51333b7`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 8.2 MB (8231389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c61e8f71d1bf670296bd1e939cb396fbbdb6a914047620148d1110de59b79`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70af4972b259e0428bd25d0f9239db63fd80283b5f63e2cfaf2704ab3449b981`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bec17e11cda34f8c5fe6ced7f8d51b6a7efdb0b2dc6e2df6bc5a4ecec8594f`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:11922d28083d76646950c58b601c3a6a271531673742733bbfe4b6351e6181c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:9c4d983abf941a23f76a1c60beb3d0a1f45d52360c16d40ac6ac0a44e9f1ac91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2133791811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f77a096e9aceb8a32926cc759eeeded549f1d81ab8d5280934516e4e7bffd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:27:38 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 13 Mar 2024 02:28:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:31:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:31:09 GMT
EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4193a3f99b58d674c462ab8215619d97e7cd97466166fc2100016f5df992d8`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163526ee2ae223bf00dfbcea1259e738ae9622a08ba9fdbf57cd49dbdd14266c`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc4b2cf894281f795703ea9f8f2c8c0c17203e71208230ba193742426998da`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c077605ed526ee27a5b02e3296ef8e7642e8a33689c72e28eabc9465d19994`  
		Last Modified: Wed, 13 Mar 2024 02:31:50 GMT  
		Size: 449.4 KB (449361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb0c9e44e3c1e2859bd5e3eb90924fa0c61842beca952ed37050d6e51333b7`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 8.2 MB (8231389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c61e8f71d1bf670296bd1e939cb396fbbdb6a914047620148d1110de59b79`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70af4972b259e0428bd25d0f9239db63fd80283b5f63e2cfaf2704ab3449b981`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bec17e11cda34f8c5fe6ced7f8d51b6a7efdb0b2dc6e2df6bc5a4ecec8594f`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6`

```console
$ docker pull nats-streaming@sha256:ae51187bae9d37f9407f237a71f7d96d65769c643fda054db9d4fb833e536661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5576; amd64

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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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

### `nats-streaming:0.25.6` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine`

```console
$ docker pull nats-streaming@sha256:218a34373e65e68ab1d1ba46e734567b52aab87f8cc53e53bc7e79f77602a4eb
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
$ docker pull nats-streaming@sha256:d2ce10a9b14c9688e136149513b52f6e5212ea20057bc91b13f6538d5296a3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97c01900c3d29a1f30dd7839b5eb37714a5824896f2fd7c46e5ba4562527825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:28:43 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 01:28:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 01:28:47 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 01:28:47 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:28:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c467d0ede34b96cc613b0d85cfc844e40ef23eb1e070b85b51567b61899917`  
		Last Modified: Sat, 16 Mar 2024 01:29:13 GMT  
		Size: 7.7 MB (7683845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c6cd433b878b1b69633bbb2071e70419e1375e8085a73ce50841bed10c7768`  
		Last Modified: Sat, 16 Mar 2024 01:29:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d97902ef67ffeddc4a7b8c9eac212681dd7a6f85964610e407425c6163105a6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d30b6c04591961ebcfd07df6a2de4e4fe77e56f1ae03ca7779fddb6ea354a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:55:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 00:55:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 00:55:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 00:55:16 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:55:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bb86a270d12a041a04c3be2965765ea401b8386f4fd499326e20bc31b41d21`  
		Last Modified: Sat, 16 Mar 2024 00:55:33 GMT  
		Size: 7.7 MB (7677331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7753a8964894b186af5b86350df25917bbe0607a3a880e809fb1aa8173074aa9`  
		Last Modified: Sat, 16 Mar 2024 00:55:32 GMT  
		Size: 420.0 B  
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
$ docker pull nats-streaming@sha256:218a34373e65e68ab1d1ba46e734567b52aab87f8cc53e53bc7e79f77602a4eb
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
$ docker pull nats-streaming@sha256:d2ce10a9b14c9688e136149513b52f6e5212ea20057bc91b13f6538d5296a3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97c01900c3d29a1f30dd7839b5eb37714a5824896f2fd7c46e5ba4562527825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:28:43 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 01:28:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 01:28:47 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 01:28:47 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:28:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c467d0ede34b96cc613b0d85cfc844e40ef23eb1e070b85b51567b61899917`  
		Last Modified: Sat, 16 Mar 2024 01:29:13 GMT  
		Size: 7.7 MB (7683845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c6cd433b878b1b69633bbb2071e70419e1375e8085a73ce50841bed10c7768`  
		Last Modified: Sat, 16 Mar 2024 01:29:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d97902ef67ffeddc4a7b8c9eac212681dd7a6f85964610e407425c6163105a6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d30b6c04591961ebcfd07df6a2de4e4fe77e56f1ae03ca7779fddb6ea354a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:55:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 00:55:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 00:55:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 00:55:16 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:55:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bb86a270d12a041a04c3be2965765ea401b8386f4fd499326e20bc31b41d21`  
		Last Modified: Sat, 16 Mar 2024 00:55:33 GMT  
		Size: 7.7 MB (7677331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7753a8964894b186af5b86350df25917bbe0607a3a880e809fb1aa8173074aa9`  
		Last Modified: Sat, 16 Mar 2024 00:55:32 GMT  
		Size: 420.0 B  
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
$ docker pull nats-streaming@sha256:1c086a660940972ef487b4c7ddd5c3b75c5e4b6d922fa2fa1acf5aa7ddfd5af1
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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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
$ docker pull nats-streaming@sha256:4e6eeed3d41c3d874c29ab6e23921230466931ed9a475b7f2b86f30cb7c45e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25.6-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:4e6eeed3d41c3d874c29ab6e23921230466931ed9a475b7f2b86f30cb7c45e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25.6-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-scratch`

```console
$ docker pull nats-streaming@sha256:1c086a660940972ef487b4c7ddd5c3b75c5e4b6d922fa2fa1acf5aa7ddfd5af1
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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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
$ docker pull nats-streaming@sha256:11922d28083d76646950c58b601c3a6a271531673742733bbfe4b6351e6181c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25.6-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:9c4d983abf941a23f76a1c60beb3d0a1f45d52360c16d40ac6ac0a44e9f1ac91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2133791811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f77a096e9aceb8a32926cc759eeeded549f1d81ab8d5280934516e4e7bffd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:27:38 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 13 Mar 2024 02:28:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:31:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:31:09 GMT
EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4193a3f99b58d674c462ab8215619d97e7cd97466166fc2100016f5df992d8`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163526ee2ae223bf00dfbcea1259e738ae9622a08ba9fdbf57cd49dbdd14266c`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc4b2cf894281f795703ea9f8f2c8c0c17203e71208230ba193742426998da`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c077605ed526ee27a5b02e3296ef8e7642e8a33689c72e28eabc9465d19994`  
		Last Modified: Wed, 13 Mar 2024 02:31:50 GMT  
		Size: 449.4 KB (449361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb0c9e44e3c1e2859bd5e3eb90924fa0c61842beca952ed37050d6e51333b7`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 8.2 MB (8231389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c61e8f71d1bf670296bd1e939cb396fbbdb6a914047620148d1110de59b79`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70af4972b259e0428bd25d0f9239db63fd80283b5f63e2cfaf2704ab3449b981`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bec17e11cda34f8c5fe6ced7f8d51b6a7efdb0b2dc6e2df6bc5a4ecec8594f`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:11922d28083d76646950c58b601c3a6a271531673742733bbfe4b6351e6181c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:0.25.6-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:9c4d983abf941a23f76a1c60beb3d0a1f45d52360c16d40ac6ac0a44e9f1ac91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2133791811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f77a096e9aceb8a32926cc759eeeded549f1d81ab8d5280934516e4e7bffd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:27:38 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 13 Mar 2024 02:28:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:31:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:31:09 GMT
EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4193a3f99b58d674c462ab8215619d97e7cd97466166fc2100016f5df992d8`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163526ee2ae223bf00dfbcea1259e738ae9622a08ba9fdbf57cd49dbdd14266c`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc4b2cf894281f795703ea9f8f2c8c0c17203e71208230ba193742426998da`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c077605ed526ee27a5b02e3296ef8e7642e8a33689c72e28eabc9465d19994`  
		Last Modified: Wed, 13 Mar 2024 02:31:50 GMT  
		Size: 449.4 KB (449361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb0c9e44e3c1e2859bd5e3eb90924fa0c61842beca952ed37050d6e51333b7`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 8.2 MB (8231389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c61e8f71d1bf670296bd1e939cb396fbbdb6a914047620148d1110de59b79`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70af4972b259e0428bd25d0f9239db63fd80283b5f63e2cfaf2704ab3449b981`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bec17e11cda34f8c5fe6ced7f8d51b6a7efdb0b2dc6e2df6bc5a4ecec8594f`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:218a34373e65e68ab1d1ba46e734567b52aab87f8cc53e53bc7e79f77602a4eb
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
$ docker pull nats-streaming@sha256:d2ce10a9b14c9688e136149513b52f6e5212ea20057bc91b13f6538d5296a3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97c01900c3d29a1f30dd7839b5eb37714a5824896f2fd7c46e5ba4562527825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:28:43 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 01:28:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 01:28:47 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 01:28:47 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:28:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c467d0ede34b96cc613b0d85cfc844e40ef23eb1e070b85b51567b61899917`  
		Last Modified: Sat, 16 Mar 2024 01:29:13 GMT  
		Size: 7.7 MB (7683845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c6cd433b878b1b69633bbb2071e70419e1375e8085a73ce50841bed10c7768`  
		Last Modified: Sat, 16 Mar 2024 01:29:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d97902ef67ffeddc4a7b8c9eac212681dd7a6f85964610e407425c6163105a6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d30b6c04591961ebcfd07df6a2de4e4fe77e56f1ae03ca7779fddb6ea354a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:55:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 00:55:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 00:55:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 00:55:16 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:55:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bb86a270d12a041a04c3be2965765ea401b8386f4fd499326e20bc31b41d21`  
		Last Modified: Sat, 16 Mar 2024 00:55:33 GMT  
		Size: 7.7 MB (7677331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7753a8964894b186af5b86350df25917bbe0607a3a880e809fb1aa8173074aa9`  
		Last Modified: Sat, 16 Mar 2024 00:55:32 GMT  
		Size: 420.0 B  
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
$ docker pull nats-streaming@sha256:218a34373e65e68ab1d1ba46e734567b52aab87f8cc53e53bc7e79f77602a4eb
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
$ docker pull nats-streaming@sha256:d2ce10a9b14c9688e136149513b52f6e5212ea20057bc91b13f6538d5296a3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10831325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97c01900c3d29a1f30dd7839b5eb37714a5824896f2fd7c46e5ba4562527825`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:28:43 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 01:28:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 01:28:47 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 01:28:47 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:28:48 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c467d0ede34b96cc613b0d85cfc844e40ef23eb1e070b85b51567b61899917`  
		Last Modified: Sat, 16 Mar 2024 01:29:13 GMT  
		Size: 7.7 MB (7683845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c6cd433b878b1b69633bbb2071e70419e1375e8085a73ce50841bed10c7768`  
		Last Modified: Sat, 16 Mar 2024 01:29:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d97902ef67ffeddc4a7b8c9eac212681dd7a6f85964610e407425c6163105a6a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10579143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d30b6c04591961ebcfd07df6a2de4e4fe77e56f1ae03ca7779fddb6ea354a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:55:13 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 00:55:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 00:55:16 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 00:55:16 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 00:55:16 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bb86a270d12a041a04c3be2965765ea401b8386f4fd499326e20bc31b41d21`  
		Last Modified: Sat, 16 Mar 2024 00:55:33 GMT  
		Size: 7.7 MB (7677331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7753a8964894b186af5b86350df25917bbe0607a3a880e809fb1aa8173074aa9`  
		Last Modified: Sat, 16 Mar 2024 00:55:32 GMT  
		Size: 420.0 B  
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
$ docker pull nats-streaming@sha256:ae51187bae9d37f9407f237a71f7d96d65769c643fda054db9d4fb833e536661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5576; amd64

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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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

### `nats-streaming:latest` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:1c086a660940972ef487b4c7ddd5c3b75c5e4b6d922fa2fa1acf5aa7ddfd5af1
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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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
$ docker pull nats-streaming@sha256:4e6eeed3d41c3d874c29ab6e23921230466931ed9a475b7f2b86f30cb7c45e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:4e6eeed3d41c3d874c29ab6e23921230466931ed9a475b7f2b86f30cb7c45e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:489107a0cb787c8008f8216a4db8659f52459ae84bc4d6ebe6b4e22d90d63b62
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.6 MB (112564606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e002c89bf30c425836ee9ef92d1c6a23adb41f9100346a099d59059c42e7a`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:21:55 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:31:27 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 13 Mar 2024 02:31:28 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:29 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e772fbc90f54f9eab2951a9615b88e9eca8fc78909aba2cb3678cc214eb88ae2`  
		Last Modified: Wed, 13 Mar 2024 02:26:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30c49cb357dffaf03f8aa4012c889342d8d148ed7439196d00ac4bc5e8ba873`  
		Last Modified: Wed, 13 Mar 2024 02:32:04 GMT  
		Size: 7.9 MB (7939849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23ce7f68fb1827ff9a57030bc9b05b1f7b30680cfb2cd2c0b071971ff546efe`  
		Last Modified: Wed, 13 Mar 2024 02:32:02 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69e656fd7ca19a2f62fb96492a2af095e6378a93565df51f3f6390f49ba2844`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ab08e2b3fac341f86ec3cbb23a10001da80bee66344871bc10e3d08edda289`  
		Last Modified: Wed, 13 Mar 2024 02:32:03 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:1c086a660940972ef487b4c7ddd5c3b75c5e4b6d922fa2fa1acf5aa7ddfd5af1
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
$ docker pull nats-streaming@sha256:06fb6244e01ee2f750a377e3b4667690606bd00b2da608ebf4d3f510da969f58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4163f52d657630a7497cc5ed780cb0e526d205ab44c1ed5db9bcd92421d441`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 01:28:54 GMT
COPY file:e4edbab8bcf05b4e72bb54c048c40d905be561470b53d7775b2681da921079bf in /nats-streaming-server 
# Sat, 16 Mar 2024 01:28:54 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 01:28:55 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 01:28:55 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:d82670b9d483091cddd30482cb665c0fc99fcc44efe4d1a3cceccc536352c6f1`  
		Last Modified: Sat, 18 Nov 2023 02:50:03 GMT  
		Size: 7.4 MB (7400558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:fd65026a57ec9b7f7526cc044f1fce18464576098d2d7f2a9f281ae551e9cfaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c161cb8c47bbfa86d413659c720348c856925d051a6aa594e3ae448d762c7a4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 00:55:20 GMT
COPY file:a0fedf18f5da1eeab300ea9cdcc5f58d326f2065865996f8076f6ad214be1e98 in /nats-streaming-server 
# Sat, 16 Mar 2024 00:55:20 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 00:55:20 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 00:55:20 GMT
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
$ docker pull nats-streaming@sha256:11922d28083d76646950c58b601c3a6a271531673742733bbfe4b6351e6181c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:9c4d983abf941a23f76a1c60beb3d0a1f45d52360c16d40ac6ac0a44e9f1ac91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2133791811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f77a096e9aceb8a32926cc759eeeded549f1d81ab8d5280934516e4e7bffd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:27:38 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 13 Mar 2024 02:28:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:31:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:31:09 GMT
EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4193a3f99b58d674c462ab8215619d97e7cd97466166fc2100016f5df992d8`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163526ee2ae223bf00dfbcea1259e738ae9622a08ba9fdbf57cd49dbdd14266c`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc4b2cf894281f795703ea9f8f2c8c0c17203e71208230ba193742426998da`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c077605ed526ee27a5b02e3296ef8e7642e8a33689c72e28eabc9465d19994`  
		Last Modified: Wed, 13 Mar 2024 02:31:50 GMT  
		Size: 449.4 KB (449361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb0c9e44e3c1e2859bd5e3eb90924fa0c61842beca952ed37050d6e51333b7`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 8.2 MB (8231389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c61e8f71d1bf670296bd1e939cb396fbbdb6a914047620148d1110de59b79`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70af4972b259e0428bd25d0f9239db63fd80283b5f63e2cfaf2704ab3449b981`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bec17e11cda34f8c5fe6ced7f8d51b6a7efdb0b2dc6e2df6bc5a4ecec8594f`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:11922d28083d76646950c58b601c3a6a271531673742733bbfe4b6351e6181c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull nats-streaming@sha256:9c4d983abf941a23f76a1c60beb3d0a1f45d52360c16d40ac6ac0a44e9f1ac91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2133791811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2f77a096e9aceb8a32926cc759eeeded549f1d81ab8d5280934516e4e7bffd`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 02:18:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 02:18:28 GMT
ENV NATS_DOCKERIZED=1
# Wed, 13 Mar 2024 02:27:38 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 13 Mar 2024 02:27:39 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 13 Mar 2024 02:28:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 13 Mar 2024 02:31:08 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 13 Mar 2024 02:31:09 GMT
EXPOSE 4222 8222
# Wed, 13 Mar 2024 02:31:10 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 13 Mar 2024 02:31:11 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e169e85f3c664d99b16235c550eb744e7e1421ceb3b4a239fd727321ccddc77`  
		Last Modified: Wed, 13 Mar 2024 02:26:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7cb8b6faf23b1820a39bd95d7664a27dd6143342b384e0331e51b7e7ba82b72`  
		Last Modified: Wed, 13 Mar 2024 02:26:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4193a3f99b58d674c462ab8215619d97e7cd97466166fc2100016f5df992d8`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163526ee2ae223bf00dfbcea1259e738ae9622a08ba9fdbf57cd49dbdd14266c`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc4b2cf894281f795703ea9f8f2c8c0c17203e71208230ba193742426998da`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c077605ed526ee27a5b02e3296ef8e7642e8a33689c72e28eabc9465d19994`  
		Last Modified: Wed, 13 Mar 2024 02:31:50 GMT  
		Size: 449.4 KB (449361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb0c9e44e3c1e2859bd5e3eb90924fa0c61842beca952ed37050d6e51333b7`  
		Last Modified: Wed, 13 Mar 2024 02:31:51 GMT  
		Size: 8.2 MB (8231389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68c61e8f71d1bf670296bd1e939cb396fbbdb6a914047620148d1110de59b79`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70af4972b259e0428bd25d0f9239db63fd80283b5f63e2cfaf2704ab3449b981`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4bec17e11cda34f8c5fe6ced7f8d51b6a7efdb0b2dc6e2df6bc5a4ecec8594f`  
		Last Modified: Wed, 13 Mar 2024 02:31:49 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
