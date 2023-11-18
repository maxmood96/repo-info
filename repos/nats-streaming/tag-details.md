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
$ docker pull nats-streaming@sha256:48e7eebc23a4c3fcb78b435c669ba42b495fc874ae9b0620524a38cf0e819f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5122; amd64

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
$ docker pull nats-streaming@sha256:a87972dc3059ea6664b8b58be08e426c79497d7ac25366e22a2d128239e94e5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7311545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab17242c3507f68896194a4ab65f92f9f98dd9c82d517bb1140b9f8660e13ae`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:31:22 GMT
COPY file:9bc2f7015ff72f7e91556a01075e89ef8a85a404228874028f7a356e8142e169 in /nats-streaming-server 
# Sat, 21 Oct 2023 00:31:22 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:22 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:31:22 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ee4a78724efc3390679e6118a2f2c5993c9075f378bd6a2f0b7f99b50579fb2b`  
		Last Modified: Wed, 21 Jun 2023 00:59:42 GMT  
		Size: 7.3 MB (7311545 bytes)  
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
$ docker pull nats-streaming@sha256:39e2025550e8c6ce15ff33eb51d4bbe0f3bee94abf9228d4c00b110d8cf8f122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee463d44f75f11b62539f48d51d34d166ae0a16a7aa08b56e946b3c5ec8c91`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:16:01 GMT
COPY file:8237d0d59fd3c6b32e52dbff50861a8848f846505c0303e7975e4a5f48ce8de9 in /nats-streaming-server 
# Sat, 21 Oct 2023 02:16:01 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:16:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:16:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c3b4c14668a8e32e87c6ea3dce4a99716b527ba7f0f4608cbab27184c89832ee`  
		Last Modified: Wed, 21 Jun 2023 01:12:24 GMT  
		Size: 7.0 MB (7011458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:446403cb2698594aa07d1df0990b2bd73e1b1a85a4c6b09a02dc76781486e6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:5859c557b26b7a0fe2ac0ed1abcd28b65b7b4079c61c5676e571a24a29ccd672
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11467834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff243b212b0831f50bcd77a0491acbace8fab4b4f90e833beb96190a36956323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 02:28:36 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:28:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 02:28:38 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 02:28:38 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 02:28:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690158cab3634c349851670ded01f5084d40069dc81a2e9b2385ccdaf4270c84`  
		Last Modified: Sat, 18 Nov 2023 02:29:17 GMT  
		Size: 8.1 MB (8065445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeb121e6ed536362a47268822d991954a198aa42e5f02a89a127a507bb50540`  
		Last Modified: Sat, 18 Nov 2023 02:29:16 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:123e1046c498e5fd86f61e61dd3b3682917c9accedb7d7774180c891601c1d09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10746016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd703820d68e38aa74550071c7f277c1a1647a0cde20da491bab952a2e0d341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:31:16 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:31:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:31:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:31:19 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:31:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f819de770d62324a67c19c681691204f02bd8de83d0d009b92714abfea616`  
		Last Modified: Sat, 21 Oct 2023 00:31:36 GMT  
		Size: 7.6 MB (7600300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4eccbe16f8571a693b997c0f54a8c9f8d081559dca4a246f0035908ceee5e1`  
		Last Modified: Sat, 21 Oct 2023 00:31:35 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b56622afee477c4e1c1f7644f71af82eac0d18a5b42323ccc2462512eb595aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10577650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f64236a48aac92e3e16bf95947467dbc7884e91f8dcde09be468e5ad0e2ca42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 01:57:31 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 01:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 01:57:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 01:57:34 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 01:57:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afe10cc0d63e3a6f9e87c371ba8152ff8d978964ee1dc901aca748ae26b8b2f`  
		Last Modified: Sat, 18 Nov 2023 01:58:06 GMT  
		Size: 7.7 MB (7677323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66aeb4d96d5dbd82f75f18b9691f89ce8e82ed9b2b5f6c5d7469a52a3561508`  
		Last Modified: Sat, 18 Nov 2023 01:58:05 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:690162b6622a5bb198bde138afc9191ec7c05b953a3d901bd26102f616e1e3cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10632371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b037ffd8b7268a4c1bc628d638199f10ba54bb901751616d66703b30c81da1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:15:54 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:15:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:15:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:15:57 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:15:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a86dd6d8430110c1d880bd46dc6c42418e7269d8140aa3e58dc795d4ecfc03`  
		Last Modified: Sat, 21 Oct 2023 02:16:14 GMT  
		Size: 7.3 MB (7300119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416d20af0c6435894ca9435014dd34f1e4f86db1cd813b20dc3e0a2f493796dd`  
		Last Modified: Sat, 21 Oct 2023 02:16:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.18`

```console
$ docker pull nats-streaming@sha256:446403cb2698594aa07d1df0990b2bd73e1b1a85a4c6b09a02dc76781486e6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:5859c557b26b7a0fe2ac0ed1abcd28b65b7b4079c61c5676e571a24a29ccd672
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11467834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff243b212b0831f50bcd77a0491acbace8fab4b4f90e833beb96190a36956323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 02:28:36 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:28:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 02:28:38 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 02:28:38 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 02:28:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690158cab3634c349851670ded01f5084d40069dc81a2e9b2385ccdaf4270c84`  
		Last Modified: Sat, 18 Nov 2023 02:29:17 GMT  
		Size: 8.1 MB (8065445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeb121e6ed536362a47268822d991954a198aa42e5f02a89a127a507bb50540`  
		Last Modified: Sat, 18 Nov 2023 02:29:16 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:123e1046c498e5fd86f61e61dd3b3682917c9accedb7d7774180c891601c1d09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10746016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd703820d68e38aa74550071c7f277c1a1647a0cde20da491bab952a2e0d341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:31:16 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:31:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:31:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:31:19 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:31:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f819de770d62324a67c19c681691204f02bd8de83d0d009b92714abfea616`  
		Last Modified: Sat, 21 Oct 2023 00:31:36 GMT  
		Size: 7.6 MB (7600300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4eccbe16f8571a693b997c0f54a8c9f8d081559dca4a246f0035908ceee5e1`  
		Last Modified: Sat, 21 Oct 2023 00:31:35 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b56622afee477c4e1c1f7644f71af82eac0d18a5b42323ccc2462512eb595aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10577650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f64236a48aac92e3e16bf95947467dbc7884e91f8dcde09be468e5ad0e2ca42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 01:57:31 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 01:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 01:57:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 01:57:34 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 01:57:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afe10cc0d63e3a6f9e87c371ba8152ff8d978964ee1dc901aca748ae26b8b2f`  
		Last Modified: Sat, 18 Nov 2023 01:58:06 GMT  
		Size: 7.7 MB (7677323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66aeb4d96d5dbd82f75f18b9691f89ce8e82ed9b2b5f6c5d7469a52a3561508`  
		Last Modified: Sat, 18 Nov 2023 01:58:05 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:690162b6622a5bb198bde138afc9191ec7c05b953a3d901bd26102f616e1e3cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10632371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b037ffd8b7268a4c1bc628d638199f10ba54bb901751616d66703b30c81da1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:15:54 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:15:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:15:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:15:57 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:15:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a86dd6d8430110c1d880bd46dc6c42418e7269d8140aa3e58dc795d4ecfc03`  
		Last Modified: Sat, 21 Oct 2023 02:16:14 GMT  
		Size: 7.3 MB (7300119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416d20af0c6435894ca9435014dd34f1e4f86db1cd813b20dc3e0a2f493796dd`  
		Last Modified: Sat, 21 Oct 2023 02:16:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-linux`

```console
$ docker pull nats-streaming@sha256:3b03df6f4f365e45ce2ff7700d817788549e41ef5106635bc8f3d9beff53573d
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
$ docker pull nats-streaming@sha256:a87972dc3059ea6664b8b58be08e426c79497d7ac25366e22a2d128239e94e5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7311545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab17242c3507f68896194a4ab65f92f9f98dd9c82d517bb1140b9f8660e13ae`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:31:22 GMT
COPY file:9bc2f7015ff72f7e91556a01075e89ef8a85a404228874028f7a356e8142e169 in /nats-streaming-server 
# Sat, 21 Oct 2023 00:31:22 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:22 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:31:22 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ee4a78724efc3390679e6118a2f2c5993c9075f378bd6a2f0b7f99b50579fb2b`  
		Last Modified: Wed, 21 Jun 2023 00:59:42 GMT  
		Size: 7.3 MB (7311545 bytes)  
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
$ docker pull nats-streaming@sha256:39e2025550e8c6ce15ff33eb51d4bbe0f3bee94abf9228d4c00b110d8cf8f122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee463d44f75f11b62539f48d51d34d166ae0a16a7aa08b56e946b3c5ec8c91`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:16:01 GMT
COPY file:8237d0d59fd3c6b32e52dbff50861a8848f846505c0303e7975e4a5f48ce8de9 in /nats-streaming-server 
# Sat, 21 Oct 2023 02:16:01 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:16:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:16:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c3b4c14668a8e32e87c6ea3dce4a99716b527ba7f0f4608cbab27184c89832ee`  
		Last Modified: Wed, 21 Jun 2023 01:12:24 GMT  
		Size: 7.0 MB (7011458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver`

```console
$ docker pull nats-streaming@sha256:90a40c6c74be4457c8c4c2052c50a992b69ef298e20426a97f9246d42eef35c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:90a40c6c74be4457c8c4c2052c50a992b69ef298e20426a97f9246d42eef35c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:3b03df6f4f365e45ce2ff7700d817788549e41ef5106635bc8f3d9beff53573d
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
$ docker pull nats-streaming@sha256:a87972dc3059ea6664b8b58be08e426c79497d7ac25366e22a2d128239e94e5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7311545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab17242c3507f68896194a4ab65f92f9f98dd9c82d517bb1140b9f8660e13ae`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:31:22 GMT
COPY file:9bc2f7015ff72f7e91556a01075e89ef8a85a404228874028f7a356e8142e169 in /nats-streaming-server 
# Sat, 21 Oct 2023 00:31:22 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:22 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:31:22 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ee4a78724efc3390679e6118a2f2c5993c9075f378bd6a2f0b7f99b50579fb2b`  
		Last Modified: Wed, 21 Jun 2023 00:59:42 GMT  
		Size: 7.3 MB (7311545 bytes)  
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
$ docker pull nats-streaming@sha256:39e2025550e8c6ce15ff33eb51d4bbe0f3bee94abf9228d4c00b110d8cf8f122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee463d44f75f11b62539f48d51d34d166ae0a16a7aa08b56e946b3c5ec8c91`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:16:01 GMT
COPY file:8237d0d59fd3c6b32e52dbff50861a8848f846505c0303e7975e4a5f48ce8de9 in /nats-streaming-server 
# Sat, 21 Oct 2023 02:16:01 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:16:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:16:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c3b4c14668a8e32e87c6ea3dce4a99716b527ba7f0f4608cbab27184c89832ee`  
		Last Modified: Wed, 21 Jun 2023 01:12:24 GMT  
		Size: 7.0 MB (7011458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore`

```console
$ docker pull nats-streaming@sha256:54d5597f5252c7667f57e449d1ab34bed3d06f116660ef7fd9c074cd836ecb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:e70e08f4da3feaebc5b3ed23fc0b453063e4959f1a29364054e290bbbfae1718
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066136738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c52ee67415fd766abb836f51194fb89dea9acc4f5e29c89de79506403ed2e60`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 05:04:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:15:44 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:15:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Sat, 18 Nov 2023 02:15:46 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Sat, 18 Nov 2023 02:16:56 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Nov 2023 02:19:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 18 Nov 2023 02:19:02 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b0af12f04914a99bd0e5616b75c205f8a22c3c23bb3e13ea8fb557b765ec1`  
		Last Modified: Thu, 16 Nov 2023 05:11:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c88afdf8aa9af5173b3c8c128d4bcab7bbbfc61260c1a8a06caabf129202f`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b9c35daf71d710280381df335a3a73f13f7a49f2b050d0fd2e5a7e0ad70c43`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38aa9d9ac84d59b315d189635288cd861d2270b2e7084325252a6ce902127ab`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696922a5b3c732f5492bb89d8732890d4d9e9326827a11ed3c12078d6aaae41e`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 457.2 KB (457228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca1c650d4640e728726b56f2a343d6b4ed6fd7a5e8cf5f7d9be2f8e21c5364`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 8.2 MB (8236590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221495cf1fb3fe6d3d8a32fe845adb595d262f4755ad2d7bcb475a4bba2d430`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83b2bee4daa90dd6450149ac6839f54aaa3297bf58b3e87d204e0154e93c2d`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2520e3f1aa07523fb9e5b0f97f51acf5c7915f0d0f3433d63b89ed58b7e61dc`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:54d5597f5252c7667f57e449d1ab34bed3d06f116660ef7fd9c074cd836ecb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:e70e08f4da3feaebc5b3ed23fc0b453063e4959f1a29364054e290bbbfae1718
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066136738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c52ee67415fd766abb836f51194fb89dea9acc4f5e29c89de79506403ed2e60`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 05:04:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:15:44 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:15:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Sat, 18 Nov 2023 02:15:46 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Sat, 18 Nov 2023 02:16:56 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Nov 2023 02:19:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 18 Nov 2023 02:19:02 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b0af12f04914a99bd0e5616b75c205f8a22c3c23bb3e13ea8fb557b765ec1`  
		Last Modified: Thu, 16 Nov 2023 05:11:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c88afdf8aa9af5173b3c8c128d4bcab7bbbfc61260c1a8a06caabf129202f`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b9c35daf71d710280381df335a3a73f13f7a49f2b050d0fd2e5a7e0ad70c43`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38aa9d9ac84d59b315d189635288cd861d2270b2e7084325252a6ce902127ab`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696922a5b3c732f5492bb89d8732890d4d9e9326827a11ed3c12078d6aaae41e`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 457.2 KB (457228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca1c650d4640e728726b56f2a343d6b4ed6fd7a5e8cf5f7d9be2f8e21c5364`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 8.2 MB (8236590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221495cf1fb3fe6d3d8a32fe845adb595d262f4755ad2d7bcb475a4bba2d430`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83b2bee4daa90dd6450149ac6839f54aaa3297bf58b3e87d204e0154e93c2d`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2520e3f1aa07523fb9e5b0f97f51acf5c7915f0d0f3433d63b89ed58b7e61dc`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6`

```console
$ docker pull nats-streaming@sha256:92a71a07e1c9b0ae347dba4bf5c795c16c90a2079c38e044bcee4423a7ff768f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	windows version 10.0.17763.5122; amd64

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

### `nats-streaming:0.25.6` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine`

```console
$ docker pull nats-streaming@sha256:e108623d4dd5772547e46da6204f0989aadffe6497976c788f03b994942d3271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm variant v7

### `nats-streaming:0.25.6-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:5859c557b26b7a0fe2ac0ed1abcd28b65b7b4079c61c5676e571a24a29ccd672
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11467834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff243b212b0831f50bcd77a0491acbace8fab4b4f90e833beb96190a36956323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 02:28:36 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:28:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 02:28:38 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 02:28:38 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 02:28:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690158cab3634c349851670ded01f5084d40069dc81a2e9b2385ccdaf4270c84`  
		Last Modified: Sat, 18 Nov 2023 02:29:17 GMT  
		Size: 8.1 MB (8065445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeb121e6ed536362a47268822d991954a198aa42e5f02a89a127a507bb50540`  
		Last Modified: Sat, 18 Nov 2023 02:29:16 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b56622afee477c4e1c1f7644f71af82eac0d18a5b42323ccc2462512eb595aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10577650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f64236a48aac92e3e16bf95947467dbc7884e91f8dcde09be468e5ad0e2ca42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 01:57:31 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 01:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 01:57:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 01:57:34 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 01:57:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afe10cc0d63e3a6f9e87c371ba8152ff8d978964ee1dc901aca748ae26b8b2f`  
		Last Modified: Sat, 18 Nov 2023 01:58:06 GMT  
		Size: 7.7 MB (7677323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66aeb4d96d5dbd82f75f18b9691f89ce8e82ed9b2b5f6c5d7469a52a3561508`  
		Last Modified: Sat, 18 Nov 2023 01:58:05 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-alpine3.18`

```console
$ docker pull nats-streaming@sha256:e108623d4dd5772547e46da6204f0989aadffe6497976c788f03b994942d3271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm variant v7

### `nats-streaming:0.25.6-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:5859c557b26b7a0fe2ac0ed1abcd28b65b7b4079c61c5676e571a24a29ccd672
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11467834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff243b212b0831f50bcd77a0491acbace8fab4b4f90e833beb96190a36956323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 02:28:36 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:28:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 02:28:38 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 02:28:38 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 02:28:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690158cab3634c349851670ded01f5084d40069dc81a2e9b2385ccdaf4270c84`  
		Last Modified: Sat, 18 Nov 2023 02:29:17 GMT  
		Size: 8.1 MB (8065445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeb121e6ed536362a47268822d991954a198aa42e5f02a89a127a507bb50540`  
		Last Modified: Sat, 18 Nov 2023 02:29:16 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.6-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b56622afee477c4e1c1f7644f71af82eac0d18a5b42323ccc2462512eb595aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10577650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f64236a48aac92e3e16bf95947467dbc7884e91f8dcde09be468e5ad0e2ca42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 01:57:31 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 01:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 01:57:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 01:57:34 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 01:57:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afe10cc0d63e3a6f9e87c371ba8152ff8d978964ee1dc901aca748ae26b8b2f`  
		Last Modified: Sat, 18 Nov 2023 01:58:06 GMT  
		Size: 7.7 MB (7677323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66aeb4d96d5dbd82f75f18b9691f89ce8e82ed9b2b5f6c5d7469a52a3561508`  
		Last Modified: Sat, 18 Nov 2023 01:58:05 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-linux`

```console
$ docker pull nats-streaming@sha256:ca9e559b77c61e88216616a761be72ad5da8fbe207e1d4bfdf99126dfc0f2ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm variant v7

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

## `nats-streaming:0.25.6-nanoserver`

```console
$ docker pull nats-streaming@sha256:90a40c6c74be4457c8c4c2052c50a992b69ef298e20426a97f9246d42eef35c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25.6-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:90a40c6c74be4457c8c4c2052c50a992b69ef298e20426a97f9246d42eef35c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25.6-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-scratch`

```console
$ docker pull nats-streaming@sha256:ca9e559b77c61e88216616a761be72ad5da8fbe207e1d4bfdf99126dfc0f2ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm variant v7

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

## `nats-streaming:0.25.6-windowsservercore`

```console
$ docker pull nats-streaming@sha256:54d5597f5252c7667f57e449d1ab34bed3d06f116660ef7fd9c074cd836ecb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25.6-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:e70e08f4da3feaebc5b3ed23fc0b453063e4959f1a29364054e290bbbfae1718
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066136738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c52ee67415fd766abb836f51194fb89dea9acc4f5e29c89de79506403ed2e60`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 05:04:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:15:44 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:15:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Sat, 18 Nov 2023 02:15:46 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Sat, 18 Nov 2023 02:16:56 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Nov 2023 02:19:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 18 Nov 2023 02:19:02 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b0af12f04914a99bd0e5616b75c205f8a22c3c23bb3e13ea8fb557b765ec1`  
		Last Modified: Thu, 16 Nov 2023 05:11:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c88afdf8aa9af5173b3c8c128d4bcab7bbbfc61260c1a8a06caabf129202f`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b9c35daf71d710280381df335a3a73f13f7a49f2b050d0fd2e5a7e0ad70c43`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38aa9d9ac84d59b315d189635288cd861d2270b2e7084325252a6ce902127ab`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696922a5b3c732f5492bb89d8732890d4d9e9326827a11ed3c12078d6aaae41e`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 457.2 KB (457228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca1c650d4640e728726b56f2a343d6b4ed6fd7a5e8cf5f7d9be2f8e21c5364`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 8.2 MB (8236590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221495cf1fb3fe6d3d8a32fe845adb595d262f4755ad2d7bcb475a4bba2d430`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83b2bee4daa90dd6450149ac6839f54aaa3297bf58b3e87d204e0154e93c2d`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2520e3f1aa07523fb9e5b0f97f51acf5c7915f0d0f3433d63b89ed58b7e61dc`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.6-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:54d5597f5252c7667f57e449d1ab34bed3d06f116660ef7fd9c074cd836ecb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:0.25.6-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:e70e08f4da3feaebc5b3ed23fc0b453063e4959f1a29364054e290bbbfae1718
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066136738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c52ee67415fd766abb836f51194fb89dea9acc4f5e29c89de79506403ed2e60`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 05:04:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:15:44 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:15:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Sat, 18 Nov 2023 02:15:46 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Sat, 18 Nov 2023 02:16:56 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Nov 2023 02:19:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 18 Nov 2023 02:19:02 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b0af12f04914a99bd0e5616b75c205f8a22c3c23bb3e13ea8fb557b765ec1`  
		Last Modified: Thu, 16 Nov 2023 05:11:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c88afdf8aa9af5173b3c8c128d4bcab7bbbfc61260c1a8a06caabf129202f`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b9c35daf71d710280381df335a3a73f13f7a49f2b050d0fd2e5a7e0ad70c43`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38aa9d9ac84d59b315d189635288cd861d2270b2e7084325252a6ce902127ab`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696922a5b3c732f5492bb89d8732890d4d9e9326827a11ed3c12078d6aaae41e`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 457.2 KB (457228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca1c650d4640e728726b56f2a343d6b4ed6fd7a5e8cf5f7d9be2f8e21c5364`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 8.2 MB (8236590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221495cf1fb3fe6d3d8a32fe845adb595d262f4755ad2d7bcb475a4bba2d430`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83b2bee4daa90dd6450149ac6839f54aaa3297bf58b3e87d204e0154e93c2d`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2520e3f1aa07523fb9e5b0f97f51acf5c7915f0d0f3433d63b89ed58b7e61dc`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:446403cb2698594aa07d1df0990b2bd73e1b1a85a4c6b09a02dc76781486e6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:5859c557b26b7a0fe2ac0ed1abcd28b65b7b4079c61c5676e571a24a29ccd672
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11467834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff243b212b0831f50bcd77a0491acbace8fab4b4f90e833beb96190a36956323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 02:28:36 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:28:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 02:28:38 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 02:28:38 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 02:28:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690158cab3634c349851670ded01f5084d40069dc81a2e9b2385ccdaf4270c84`  
		Last Modified: Sat, 18 Nov 2023 02:29:17 GMT  
		Size: 8.1 MB (8065445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeb121e6ed536362a47268822d991954a198aa42e5f02a89a127a507bb50540`  
		Last Modified: Sat, 18 Nov 2023 02:29:16 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:123e1046c498e5fd86f61e61dd3b3682917c9accedb7d7774180c891601c1d09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10746016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd703820d68e38aa74550071c7f277c1a1647a0cde20da491bab952a2e0d341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:31:16 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:31:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:31:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:31:19 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:31:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f819de770d62324a67c19c681691204f02bd8de83d0d009b92714abfea616`  
		Last Modified: Sat, 21 Oct 2023 00:31:36 GMT  
		Size: 7.6 MB (7600300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4eccbe16f8571a693b997c0f54a8c9f8d081559dca4a246f0035908ceee5e1`  
		Last Modified: Sat, 21 Oct 2023 00:31:35 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b56622afee477c4e1c1f7644f71af82eac0d18a5b42323ccc2462512eb595aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10577650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f64236a48aac92e3e16bf95947467dbc7884e91f8dcde09be468e5ad0e2ca42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 01:57:31 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 01:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 01:57:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 01:57:34 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 01:57:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afe10cc0d63e3a6f9e87c371ba8152ff8d978964ee1dc901aca748ae26b8b2f`  
		Last Modified: Sat, 18 Nov 2023 01:58:06 GMT  
		Size: 7.7 MB (7677323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66aeb4d96d5dbd82f75f18b9691f89ce8e82ed9b2b5f6c5d7469a52a3561508`  
		Last Modified: Sat, 18 Nov 2023 01:58:05 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:690162b6622a5bb198bde138afc9191ec7c05b953a3d901bd26102f616e1e3cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10632371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b037ffd8b7268a4c1bc628d638199f10ba54bb901751616d66703b30c81da1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:15:54 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:15:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:15:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:15:57 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:15:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a86dd6d8430110c1d880bd46dc6c42418e7269d8140aa3e58dc795d4ecfc03`  
		Last Modified: Sat, 21 Oct 2023 02:16:14 GMT  
		Size: 7.3 MB (7300119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416d20af0c6435894ca9435014dd34f1e4f86db1cd813b20dc3e0a2f493796dd`  
		Last Modified: Sat, 21 Oct 2023 02:16:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.18`

```console
$ docker pull nats-streaming@sha256:446403cb2698594aa07d1df0990b2bd73e1b1a85a4c6b09a02dc76781486e6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:5859c557b26b7a0fe2ac0ed1abcd28b65b7b4079c61c5676e571a24a29ccd672
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11467834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff243b212b0831f50bcd77a0491acbace8fab4b4f90e833beb96190a36956323`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 02:28:36 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:28:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 02:28:38 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 02:28:38 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 02:28:38 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690158cab3634c349851670ded01f5084d40069dc81a2e9b2385ccdaf4270c84`  
		Last Modified: Sat, 18 Nov 2023 02:29:17 GMT  
		Size: 8.1 MB (8065445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeb121e6ed536362a47268822d991954a198aa42e5f02a89a127a507bb50540`  
		Last Modified: Sat, 18 Nov 2023 02:29:16 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:123e1046c498e5fd86f61e61dd3b3682917c9accedb7d7774180c891601c1d09
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10746016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd703820d68e38aa74550071c7f277c1a1647a0cde20da491bab952a2e0d341`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:31:16 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:31:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:31:19 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:31:19 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:31:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99f819de770d62324a67c19c681691204f02bd8de83d0d009b92714abfea616`  
		Last Modified: Sat, 21 Oct 2023 00:31:36 GMT  
		Size: 7.6 MB (7600300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4eccbe16f8571a693b997c0f54a8c9f8d081559dca4a246f0035908ceee5e1`  
		Last Modified: Sat, 21 Oct 2023 00:31:35 GMT  
		Size: 425.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b56622afee477c4e1c1f7644f71af82eac0d18a5b42323ccc2462512eb595aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10577650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f64236a48aac92e3e16bf95947467dbc7884e91f8dcde09be468e5ad0e2ca42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 18 Nov 2023 01:57:31 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 01:57:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='caf2839d14c610d9d62afeb9022ee36aa4ff5adc86d0402bb7e1a5d7f5e7d26f' ;; 		armhf) natsArch='arm6'; sha256='afe4cad7cbd39c029c1a8286099c635e174cc04494dde27595e3ae461e9c187a' ;; 		armv7) natsArch='arm7'; sha256='0264455a2c028e2828d517070bb06837206a70702bfba66656406bc9d750c282' ;; 		x86_64) natsArch='amd64'; sha256='10f25b100a5b9a7389882883259790d599b557a16ddde1accdfcf9361e19b2f9' ;; 		x86) natsArch='386'; sha256='796d25d9411e42c7f183950ad109b1918e039236960919cb22d57748b329cae0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 18 Nov 2023 01:57:34 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 18 Nov 2023 01:57:34 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 01:57:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Nov 2023 01:57:34 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afe10cc0d63e3a6f9e87c371ba8152ff8d978964ee1dc901aca748ae26b8b2f`  
		Last Modified: Sat, 18 Nov 2023 01:58:06 GMT  
		Size: 7.7 MB (7677323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66aeb4d96d5dbd82f75f18b9691f89ce8e82ed9b2b5f6c5d7469a52a3561508`  
		Last Modified: Sat, 18 Nov 2023 01:58:05 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:690162b6622a5bb198bde138afc9191ec7c05b953a3d901bd26102f616e1e3cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10632371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b037ffd8b7268a4c1bc628d638199f10ba54bb901751616d66703b30c81da1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:15:54 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:15:57 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:15:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:15:57 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:15:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a86dd6d8430110c1d880bd46dc6c42418e7269d8140aa3e58dc795d4ecfc03`  
		Last Modified: Sat, 21 Oct 2023 02:16:14 GMT  
		Size: 7.3 MB (7300119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416d20af0c6435894ca9435014dd34f1e4f86db1cd813b20dc3e0a2f493796dd`  
		Last Modified: Sat, 21 Oct 2023 02:16:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:48e7eebc23a4c3fcb78b435c669ba42b495fc874ae9b0620524a38cf0e819f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.5122; amd64

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
$ docker pull nats-streaming@sha256:a87972dc3059ea6664b8b58be08e426c79497d7ac25366e22a2d128239e94e5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7311545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab17242c3507f68896194a4ab65f92f9f98dd9c82d517bb1140b9f8660e13ae`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:31:22 GMT
COPY file:9bc2f7015ff72f7e91556a01075e89ef8a85a404228874028f7a356e8142e169 in /nats-streaming-server 
# Sat, 21 Oct 2023 00:31:22 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:22 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:31:22 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ee4a78724efc3390679e6118a2f2c5993c9075f378bd6a2f0b7f99b50579fb2b`  
		Last Modified: Wed, 21 Jun 2023 00:59:42 GMT  
		Size: 7.3 MB (7311545 bytes)  
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
$ docker pull nats-streaming@sha256:39e2025550e8c6ce15ff33eb51d4bbe0f3bee94abf9228d4c00b110d8cf8f122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee463d44f75f11b62539f48d51d34d166ae0a16a7aa08b56e946b3c5ec8c91`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:16:01 GMT
COPY file:8237d0d59fd3c6b32e52dbff50861a8848f846505c0303e7975e4a5f48ce8de9 in /nats-streaming-server 
# Sat, 21 Oct 2023 02:16:01 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:16:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:16:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c3b4c14668a8e32e87c6ea3dce4a99716b527ba7f0f4608cbab27184c89832ee`  
		Last Modified: Wed, 21 Jun 2023 01:12:24 GMT  
		Size: 7.0 MB (7011458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:3b03df6f4f365e45ce2ff7700d817788549e41ef5106635bc8f3d9beff53573d
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
$ docker pull nats-streaming@sha256:a87972dc3059ea6664b8b58be08e426c79497d7ac25366e22a2d128239e94e5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7311545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab17242c3507f68896194a4ab65f92f9f98dd9c82d517bb1140b9f8660e13ae`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:31:22 GMT
COPY file:9bc2f7015ff72f7e91556a01075e89ef8a85a404228874028f7a356e8142e169 in /nats-streaming-server 
# Sat, 21 Oct 2023 00:31:22 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:22 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:31:22 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ee4a78724efc3390679e6118a2f2c5993c9075f378bd6a2f0b7f99b50579fb2b`  
		Last Modified: Wed, 21 Jun 2023 00:59:42 GMT  
		Size: 7.3 MB (7311545 bytes)  
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
$ docker pull nats-streaming@sha256:39e2025550e8c6ce15ff33eb51d4bbe0f3bee94abf9228d4c00b110d8cf8f122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee463d44f75f11b62539f48d51d34d166ae0a16a7aa08b56e946b3c5ec8c91`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:16:01 GMT
COPY file:8237d0d59fd3c6b32e52dbff50861a8848f846505c0303e7975e4a5f48ce8de9 in /nats-streaming-server 
# Sat, 21 Oct 2023 02:16:01 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:16:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:16:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c3b4c14668a8e32e87c6ea3dce4a99716b527ba7f0f4608cbab27184c89832ee`  
		Last Modified: Wed, 21 Jun 2023 01:12:24 GMT  
		Size: 7.0 MB (7011458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:90a40c6c74be4457c8c4c2052c50a992b69ef298e20426a97f9246d42eef35c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:90a40c6c74be4457c8c4c2052c50a992b69ef298e20426a97f9246d42eef35c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:62055a1ec937db681b3d982e936b10282bd3d8b03c5e912946038c31eba4f334
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.4 MB (112441938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db62e11729b935964a0936f688f7c65f47774a0a4587bf664bb5857eb47abe57`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 05:07:37 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:19:12 GMT
RUN cmd /S /C #(nop) COPY file:10633c354e10815674f36bf0c5a1fa1b02d5a27ab4c71370a1de64aba09dd3dd in C:\nats-streaming-server.exe 
# Sat, 18 Nov 2023 02:19:13 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:14 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:15 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6482f23797692e3cc4e6739a9923a136f784b599c3f22a9d2ecb0570cdda33fa`  
		Last Modified: Thu, 16 Nov 2023 05:12:04 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ee4f60c8b850e8321d53250cf161a304bb8f1629eb69b3dd43df4dc9cc21df`  
		Last Modified: Sat, 18 Nov 2023 02:19:57 GMT  
		Size: 7.9 MB (7939869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b44f94a1a9f7b814d7137fd4fd5e4b3eed6e9049487b72886fb95aa066d76c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3121013cc33bf72ae1c5798c30f463750db5cef9ae2d3b90498750efa1321a32`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d13248cf66f85635dc7408113dca2374e6da3fa2d86b000247fa8832f1b16c`  
		Last Modified: Sat, 18 Nov 2023 02:19:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:3b03df6f4f365e45ce2ff7700d817788549e41ef5106635bc8f3d9beff53573d
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
$ docker pull nats-streaming@sha256:a87972dc3059ea6664b8b58be08e426c79497d7ac25366e22a2d128239e94e5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7311545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab17242c3507f68896194a4ab65f92f9f98dd9c82d517bb1140b9f8660e13ae`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:31:22 GMT
COPY file:9bc2f7015ff72f7e91556a01075e89ef8a85a404228874028f7a356e8142e169 in /nats-streaming-server 
# Sat, 21 Oct 2023 00:31:22 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:31:22 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:31:22 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:ee4a78724efc3390679e6118a2f2c5993c9075f378bd6a2f0b7f99b50579fb2b`  
		Last Modified: Wed, 21 Jun 2023 00:59:42 GMT  
		Size: 7.3 MB (7311545 bytes)  
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
$ docker pull nats-streaming@sha256:39e2025550e8c6ce15ff33eb51d4bbe0f3bee94abf9228d4c00b110d8cf8f122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7011458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ee463d44f75f11b62539f48d51d34d166ae0a16a7aa08b56e946b3c5ec8c91`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:16:01 GMT
COPY file:8237d0d59fd3c6b32e52dbff50861a8848f846505c0303e7975e4a5f48ce8de9 in /nats-streaming-server 
# Sat, 21 Oct 2023 02:16:01 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:16:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:16:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c3b4c14668a8e32e87c6ea3dce4a99716b527ba7f0f4608cbab27184c89832ee`  
		Last Modified: Wed, 21 Jun 2023 01:12:24 GMT  
		Size: 7.0 MB (7011458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:54d5597f5252c7667f57e449d1ab34bed3d06f116660ef7fd9c074cd836ecb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:e70e08f4da3feaebc5b3ed23fc0b453063e4959f1a29364054e290bbbfae1718
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066136738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c52ee67415fd766abb836f51194fb89dea9acc4f5e29c89de79506403ed2e60`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 05:04:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:15:44 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:15:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Sat, 18 Nov 2023 02:15:46 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Sat, 18 Nov 2023 02:16:56 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Nov 2023 02:19:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 18 Nov 2023 02:19:02 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b0af12f04914a99bd0e5616b75c205f8a22c3c23bb3e13ea8fb557b765ec1`  
		Last Modified: Thu, 16 Nov 2023 05:11:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c88afdf8aa9af5173b3c8c128d4bcab7bbbfc61260c1a8a06caabf129202f`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b9c35daf71d710280381df335a3a73f13f7a49f2b050d0fd2e5a7e0ad70c43`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38aa9d9ac84d59b315d189635288cd861d2270b2e7084325252a6ce902127ab`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696922a5b3c732f5492bb89d8732890d4d9e9326827a11ed3c12078d6aaae41e`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 457.2 KB (457228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca1c650d4640e728726b56f2a343d6b4ed6fd7a5e8cf5f7d9be2f8e21c5364`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 8.2 MB (8236590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221495cf1fb3fe6d3d8a32fe845adb595d262f4755ad2d7bcb475a4bba2d430`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83b2bee4daa90dd6450149ac6839f54aaa3297bf58b3e87d204e0154e93c2d`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2520e3f1aa07523fb9e5b0f97f51acf5c7915f0d0f3433d63b89ed58b7e61dc`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:54d5597f5252c7667f57e449d1ab34bed3d06f116660ef7fd9c074cd836ecb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull nats-streaming@sha256:e70e08f4da3feaebc5b3ed23fc0b453063e4959f1a29364054e290bbbfae1718
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2066136738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c52ee67415fd766abb836f51194fb89dea9acc4f5e29c89de79506403ed2e60`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 05:04:35 GMT
ENV NATS_DOCKERIZED=1
# Sat, 18 Nov 2023 02:15:44 GMT
ENV NATS_STREAMING_SERVER=0.25.6
# Sat, 18 Nov 2023 02:15:45 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.6/nats-streaming-server-v0.25.6-windows-amd64.zip
# Sat, 18 Nov 2023 02:15:46 GMT
ENV NATS_STREAMING_SERVER_SHASUM=41be7de372eea07f0923420c525336eaf311ab9f9878d8823cf7b69c74da5351
# Sat, 18 Nov 2023 02:16:56 GMT
RUN Set-PSDebug -Trace 2
# Sat, 18 Nov 2023 02:19:01 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Sat, 18 Nov 2023 02:19:02 GMT
EXPOSE 4222 8222
# Sat, 18 Nov 2023 02:19:03 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Sat, 18 Nov 2023 02:19:04 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e18b0af12f04914a99bd0e5616b75c205f8a22c3c23bb3e13ea8fb557b765ec1`  
		Last Modified: Thu, 16 Nov 2023 05:11:46 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2c88afdf8aa9af5173b3c8c128d4bcab7bbbfc61260c1a8a06caabf129202f`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b9c35daf71d710280381df335a3a73f13f7a49f2b050d0fd2e5a7e0ad70c43`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38aa9d9ac84d59b315d189635288cd861d2270b2e7084325252a6ce902127ab`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696922a5b3c732f5492bb89d8732890d4d9e9326827a11ed3c12078d6aaae41e`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 457.2 KB (457228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ca1c650d4640e728726b56f2a343d6b4ed6fd7a5e8cf5f7d9be2f8e21c5364`  
		Last Modified: Sat, 18 Nov 2023 02:19:42 GMT  
		Size: 8.2 MB (8236590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9221495cf1fb3fe6d3d8a32fe845adb595d262f4755ad2d7bcb475a4bba2d430`  
		Last Modified: Sat, 18 Nov 2023 02:19:41 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83b2bee4daa90dd6450149ac6839f54aaa3297bf58b3e87d204e0154e93c2d`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2520e3f1aa07523fb9e5b0f97f51acf5c7915f0d0f3433d63b89ed58b7e61dc`  
		Last Modified: Sat, 18 Nov 2023 02:19:40 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
