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
$ docker pull nats-streaming@sha256:e36f453ee118d120d1b17181ef0944c451d3f7da663f34a05a0ca9d2a39aaa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5329; amd64

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

### `nats-streaming:0.25` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:60b023557a91c23e126b543419e8e6cbefbc11c907bf0f635ebe3b96f900217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d84da22737144287b6459bc98bce1b143544f83c8f33ec4c1e8feef688c0e39c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88617ef01bf601eb17e8b5fd1755397608ced1859ce0fee5fc87a1c438723b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:22:12 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 07:22:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 07:22:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 07:22:14 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 07:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:22:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684dd758c98c554ddaa95d325c1619aeb3ad47f95d6182101a99dfa8e13e4c2`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 8.1 MB (8065444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb019fe9da20cfe7c67066cdd6069b21276ccfb7fa27954f3555a969c97a7ba`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
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
$ docker pull nats-streaming@sha256:abbbf5007a2b2dfbeb0a7efdb8cbc36ca614876b1abe4d6756bfd1acc1323f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10578767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd5898d661a32e966f4ea31877d9ac99eb67a9ea2c196202dee1910f35877b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:30:29 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 08:30:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 08:30:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 08:30:32 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 08:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:30:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421082cacf280bb45849c620ac6d8a0c8d0509ec30fb7d17db4ba192fbc5c84`  
		Last Modified: Fri, 01 Dec 2023 08:31:00 GMT  
		Size: 7.7 MB (7677340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad03b6741b55853dea5a04939f9598d890645714c62c4fda469423b3977fd5b`  
		Last Modified: Fri, 01 Dec 2023 08:30:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:cef82268848dc537eae48cbc4bf414c58cbdacc7c6b0e609ccd07d4ed92dcde4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893998fae52b1f3f958aa9a0ac466176d842e3af553b094603bfc0ce69e4db4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:39:14 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 02:39:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 02:39:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 02:39:17 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 02:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:39:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318505a0c79672c628a0ac4d008fae18ecb79f1b702c6bdcef5040f64e4046e5`  
		Last Modified: Fri, 01 Dec 2023 02:39:48 GMT  
		Size: 7.4 MB (7384194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5007e76563fe796b31efc1feab7f88579a0c81b3272b05be4a465aa15e9cac7`  
		Last Modified: Fri, 01 Dec 2023 02:39:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.18`

```console
$ docker pull nats-streaming@sha256:60b023557a91c23e126b543419e8e6cbefbc11c907bf0f635ebe3b96f900217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d84da22737144287b6459bc98bce1b143544f83c8f33ec4c1e8feef688c0e39c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88617ef01bf601eb17e8b5fd1755397608ced1859ce0fee5fc87a1c438723b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:22:12 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 07:22:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 07:22:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 07:22:14 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 07:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:22:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684dd758c98c554ddaa95d325c1619aeb3ad47f95d6182101a99dfa8e13e4c2`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 8.1 MB (8065444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb019fe9da20cfe7c67066cdd6069b21276ccfb7fa27954f3555a969c97a7ba`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
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
$ docker pull nats-streaming@sha256:abbbf5007a2b2dfbeb0a7efdb8cbc36ca614876b1abe4d6756bfd1acc1323f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10578767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd5898d661a32e966f4ea31877d9ac99eb67a9ea2c196202dee1910f35877b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:30:29 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 08:30:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 08:30:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 08:30:32 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 08:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:30:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421082cacf280bb45849c620ac6d8a0c8d0509ec30fb7d17db4ba192fbc5c84`  
		Last Modified: Fri, 01 Dec 2023 08:31:00 GMT  
		Size: 7.7 MB (7677340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad03b6741b55853dea5a04939f9598d890645714c62c4fda469423b3977fd5b`  
		Last Modified: Fri, 01 Dec 2023 08:30:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:cef82268848dc537eae48cbc4bf414c58cbdacc7c6b0e609ccd07d4ed92dcde4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893998fae52b1f3f958aa9a0ac466176d842e3af553b094603bfc0ce69e4db4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:39:14 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 02:39:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 02:39:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 02:39:17 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 02:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:39:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318505a0c79672c628a0ac4d008fae18ecb79f1b702c6bdcef5040f64e4046e5`  
		Last Modified: Fri, 01 Dec 2023 02:39:48 GMT  
		Size: 7.4 MB (7384194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5007e76563fe796b31efc1feab7f88579a0c81b3272b05be4a465aa15e9cac7`  
		Last Modified: Fri, 01 Dec 2023 02:39:47 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:d9baff41672286456cb25553f6b3752ff4195b72941e2d751078740011015a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d9baff41672286456cb25553f6b3752ff4195b72941e2d751078740011015a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
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
$ docker pull nats-streaming@sha256:4cbd2706cd1d95119a7ce51031370a8a5b7653f014d9b1f0bf07edcece3b158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:44cccd1de5cdef464c71e1b292c7dead72c426910571658e8850fd4d1b309309
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2078396844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df3fcbf0ec9a34211939157e551b4bdc55ff171d3c0f0b9e20097ef2f20639c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:19:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Thu, 11 Jan 2024 00:20:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:22:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:22:10 GMT
EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05ab57d44543385151c8610fa56ab11106332c85a7ab348d845a673f20bb0db`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ba15a853867300bc022ffc6df9788bf7dc9bf4d757e08474b225a16a0412b`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232131abf9c289a8a4ab64a9404d7f8fa5d411c4b611a26858ece34341938fba`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab33fd8dad737256a3607627cde82f29f9ac5c0df0a4b7097242b7ddfe890e`  
		Last Modified: Thu, 11 Jan 2024 00:22:47 GMT  
		Size: 442.4 KB (442432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb917942de51002790d35e5cdb486ee6e00826918915053e5519433ed62b9c`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 8.2 MB (8221411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7694c6a6449f76f0a367250a8aec212973656a265f03d865aec7aa7eba9c5cb`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c94ea4fdaee7450ea36246d255fef77fa0a55f7fc11fae44cb4205f54a23e3`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d321e2b1505d745fdf03d2ca8d0b061d57682436fa3900be5b22a4ffb4c055`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:4cbd2706cd1d95119a7ce51031370a8a5b7653f014d9b1f0bf07edcece3b158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:44cccd1de5cdef464c71e1b292c7dead72c426910571658e8850fd4d1b309309
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2078396844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df3fcbf0ec9a34211939157e551b4bdc55ff171d3c0f0b9e20097ef2f20639c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:19:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Thu, 11 Jan 2024 00:20:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:22:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:22:10 GMT
EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05ab57d44543385151c8610fa56ab11106332c85a7ab348d845a673f20bb0db`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ba15a853867300bc022ffc6df9788bf7dc9bf4d757e08474b225a16a0412b`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232131abf9c289a8a4ab64a9404d7f8fa5d411c4b611a26858ece34341938fba`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab33fd8dad737256a3607627cde82f29f9ac5c0df0a4b7097242b7ddfe890e`  
		Last Modified: Thu, 11 Jan 2024 00:22:47 GMT  
		Size: 442.4 KB (442432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb917942de51002790d35e5cdb486ee6e00826918915053e5519433ed62b9c`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 8.2 MB (8221411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7694c6a6449f76f0a367250a8aec212973656a265f03d865aec7aa7eba9c5cb`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c94ea4fdaee7450ea36246d255fef77fa0a55f7fc11fae44cb4205f54a23e3`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d321e2b1505d745fdf03d2ca8d0b061d57682436fa3900be5b22a4ffb4c055`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6`

```console
$ docker pull nats-streaming@sha256:e36f453ee118d120d1b17181ef0944c451d3f7da663f34a05a0ca9d2a39aaa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5329; amd64

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

### `nats-streaming:0.25.6` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine`

```console
$ docker pull nats-streaming@sha256:60b023557a91c23e126b543419e8e6cbefbc11c907bf0f635ebe3b96f900217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d84da22737144287b6459bc98bce1b143544f83c8f33ec4c1e8feef688c0e39c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88617ef01bf601eb17e8b5fd1755397608ced1859ce0fee5fc87a1c438723b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:22:12 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 07:22:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 07:22:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 07:22:14 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 07:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:22:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684dd758c98c554ddaa95d325c1619aeb3ad47f95d6182101a99dfa8e13e4c2`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 8.1 MB (8065444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb019fe9da20cfe7c67066cdd6069b21276ccfb7fa27954f3555a969c97a7ba`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
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
$ docker pull nats-streaming@sha256:abbbf5007a2b2dfbeb0a7efdb8cbc36ca614876b1abe4d6756bfd1acc1323f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10578767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd5898d661a32e966f4ea31877d9ac99eb67a9ea2c196202dee1910f35877b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:30:29 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 08:30:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 08:30:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 08:30:32 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 08:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:30:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421082cacf280bb45849c620ac6d8a0c8d0509ec30fb7d17db4ba192fbc5c84`  
		Last Modified: Fri, 01 Dec 2023 08:31:00 GMT  
		Size: 7.7 MB (7677340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad03b6741b55853dea5a04939f9598d890645714c62c4fda469423b3977fd5b`  
		Last Modified: Fri, 01 Dec 2023 08:30:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:cef82268848dc537eae48cbc4bf414c58cbdacc7c6b0e609ccd07d4ed92dcde4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893998fae52b1f3f958aa9a0ac466176d842e3af553b094603bfc0ce69e4db4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:39:14 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 02:39:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 02:39:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 02:39:17 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 02:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:39:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318505a0c79672c628a0ac4d008fae18ecb79f1b702c6bdcef5040f64e4046e5`  
		Last Modified: Fri, 01 Dec 2023 02:39:48 GMT  
		Size: 7.4 MB (7384194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5007e76563fe796b31efc1feab7f88579a0c81b3272b05be4a465aa15e9cac7`  
		Last Modified: Fri, 01 Dec 2023 02:39:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine3.18`

```console
$ docker pull nats-streaming@sha256:60b023557a91c23e126b543419e8e6cbefbc11c907bf0f635ebe3b96f900217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.6-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d84da22737144287b6459bc98bce1b143544f83c8f33ec4c1e8feef688c0e39c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88617ef01bf601eb17e8b5fd1755397608ced1859ce0fee5fc87a1c438723b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:22:12 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 07:22:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 07:22:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 07:22:14 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 07:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:22:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684dd758c98c554ddaa95d325c1619aeb3ad47f95d6182101a99dfa8e13e4c2`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 8.1 MB (8065444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb019fe9da20cfe7c67066cdd6069b21276ccfb7fa27954f3555a969c97a7ba`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
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
$ docker pull nats-streaming@sha256:abbbf5007a2b2dfbeb0a7efdb8cbc36ca614876b1abe4d6756bfd1acc1323f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10578767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd5898d661a32e966f4ea31877d9ac99eb67a9ea2c196202dee1910f35877b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:30:29 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 08:30:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 08:30:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 08:30:32 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 08:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:30:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421082cacf280bb45849c620ac6d8a0c8d0509ec30fb7d17db4ba192fbc5c84`  
		Last Modified: Fri, 01 Dec 2023 08:31:00 GMT  
		Size: 7.7 MB (7677340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad03b6741b55853dea5a04939f9598d890645714c62c4fda469423b3977fd5b`  
		Last Modified: Fri, 01 Dec 2023 08:30:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:cef82268848dc537eae48cbc4bf414c58cbdacc7c6b0e609ccd07d4ed92dcde4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893998fae52b1f3f958aa9a0ac466176d842e3af553b094603bfc0ce69e4db4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:39:14 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 02:39:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 02:39:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 02:39:17 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 02:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:39:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318505a0c79672c628a0ac4d008fae18ecb79f1b702c6bdcef5040f64e4046e5`  
		Last Modified: Fri, 01 Dec 2023 02:39:48 GMT  
		Size: 7.4 MB (7384194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5007e76563fe796b31efc1feab7f88579a0c81b3272b05be4a465aa15e9cac7`  
		Last Modified: Fri, 01 Dec 2023 02:39:47 GMT  
		Size: 421.0 B  
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
$ docker pull nats-streaming@sha256:d9baff41672286456cb25553f6b3752ff4195b72941e2d751078740011015a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25.6-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d9baff41672286456cb25553f6b3752ff4195b72941e2d751078740011015a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25.6-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
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
$ docker pull nats-streaming@sha256:4cbd2706cd1d95119a7ce51031370a8a5b7653f014d9b1f0bf07edcece3b158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25.6-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:44cccd1de5cdef464c71e1b292c7dead72c426910571658e8850fd4d1b309309
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2078396844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df3fcbf0ec9a34211939157e551b4bdc55ff171d3c0f0b9e20097ef2f20639c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:19:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Thu, 11 Jan 2024 00:20:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:22:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:22:10 GMT
EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05ab57d44543385151c8610fa56ab11106332c85a7ab348d845a673f20bb0db`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ba15a853867300bc022ffc6df9788bf7dc9bf4d757e08474b225a16a0412b`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232131abf9c289a8a4ab64a9404d7f8fa5d411c4b611a26858ece34341938fba`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab33fd8dad737256a3607627cde82f29f9ac5c0df0a4b7097242b7ddfe890e`  
		Last Modified: Thu, 11 Jan 2024 00:22:47 GMT  
		Size: 442.4 KB (442432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb917942de51002790d35e5cdb486ee6e00826918915053e5519433ed62b9c`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 8.2 MB (8221411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7694c6a6449f76f0a367250a8aec212973656a265f03d865aec7aa7eba9c5cb`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c94ea4fdaee7450ea36246d255fef77fa0a55f7fc11fae44cb4205f54a23e3`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d321e2b1505d745fdf03d2ca8d0b061d57682436fa3900be5b22a4ffb4c055`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:4cbd2706cd1d95119a7ce51031370a8a5b7653f014d9b1f0bf07edcece3b158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:0.25.6-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:44cccd1de5cdef464c71e1b292c7dead72c426910571658e8850fd4d1b309309
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2078396844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df3fcbf0ec9a34211939157e551b4bdc55ff171d3c0f0b9e20097ef2f20639c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:19:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Thu, 11 Jan 2024 00:20:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:22:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:22:10 GMT
EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05ab57d44543385151c8610fa56ab11106332c85a7ab348d845a673f20bb0db`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ba15a853867300bc022ffc6df9788bf7dc9bf4d757e08474b225a16a0412b`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232131abf9c289a8a4ab64a9404d7f8fa5d411c4b611a26858ece34341938fba`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab33fd8dad737256a3607627cde82f29f9ac5c0df0a4b7097242b7ddfe890e`  
		Last Modified: Thu, 11 Jan 2024 00:22:47 GMT  
		Size: 442.4 KB (442432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb917942de51002790d35e5cdb486ee6e00826918915053e5519433ed62b9c`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 8.2 MB (8221411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7694c6a6449f76f0a367250a8aec212973656a265f03d865aec7aa7eba9c5cb`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c94ea4fdaee7450ea36246d255fef77fa0a55f7fc11fae44cb4205f54a23e3`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d321e2b1505d745fdf03d2ca8d0b061d57682436fa3900be5b22a4ffb4c055`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:60b023557a91c23e126b543419e8e6cbefbc11c907bf0f635ebe3b96f900217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d84da22737144287b6459bc98bce1b143544f83c8f33ec4c1e8feef688c0e39c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88617ef01bf601eb17e8b5fd1755397608ced1859ce0fee5fc87a1c438723b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:22:12 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 07:22:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 07:22:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 07:22:14 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 07:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:22:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684dd758c98c554ddaa95d325c1619aeb3ad47f95d6182101a99dfa8e13e4c2`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 8.1 MB (8065444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb019fe9da20cfe7c67066cdd6069b21276ccfb7fa27954f3555a969c97a7ba`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
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
$ docker pull nats-streaming@sha256:abbbf5007a2b2dfbeb0a7efdb8cbc36ca614876b1abe4d6756bfd1acc1323f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10578767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd5898d661a32e966f4ea31877d9ac99eb67a9ea2c196202dee1910f35877b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:30:29 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 08:30:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 08:30:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 08:30:32 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 08:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:30:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421082cacf280bb45849c620ac6d8a0c8d0509ec30fb7d17db4ba192fbc5c84`  
		Last Modified: Fri, 01 Dec 2023 08:31:00 GMT  
		Size: 7.7 MB (7677340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad03b6741b55853dea5a04939f9598d890645714c62c4fda469423b3977fd5b`  
		Last Modified: Fri, 01 Dec 2023 08:30:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:cef82268848dc537eae48cbc4bf414c58cbdacc7c6b0e609ccd07d4ed92dcde4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893998fae52b1f3f958aa9a0ac466176d842e3af553b094603bfc0ce69e4db4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:39:14 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 02:39:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 02:39:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 02:39:17 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 02:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:39:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318505a0c79672c628a0ac4d008fae18ecb79f1b702c6bdcef5040f64e4046e5`  
		Last Modified: Fri, 01 Dec 2023 02:39:48 GMT  
		Size: 7.4 MB (7384194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5007e76563fe796b31efc1feab7f88579a0c81b3272b05be4a465aa15e9cac7`  
		Last Modified: Fri, 01 Dec 2023 02:39:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.18`

```console
$ docker pull nats-streaming@sha256:60b023557a91c23e126b543419e8e6cbefbc11c907bf0f635ebe3b96f900217d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:d84da22737144287b6459bc98bce1b143544f83c8f33ec4c1e8feef688c0e39c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88617ef01bf601eb17e8b5fd1755397608ced1859ce0fee5fc87a1c438723b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:22:12 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 07:22:14 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 07:22:14 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 07:22:14 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 07:22:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:22:15 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684dd758c98c554ddaa95d325c1619aeb3ad47f95d6182101a99dfa8e13e4c2`  
		Last Modified: Fri, 01 Dec 2023 07:22:37 GMT  
		Size: 8.1 MB (8065444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb019fe9da20cfe7c67066cdd6069b21276ccfb7fa27954f3555a969c97a7ba`  
		Last Modified: Fri, 01 Dec 2023 07:22:35 GMT  
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
$ docker pull nats-streaming@sha256:abbbf5007a2b2dfbeb0a7efdb8cbc36ca614876b1abe4d6756bfd1acc1323f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10578767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd5898d661a32e966f4ea31877d9ac99eb67a9ea2c196202dee1910f35877b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:30:29 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 08:30:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 08:30:32 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 08:30:32 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 08:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 08:30:32 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f421082cacf280bb45849c620ac6d8a0c8d0509ec30fb7d17db4ba192fbc5c84`  
		Last Modified: Fri, 01 Dec 2023 08:31:00 GMT  
		Size: 7.7 MB (7677340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad03b6741b55853dea5a04939f9598d890645714c62c4fda469423b3977fd5b`  
		Last Modified: Fri, 01 Dec 2023 08:30:59 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:cef82268848dc537eae48cbc4bf414c58cbdacc7c6b0e609ccd07d4ed92dcde4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9893998fae52b1f3f958aa9a0ac466176d842e3af553b094603bfc0ce69e4db4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:39:14 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Fri, 01 Dec 2023 02:39:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Fri, 01 Dec 2023 02:39:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Fri, 01 Dec 2023 02:39:17 GMT
EXPOSE 4222 8222
# Fri, 01 Dec 2023 02:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:39:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:318505a0c79672c628a0ac4d008fae18ecb79f1b702c6bdcef5040f64e4046e5`  
		Last Modified: Fri, 01 Dec 2023 02:39:48 GMT  
		Size: 7.4 MB (7384194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5007e76563fe796b31efc1feab7f88579a0c81b3272b05be4a465aa15e9cac7`  
		Last Modified: Fri, 01 Dec 2023 02:39:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:e36f453ee118d120d1b17181ef0944c451d3f7da663f34a05a0ca9d2a39aaa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5329; amd64

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

### `nats-streaming:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
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
$ docker pull nats-streaming@sha256:d9baff41672286456cb25553f6b3752ff4195b72941e2d751078740011015a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:d9baff41672286456cb25553f6b3752ff4195b72941e2d751078740011015a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:9040f45949185aa31e9ba6f2ebbee0dc53dbf39d1c2bc1dc9126c5989886a411
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112535314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61246a9f36f2538b44b2683657710097a065db5b770955abbfcec5842cbaa756`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:14:04 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Thu, 11 Jan 2024 00:22:22 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:23 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:24 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4377a0a62f51b1f64493890ef3b4440dbd88c0cc9d4dc760b7faadc1595b426`  
		Last Modified: Thu, 11 Jan 2024 00:18:07 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d99a3500b296e1a4c18f430fc41a7c97484378839749328221a462d6686d73`  
		Last Modified: Thu, 11 Jan 2024 00:23:02 GMT  
		Size: 7.9 MB (7939720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6942b3af1e5d39cd92daf589553d832e60cc4a61e3b822daffba9ca553a8b479`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f48ed9fda722cf6aae8ec7922efb1a64a1082ec4e59f3102d52e7e23fdb052e`  
		Last Modified: Thu, 11 Jan 2024 00:23:00 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8282b138066213461dc4281e25ce96528b046ca517df50c831315e1c9c44965`  
		Last Modified: Thu, 11 Jan 2024 00:23:01 GMT  
		Size: 1.0 KB (1030 bytes)  
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
$ docker pull nats-streaming@sha256:4cbd2706cd1d95119a7ce51031370a8a5b7653f014d9b1f0bf07edcece3b158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:44cccd1de5cdef464c71e1b292c7dead72c426910571658e8850fd4d1b309309
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2078396844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df3fcbf0ec9a34211939157e551b4bdc55ff171d3c0f0b9e20097ef2f20639c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:19:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Thu, 11 Jan 2024 00:20:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:22:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:22:10 GMT
EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05ab57d44543385151c8610fa56ab11106332c85a7ab348d845a673f20bb0db`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ba15a853867300bc022ffc6df9788bf7dc9bf4d757e08474b225a16a0412b`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232131abf9c289a8a4ab64a9404d7f8fa5d411c4b611a26858ece34341938fba`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab33fd8dad737256a3607627cde82f29f9ac5c0df0a4b7097242b7ddfe890e`  
		Last Modified: Thu, 11 Jan 2024 00:22:47 GMT  
		Size: 442.4 KB (442432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb917942de51002790d35e5cdb486ee6e00826918915053e5519433ed62b9c`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 8.2 MB (8221411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7694c6a6449f76f0a367250a8aec212973656a265f03d865aec7aa7eba9c5cb`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c94ea4fdaee7450ea36246d255fef77fa0a55f7fc11fae44cb4205f54a23e3`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d321e2b1505d745fdf03d2ca8d0b061d57682436fa3900be5b22a4ffb4c055`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:4cbd2706cd1d95119a7ce51031370a8a5b7653f014d9b1f0bf07edcece3b158c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull nats-streaming@sha256:44cccd1de5cdef464c71e1b292c7dead72c426910571658e8850fd4d1b309309
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2078396844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df3fcbf0ec9a34211939157e551b4bdc55ff171d3c0f0b9e20097ef2f20639c`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 11 Jan 2024 00:11:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:11:22 GMT
ENV NATS_DOCKERIZED=1
# Thu, 11 Jan 2024 00:19:22 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Thu, 11 Jan 2024 00:19:23 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Thu, 11 Jan 2024 00:20:20 GMT
RUN Set-PSDebug -Trace 2
# Thu, 11 Jan 2024 00:22:09 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Thu, 11 Jan 2024 00:22:10 GMT
EXPOSE 4222 8222
# Thu, 11 Jan 2024 00:22:11 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Thu, 11 Jan 2024 00:22:12 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f58648120a89cda871dff4e60c5ba44243bbdf720f3062ba50394593b19f0a`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e7c0830e36cde394e19298af81bfc1484702705b4c82f8695e7c7c3e90d452`  
		Last Modified: Thu, 11 Jan 2024 00:17:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05ab57d44543385151c8610fa56ab11106332c85a7ab348d845a673f20bb0db`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626ba15a853867300bc022ffc6df9788bf7dc9bf4d757e08474b225a16a0412b`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232131abf9c289a8a4ab64a9404d7f8fa5d411c4b611a26858ece34341938fba`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eab33fd8dad737256a3607627cde82f29f9ac5c0df0a4b7097242b7ddfe890e`  
		Last Modified: Thu, 11 Jan 2024 00:22:47 GMT  
		Size: 442.4 KB (442432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fb917942de51002790d35e5cdb486ee6e00826918915053e5519433ed62b9c`  
		Last Modified: Thu, 11 Jan 2024 00:22:48 GMT  
		Size: 8.2 MB (8221411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7694c6a6449f76f0a367250a8aec212973656a265f03d865aec7aa7eba9c5cb`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c94ea4fdaee7450ea36246d255fef77fa0a55f7fc11fae44cb4205f54a23e3`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d321e2b1505d745fdf03d2ca8d0b061d57682436fa3900be5b22a4ffb4c055`  
		Last Modified: Thu, 11 Jan 2024 00:22:46 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
