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
$ docker pull nats-streaming@sha256:0ad6861379c936d508e2aad174fb402c170ec0b28c8f634549dea4b09f0451cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:cb5d0dd3013d543d571bb98a6052b8b31cdccc887c66c3487bdaaa3e456297dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:7bca31b2f5dc712636472d90fe2e901c92e595efa867f012ffe514f5342b3bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2055bdbd867e257f5dfbaad966437db74f2a8fb91c0ce34e11c01d843cf0cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:50:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 08:50:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 08:50:52 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 08:50:52 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:50:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea30858fa1d1a544c660e2832502015da4916b3aecc47e9b13ed0890564f49`  
		Last Modified: Sat, 16 Mar 2024 08:51:11 GMT  
		Size: 8.1 MB (8065454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a6c57f3a81f1d7f0a635dddd7f8ee5a87a1c3e7ab4f52cf1fac4f9ebd4c4f8`  
		Last Modified: Sat, 16 Mar 2024 08:51:09 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:0b5f8f8393d3bb6c76f6613d1e8b4b7c6c6b40382874392828306d9b44c5c6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4814ec8c6a7c47abdf62159668be50b1e9e0b9a7d3af6776e720367a11d27c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:57 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 05:16:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 05:16:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 05:16:00 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:16:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f7f4286faf28a5d67e6cd2e5bf722dcb70ca247d34f2065c50d7ba84e453d1`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 7.4 MB (7384186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6da6b8138b224e53df86980dec6e31a3a413bd8ecedba0e7517cfd26b1752c0`  
		Last Modified: Sat, 16 Mar 2024 05:16:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.18`

```console
$ docker pull nats-streaming@sha256:cb5d0dd3013d543d571bb98a6052b8b31cdccc887c66c3487bdaaa3e456297dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:7bca31b2f5dc712636472d90fe2e901c92e595efa867f012ffe514f5342b3bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2055bdbd867e257f5dfbaad966437db74f2a8fb91c0ce34e11c01d843cf0cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:50:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 08:50:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 08:50:52 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 08:50:52 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:50:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea30858fa1d1a544c660e2832502015da4916b3aecc47e9b13ed0890564f49`  
		Last Modified: Sat, 16 Mar 2024 08:51:11 GMT  
		Size: 8.1 MB (8065454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a6c57f3a81f1d7f0a635dddd7f8ee5a87a1c3e7ab4f52cf1fac4f9ebd4c4f8`  
		Last Modified: Sat, 16 Mar 2024 08:51:09 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:0b5f8f8393d3bb6c76f6613d1e8b4b7c6c6b40382874392828306d9b44c5c6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4814ec8c6a7c47abdf62159668be50b1e9e0b9a7d3af6776e720367a11d27c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:57 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 05:16:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 05:16:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 05:16:00 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:16:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f7f4286faf28a5d67e6cd2e5bf722dcb70ca247d34f2065c50d7ba84e453d1`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 7.4 MB (7384186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6da6b8138b224e53df86980dec6e31a3a413bd8ecedba0e7517cfd26b1752c0`  
		Last Modified: Sat, 16 Mar 2024 05:16:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-linux`

```console
$ docker pull nats-streaming@sha256:3b640126ccd563a5027ba457581e1ff5b1991e43eb043542643dfad1ca3e2b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver`

```console
$ docker pull nats-streaming@sha256:432b88d315533e8344457d46cb18ee124d5f5776ca25560c0523441189cbb037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:432b88d315533e8344457d46cb18ee124d5f5776ca25560c0523441189cbb037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:3b640126ccd563a5027ba457581e1ff5b1991e43eb043542643dfad1ca3e2b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore`

```console
$ docker pull nats-streaming@sha256:5de1094142e1b161973750a17e245ea11f7b8bb7fd72db8ebd8a8395d1b81295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:6f9381d3e4ff76527621bb14375d52c4d107252e674fdfc44141233eec505183
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229355246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b470f67940400e0346a52c19e778babf405bc629ddd82fa11245ff01f14b48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:08:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 12 Jun 2024 19:08:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 12 Jun 2024 19:08:24 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 12 Jun 2024 19:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:11:45 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:11:46 GMT
EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:11:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:11:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f890c2f6d49f5b5faa72376a41109d1cd36e69f78c8be56278197ed420fce`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b095918301fc53ed9bc33cc42d7e0fbc7dda23062ab25af935c830e8e09f905`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd55c0a09dea8ff8113a7ef260d9a54599812f142b49578fd6c9d1896ea85ac`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318ccb92ab256e146401cfd636034263605a419cf1410b1275bd25d2f0d2103f`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 431.4 KB (431424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86db8acc59d2bc7b36832ef64fa78a92e9b65cc2e25aac00020d73a1a0fdb320`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 8.2 MB (8231342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9e5c96fc63f40856e0ee532d33086bcd8983ba0a3d3ac158ceaeb049133276`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113eb53f25a86a92e3a3332f771b5dbaea535847c70103187bcadc9f15d4bb8`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bad7162e1e2ffefa1b46ea60f331ca73c099443695c2a54f813e45e4417b6d`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:5de1094142e1b161973750a17e245ea11f7b8bb7fd72db8ebd8a8395d1b81295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:6f9381d3e4ff76527621bb14375d52c4d107252e674fdfc44141233eec505183
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229355246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b470f67940400e0346a52c19e778babf405bc629ddd82fa11245ff01f14b48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:08:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 12 Jun 2024 19:08:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 12 Jun 2024 19:08:24 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 12 Jun 2024 19:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:11:45 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:11:46 GMT
EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:11:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:11:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f890c2f6d49f5b5faa72376a41109d1cd36e69f78c8be56278197ed420fce`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b095918301fc53ed9bc33cc42d7e0fbc7dda23062ab25af935c830e8e09f905`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd55c0a09dea8ff8113a7ef260d9a54599812f142b49578fd6c9d1896ea85ac`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318ccb92ab256e146401cfd636034263605a419cf1410b1275bd25d2f0d2103f`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 431.4 KB (431424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86db8acc59d2bc7b36832ef64fa78a92e9b65cc2e25aac00020d73a1a0fdb320`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 8.2 MB (8231342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9e5c96fc63f40856e0ee532d33086bcd8983ba0a3d3ac158ceaeb049133276`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113eb53f25a86a92e3a3332f771b5dbaea535847c70103187bcadc9f15d4bb8`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bad7162e1e2ffefa1b46ea60f331ca73c099443695c2a54f813e45e4417b6d`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6`

```console
$ docker pull nats-streaming@sha256:0ad6861379c936d508e2aad174fb402c170ec0b28c8f634549dea4b09f0451cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25.6` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine`

```console
$ docker pull nats-streaming@sha256:cb5d0dd3013d543d571bb98a6052b8b31cdccc887c66c3487bdaaa3e456297dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:7bca31b2f5dc712636472d90fe2e901c92e595efa867f012ffe514f5342b3bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2055bdbd867e257f5dfbaad966437db74f2a8fb91c0ce34e11c01d843cf0cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:50:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 08:50:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 08:50:52 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 08:50:52 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:50:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea30858fa1d1a544c660e2832502015da4916b3aecc47e9b13ed0890564f49`  
		Last Modified: Sat, 16 Mar 2024 08:51:11 GMT  
		Size: 8.1 MB (8065454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a6c57f3a81f1d7f0a635dddd7f8ee5a87a1c3e7ab4f52cf1fac4f9ebd4c4f8`  
		Last Modified: Sat, 16 Mar 2024 08:51:09 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:0b5f8f8393d3bb6c76f6613d1e8b4b7c6c6b40382874392828306d9b44c5c6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4814ec8c6a7c47abdf62159668be50b1e9e0b9a7d3af6776e720367a11d27c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:57 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 05:16:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 05:16:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 05:16:00 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:16:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f7f4286faf28a5d67e6cd2e5bf722dcb70ca247d34f2065c50d7ba84e453d1`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 7.4 MB (7384186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6da6b8138b224e53df86980dec6e31a3a413bd8ecedba0e7517cfd26b1752c0`  
		Last Modified: Sat, 16 Mar 2024 05:16:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine3.18`

```console
$ docker pull nats-streaming@sha256:cb5d0dd3013d543d571bb98a6052b8b31cdccc887c66c3487bdaaa3e456297dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:7bca31b2f5dc712636472d90fe2e901c92e595efa867f012ffe514f5342b3bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2055bdbd867e257f5dfbaad966437db74f2a8fb91c0ce34e11c01d843cf0cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:50:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 08:50:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 08:50:52 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 08:50:52 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:50:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea30858fa1d1a544c660e2832502015da4916b3aecc47e9b13ed0890564f49`  
		Last Modified: Sat, 16 Mar 2024 08:51:11 GMT  
		Size: 8.1 MB (8065454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a6c57f3a81f1d7f0a635dddd7f8ee5a87a1c3e7ab4f52cf1fac4f9ebd4c4f8`  
		Last Modified: Sat, 16 Mar 2024 08:51:09 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:0b5f8f8393d3bb6c76f6613d1e8b4b7c6c6b40382874392828306d9b44c5c6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4814ec8c6a7c47abdf62159668be50b1e9e0b9a7d3af6776e720367a11d27c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:57 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 05:16:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 05:16:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 05:16:00 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:16:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f7f4286faf28a5d67e6cd2e5bf722dcb70ca247d34f2065c50d7ba84e453d1`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 7.4 MB (7384186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6da6b8138b224e53df86980dec6e31a3a413bd8ecedba0e7517cfd26b1752c0`  
		Last Modified: Sat, 16 Mar 2024 05:16:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-linux`

```console
$ docker pull nats-streaming@sha256:3b640126ccd563a5027ba457581e1ff5b1991e43eb043542643dfad1ca3e2b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-nanoserver`

```console
$ docker pull nats-streaming@sha256:432b88d315533e8344457d46cb18ee124d5f5776ca25560c0523441189cbb037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25.6-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:432b88d315533e8344457d46cb18ee124d5f5776ca25560c0523441189cbb037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25.6-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-scratch`

```console
$ docker pull nats-streaming@sha256:3b640126ccd563a5027ba457581e1ff5b1991e43eb043542643dfad1ca3e2b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-windowsservercore`

```console
$ docker pull nats-streaming@sha256:5de1094142e1b161973750a17e245ea11f7b8bb7fd72db8ebd8a8395d1b81295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25.6-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:6f9381d3e4ff76527621bb14375d52c4d107252e674fdfc44141233eec505183
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229355246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b470f67940400e0346a52c19e778babf405bc629ddd82fa11245ff01f14b48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:08:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 12 Jun 2024 19:08:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 12 Jun 2024 19:08:24 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 12 Jun 2024 19:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:11:45 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:11:46 GMT
EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:11:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:11:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f890c2f6d49f5b5faa72376a41109d1cd36e69f78c8be56278197ed420fce`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b095918301fc53ed9bc33cc42d7e0fbc7dda23062ab25af935c830e8e09f905`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd55c0a09dea8ff8113a7ef260d9a54599812f142b49578fd6c9d1896ea85ac`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318ccb92ab256e146401cfd636034263605a419cf1410b1275bd25d2f0d2103f`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 431.4 KB (431424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86db8acc59d2bc7b36832ef64fa78a92e9b65cc2e25aac00020d73a1a0fdb320`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 8.2 MB (8231342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9e5c96fc63f40856e0ee532d33086bcd8983ba0a3d3ac158ceaeb049133276`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113eb53f25a86a92e3a3332f771b5dbaea535847c70103187bcadc9f15d4bb8`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bad7162e1e2ffefa1b46ea60f331ca73c099443695c2a54f813e45e4417b6d`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:5de1094142e1b161973750a17e245ea11f7b8bb7fd72db8ebd8a8395d1b81295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:0.25.6-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:6f9381d3e4ff76527621bb14375d52c4d107252e674fdfc44141233eec505183
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229355246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b470f67940400e0346a52c19e778babf405bc629ddd82fa11245ff01f14b48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:08:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 12 Jun 2024 19:08:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 12 Jun 2024 19:08:24 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 12 Jun 2024 19:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:11:45 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:11:46 GMT
EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:11:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:11:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f890c2f6d49f5b5faa72376a41109d1cd36e69f78c8be56278197ed420fce`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b095918301fc53ed9bc33cc42d7e0fbc7dda23062ab25af935c830e8e09f905`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd55c0a09dea8ff8113a7ef260d9a54599812f142b49578fd6c9d1896ea85ac`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318ccb92ab256e146401cfd636034263605a419cf1410b1275bd25d2f0d2103f`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 431.4 KB (431424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86db8acc59d2bc7b36832ef64fa78a92e9b65cc2e25aac00020d73a1a0fdb320`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 8.2 MB (8231342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9e5c96fc63f40856e0ee532d33086bcd8983ba0a3d3ac158ceaeb049133276`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113eb53f25a86a92e3a3332f771b5dbaea535847c70103187bcadc9f15d4bb8`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bad7162e1e2ffefa1b46ea60f331ca73c099443695c2a54f813e45e4417b6d`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:cb5d0dd3013d543d571bb98a6052b8b31cdccc887c66c3487bdaaa3e456297dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:7bca31b2f5dc712636472d90fe2e901c92e595efa867f012ffe514f5342b3bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2055bdbd867e257f5dfbaad966437db74f2a8fb91c0ce34e11c01d843cf0cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:50:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 08:50:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 08:50:52 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 08:50:52 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:50:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea30858fa1d1a544c660e2832502015da4916b3aecc47e9b13ed0890564f49`  
		Last Modified: Sat, 16 Mar 2024 08:51:11 GMT  
		Size: 8.1 MB (8065454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a6c57f3a81f1d7f0a635dddd7f8ee5a87a1c3e7ab4f52cf1fac4f9ebd4c4f8`  
		Last Modified: Sat, 16 Mar 2024 08:51:09 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:0b5f8f8393d3bb6c76f6613d1e8b4b7c6c6b40382874392828306d9b44c5c6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4814ec8c6a7c47abdf62159668be50b1e9e0b9a7d3af6776e720367a11d27c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:57 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 05:16:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 05:16:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 05:16:00 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:16:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f7f4286faf28a5d67e6cd2e5bf722dcb70ca247d34f2065c50d7ba84e453d1`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 7.4 MB (7384186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6da6b8138b224e53df86980dec6e31a3a413bd8ecedba0e7517cfd26b1752c0`  
		Last Modified: Sat, 16 Mar 2024 05:16:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.18`

```console
$ docker pull nats-streaming@sha256:cb5d0dd3013d543d571bb98a6052b8b31cdccc887c66c3487bdaaa3e456297dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:7bca31b2f5dc712636472d90fe2e901c92e595efa867f012ffe514f5342b3bc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2055bdbd867e257f5dfbaad966437db74f2a8fb91c0ce34e11c01d843cf0cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:50:49 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 08:50:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 08:50:52 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 08:50:52 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:50:52 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eea30858fa1d1a544c660e2832502015da4916b3aecc47e9b13ed0890564f49`  
		Last Modified: Sat, 16 Mar 2024 08:51:11 GMT  
		Size: 8.1 MB (8065454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a6c57f3a81f1d7f0a635dddd7f8ee5a87a1c3e7ab4f52cf1fac4f9ebd4c4f8`  
		Last Modified: Sat, 16 Mar 2024 08:51:09 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:0b5f8f8393d3bb6c76f6613d1e8b4b7c6c6b40382874392828306d9b44c5c6ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4814ec8c6a7c47abdf62159668be50b1e9e0b9a7d3af6776e720367a11d27c6a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:15:57 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 16 Mar 2024 05:16:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 16 Mar 2024 05:16:00 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 16 Mar 2024 05:16:00 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:16:00 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f7f4286faf28a5d67e6cd2e5bf722dcb70ca247d34f2065c50d7ba84e453d1`  
		Last Modified: Sat, 16 Mar 2024 05:16:17 GMT  
		Size: 7.4 MB (7384186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6da6b8138b224e53df86980dec6e31a3a413bd8ecedba0e7517cfd26b1752c0`  
		Last Modified: Sat, 16 Mar 2024 05:16:16 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:0ad6861379c936d508e2aad174fb402c170ec0b28c8f634549dea4b09f0451cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:3b640126ccd563a5027ba457581e1ff5b1991e43eb043542643dfad1ca3e2b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:432b88d315533e8344457d46cb18ee124d5f5776ca25560c0523441189cbb037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:432b88d315533e8344457d46cb18ee124d5f5776ca25560c0523441189cbb037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:f0063eac606b42959bdec335d6315fb60ba8c6c25fdd8a621bed60ab9d918bd6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162977702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9213e0a566ffb01024513e9eb365b561f701bb42940cdb0921281d1946740b40`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:02:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:12:07 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Wed, 12 Jun 2024 19:12:08 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:12:09 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:12:10 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c539c028d0db9674b43971ee9d9dd647ef348536c7a8d55f6eede1247af0`  
		Last Modified: Wed, 12 Jun 2024 19:07:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca7d1aa5c6d118589b127f7495cbfe0f23ccb770817e9e5945b1a2f21971887`  
		Last Modified: Wed, 12 Jun 2024 19:12:50 GMT  
		Size: 7.9 MB (7939844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ac0c8798b798dd8479fcb6c21e23d74237f7ebf272d7f2064bdfb6557086`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b431e66df9ca6cda95a902271bd7f6a74e69eca60ac2a35d5e88af1f9977150`  
		Last Modified: Wed, 12 Jun 2024 19:12:49 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffeef166e44d5500efdd30e2330ed109e14423c0e61c78e2637f56b431b76034`  
		Last Modified: Wed, 12 Jun 2024 19:12:48 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:3b640126ccd563a5027ba457581e1ff5b1991e43eb043542643dfad1ca3e2b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:cfeaa9d128d0dfdfbe254f3cab4ca9c6b562a03d4dbd695d64f3f4d1383a6255
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7777354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057c745866d77be6899705727e5702fd275b8061d4d3ad11c4e16afd8e110cdb`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 08:50:57 GMT
COPY file:92b8f18bcb458f5a197f505a3104acf1ff24dd17af04c49ea6ec9023b8329567 in /nats-streaming-server 
# Sat, 16 Mar 2024 08:50:57 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 08:50:57 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 08:50:57 GMT
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
$ docker pull nats-streaming@sha256:2b6043ce38d64e7124f35bb0fcafbe3eb1bb3d9f73d7449e1e3e97c39dd2e8f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a58171c486dd5f62d5bc6dfb3885e61f2c433f7e9975b78bd527e64ca6d1ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 16 Mar 2024 05:16:04 GMT
COPY file:8f9c2dbf1fcd3755dd17d681f1b889ae68b5cedb72307930fdc22fbc67eb18de in /nats-streaming-server 
# Sat, 16 Mar 2024 05:16:04 GMT
EXPOSE 4222 8222
# Sat, 16 Mar 2024 05:16:04 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 16 Mar 2024 05:16:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:dc12bae7d7f45f1f51e8e37b3fb5b893b9d91868787b681621a8d425376bb434`  
		Last Modified: Sat, 18 Nov 2023 02:45:08 GMT  
		Size: 7.1 MB (7094726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:5de1094142e1b161973750a17e245ea11f7b8bb7fd72db8ebd8a8395d1b81295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:6f9381d3e4ff76527621bb14375d52c4d107252e674fdfc44141233eec505183
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229355246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b470f67940400e0346a52c19e778babf405bc629ddd82fa11245ff01f14b48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:08:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 12 Jun 2024 19:08:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 12 Jun 2024 19:08:24 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 12 Jun 2024 19:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:11:45 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:11:46 GMT
EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:11:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:11:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f890c2f6d49f5b5faa72376a41109d1cd36e69f78c8be56278197ed420fce`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b095918301fc53ed9bc33cc42d7e0fbc7dda23062ab25af935c830e8e09f905`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd55c0a09dea8ff8113a7ef260d9a54599812f142b49578fd6c9d1896ea85ac`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318ccb92ab256e146401cfd636034263605a419cf1410b1275bd25d2f0d2103f`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 431.4 KB (431424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86db8acc59d2bc7b36832ef64fa78a92e9b65cc2e25aac00020d73a1a0fdb320`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 8.2 MB (8231342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9e5c96fc63f40856e0ee532d33086bcd8983ba0a3d3ac158ceaeb049133276`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113eb53f25a86a92e3a3332f771b5dbaea535847c70103187bcadc9f15d4bb8`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bad7162e1e2ffefa1b46ea60f331ca73c099443695c2a54f813e45e4417b6d`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:5de1094142e1b161973750a17e245ea11f7b8bb7fd72db8ebd8a8395d1b81295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull nats-streaming@sha256:6f9381d3e4ff76527621bb14375d52c4d107252e674fdfc44141233eec505183
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229355246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b470f67940400e0346a52c19e778babf405bc629ddd82fa11245ff01f14b48`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:59:30 GMT
ENV NATS_DOCKERIZED=1
# Wed, 12 Jun 2024 19:08:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Wed, 12 Jun 2024 19:08:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Wed, 12 Jun 2024 19:08:24 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Wed, 12 Jun 2024 19:09:39 GMT
RUN Set-PSDebug -Trace 2
# Wed, 12 Jun 2024 19:11:45 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 12 Jun 2024 19:11:46 GMT
EXPOSE 4222 8222
# Wed, 12 Jun 2024 19:11:46 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 12 Jun 2024 19:11:47 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06141158aebc1921afac5da541cf6a80846edb4296669ef6f8370783d67dfd2`  
		Last Modified: Wed, 12 Jun 2024 19:06:58 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1f890c2f6d49f5b5faa72376a41109d1cd36e69f78c8be56278197ed420fce`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b095918301fc53ed9bc33cc42d7e0fbc7dda23062ab25af935c830e8e09f905`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd55c0a09dea8ff8113a7ef260d9a54599812f142b49578fd6c9d1896ea85ac`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318ccb92ab256e146401cfd636034263605a419cf1410b1275bd25d2f0d2103f`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 431.4 KB (431424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86db8acc59d2bc7b36832ef64fa78a92e9b65cc2e25aac00020d73a1a0fdb320`  
		Last Modified: Wed, 12 Jun 2024 19:12:37 GMT  
		Size: 8.2 MB (8231342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9e5c96fc63f40856e0ee532d33086bcd8983ba0a3d3ac158ceaeb049133276`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113eb53f25a86a92e3a3332f771b5dbaea535847c70103187bcadc9f15d4bb8`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bad7162e1e2ffefa1b46ea60f331ca73c099443695c2a54f813e45e4417b6d`  
		Last Modified: Wed, 12 Jun 2024 19:12:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
