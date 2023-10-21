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
-	[`nats-streaming:0.25.5`](#nats-streaming0255)
-	[`nats-streaming:0.25.5-alpine`](#nats-streaming0255-alpine)
-	[`nats-streaming:0.25.5-alpine3.18`](#nats-streaming0255-alpine318)
-	[`nats-streaming:0.25.5-linux`](#nats-streaming0255-linux)
-	[`nats-streaming:0.25.5-nanoserver`](#nats-streaming0255-nanoserver)
-	[`nats-streaming:0.25.5-nanoserver-1809`](#nats-streaming0255-nanoserver-1809)
-	[`nats-streaming:0.25.5-scratch`](#nats-streaming0255-scratch)
-	[`nats-streaming:0.25.5-windowsservercore`](#nats-streaming0255-windowsservercore)
-	[`nats-streaming:0.25.5-windowsservercore-1809`](#nats-streaming0255-windowsservercore-1809)
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
$ docker pull nats-streaming@sha256:030bf2dd73eac06ff3da645f64c39759268568e6436ce85a61b56da93060a96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
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
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
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

### `nats-streaming:0.25` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:a84199889b9444aa2603c2d5d058c4bd71b0e507c32cfc30c795e0dfe898d646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:de419b7997eac65efd3c69eca61900cbea2360650384e6d9cdaab78293e44386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11348072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ffcfbe9209faf99efdf3c2ee984c6ab372cda6041bbbe875b34e128150962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:41:34 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:41:36 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:41:36 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:41:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03db809068feb487c808151d8744b43434119b95b9c1b8ac4ad777b87015dff`  
		Last Modified: Sat, 21 Oct 2023 02:41:59 GMT  
		Size: 7.9 MB (7945683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f357f72bbb66966a9a66b3687b61fce540b7000f2c1627cb41706563cc7c7`  
		Last Modified: Sat, 21 Oct 2023 02:41:58 GMT  
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
$ docker pull nats-streaming@sha256:b97a488869be5065f218d4742e6514a894c10a58bd1c724056304affdc9fd1fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1a77fe316c388b3888a1e6bc2dbc42d2e107246b223dd518187f7043f8eeea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:55:15 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:55:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:55:18 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:55:18 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:55:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f5dcb09a4588deb1baa2877e03030901f33a5f4ef4650424c36476cebd0c`  
		Last Modified: Sat, 21 Oct 2023 00:55:37 GMT  
		Size: 7.6 MB (7588102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64863620b98334bd938d8926906884d8110812691a985226190f7dd7ba394bf7`  
		Last Modified: Sat, 21 Oct 2023 00:55:36 GMT  
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
$ docker pull nats-streaming@sha256:a84199889b9444aa2603c2d5d058c4bd71b0e507c32cfc30c795e0dfe898d646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:de419b7997eac65efd3c69eca61900cbea2360650384e6d9cdaab78293e44386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11348072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ffcfbe9209faf99efdf3c2ee984c6ab372cda6041bbbe875b34e128150962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:41:34 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:41:36 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:41:36 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:41:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03db809068feb487c808151d8744b43434119b95b9c1b8ac4ad777b87015dff`  
		Last Modified: Sat, 21 Oct 2023 02:41:59 GMT  
		Size: 7.9 MB (7945683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f357f72bbb66966a9a66b3687b61fce540b7000f2c1627cb41706563cc7c7`  
		Last Modified: Sat, 21 Oct 2023 02:41:58 GMT  
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
$ docker pull nats-streaming@sha256:b97a488869be5065f218d4742e6514a894c10a58bd1c724056304affdc9fd1fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1a77fe316c388b3888a1e6bc2dbc42d2e107246b223dd518187f7043f8eeea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:55:15 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:55:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:55:18 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:55:18 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:55:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f5dcb09a4588deb1baa2877e03030901f33a5f4ef4650424c36476cebd0c`  
		Last Modified: Sat, 21 Oct 2023 00:55:37 GMT  
		Size: 7.6 MB (7588102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64863620b98334bd938d8926906884d8110812691a985226190f7dd7ba394bf7`  
		Last Modified: Sat, 21 Oct 2023 00:55:36 GMT  
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
$ docker pull nats-streaming@sha256:556ba52cac20d3ac56a9e0a25227feaab2f9dcaf11a226faaeda151db2c46f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
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
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
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
$ docker pull nats-streaming@sha256:f3fa9bfcd019cde80a83f2a8e2f9e1e985b7c37692940a245be4adee5f0b17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:f3fa9bfcd019cde80a83f2a8e2f9e1e985b7c37692940a245be4adee5f0b17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:556ba52cac20d3ac56a9e0a25227feaab2f9dcaf11a226faaeda151db2c46f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
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
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
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
$ docker pull nats-streaming@sha256:a6d657e66afa846325fb726a3f8587f246c08c5e8a9f960defd40740326165ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:4eb649beae9ce26c6ccf0f0dbd3c3e198983dd2c23ff75af13eb3456388c52c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040135445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40986464eb49491748626500020ee674f8d14939636bf5719837a93fb7d67c87`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:42:17 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Wed, 11 Oct 2023 03:42:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.5/nats-streaming-server-v0.25.5-windows-amd64.zip
# Wed, 11 Oct 2023 03:42:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=709b481bfa3537dc7941490365e065554f19c7029830d765ef49e8cd16657b75
# Wed, 11 Oct 2023 03:43:58 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Oct 2023 03:46:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Oct 2023 03:46:31 GMT
EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f30b1f53ee1616f24332acf6cdcca95e017a8ba32e308605859877b9ed83c`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb77616131a4292e9336a73c3285b758675cccf268367732e95f68d705bcba`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a926a9c704cce075dcda274fd7979538a59de5fb16df6eb1b1ec8fc1de42fd07`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02713c5d92e8c7136d3ce18a3eb90deda51b81323e65a7f13f48bc665e154f`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 443.6 KB (443570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda3c2b906ebceedb516bcca46cdf2e1cb8c5dae6c8d9e1eab434c1b1782c761`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 8.1 MB (8089974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a521779f3391f596ac25e9b136ea30296ebb050951a2acbae3f25e65aaed67`  
		Last Modified: Wed, 11 Oct 2023 03:47:10 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d1809820a3e752c85d4a50b42b8287f119da9d82d6a6989374ae4e038348e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9560dcf383eab30612cff911b05b7eebfae68baaae360a3439512b15b86f5`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:a6d657e66afa846325fb726a3f8587f246c08c5e8a9f960defd40740326165ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:4eb649beae9ce26c6ccf0f0dbd3c3e198983dd2c23ff75af13eb3456388c52c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040135445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40986464eb49491748626500020ee674f8d14939636bf5719837a93fb7d67c87`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:42:17 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Wed, 11 Oct 2023 03:42:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.5/nats-streaming-server-v0.25.5-windows-amd64.zip
# Wed, 11 Oct 2023 03:42:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=709b481bfa3537dc7941490365e065554f19c7029830d765ef49e8cd16657b75
# Wed, 11 Oct 2023 03:43:58 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Oct 2023 03:46:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Oct 2023 03:46:31 GMT
EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f30b1f53ee1616f24332acf6cdcca95e017a8ba32e308605859877b9ed83c`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb77616131a4292e9336a73c3285b758675cccf268367732e95f68d705bcba`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a926a9c704cce075dcda274fd7979538a59de5fb16df6eb1b1ec8fc1de42fd07`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02713c5d92e8c7136d3ce18a3eb90deda51b81323e65a7f13f48bc665e154f`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 443.6 KB (443570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda3c2b906ebceedb516bcca46cdf2e1cb8c5dae6c8d9e1eab434c1b1782c761`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 8.1 MB (8089974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a521779f3391f596ac25e9b136ea30296ebb050951a2acbae3f25e65aaed67`  
		Last Modified: Wed, 11 Oct 2023 03:47:10 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d1809820a3e752c85d4a50b42b8287f119da9d82d6a6989374ae4e038348e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9560dcf383eab30612cff911b05b7eebfae68baaae360a3439512b15b86f5`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.5`

```console
$ docker pull nats-streaming@sha256:030bf2dd73eac06ff3da645f64c39759268568e6436ce85a61b56da93060a96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25.5` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5` - linux; arm variant v6

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

### `nats-streaming:0.25.5` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5` - linux; arm64 variant v8

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

### `nats-streaming:0.25.5` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.5-alpine`

```console
$ docker pull nats-streaming@sha256:a84199889b9444aa2603c2d5d058c4bd71b0e507c32cfc30c795e0dfe898d646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.5-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:de419b7997eac65efd3c69eca61900cbea2360650384e6d9cdaab78293e44386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11348072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ffcfbe9209faf99efdf3c2ee984c6ab372cda6041bbbe875b34e128150962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:41:34 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:41:36 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:41:36 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:41:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03db809068feb487c808151d8744b43434119b95b9c1b8ac4ad777b87015dff`  
		Last Modified: Sat, 21 Oct 2023 02:41:59 GMT  
		Size: 7.9 MB (7945683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f357f72bbb66966a9a66b3687b61fce540b7000f2c1627cb41706563cc7c7`  
		Last Modified: Sat, 21 Oct 2023 02:41:58 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-alpine` - linux; arm variant v6

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

### `nats-streaming:0.25.5-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b97a488869be5065f218d4742e6514a894c10a58bd1c724056304affdc9fd1fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1a77fe316c388b3888a1e6bc2dbc42d2e107246b223dd518187f7043f8eeea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:55:15 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:55:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:55:18 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:55:18 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:55:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f5dcb09a4588deb1baa2877e03030901f33a5f4ef4650424c36476cebd0c`  
		Last Modified: Sat, 21 Oct 2023 00:55:37 GMT  
		Size: 7.6 MB (7588102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64863620b98334bd938d8926906884d8110812691a985226190f7dd7ba394bf7`  
		Last Modified: Sat, 21 Oct 2023 00:55:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-alpine` - linux; arm64 variant v8

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

## `nats-streaming:0.25.5-alpine3.18`

```console
$ docker pull nats-streaming@sha256:a84199889b9444aa2603c2d5d058c4bd71b0e507c32cfc30c795e0dfe898d646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.5-alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:de419b7997eac65efd3c69eca61900cbea2360650384e6d9cdaab78293e44386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11348072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ffcfbe9209faf99efdf3c2ee984c6ab372cda6041bbbe875b34e128150962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:41:34 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:41:36 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:41:36 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:41:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03db809068feb487c808151d8744b43434119b95b9c1b8ac4ad777b87015dff`  
		Last Modified: Sat, 21 Oct 2023 02:41:59 GMT  
		Size: 7.9 MB (7945683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f357f72bbb66966a9a66b3687b61fce540b7000f2c1627cb41706563cc7c7`  
		Last Modified: Sat, 21 Oct 2023 02:41:58 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-alpine3.18` - linux; arm variant v6

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

### `nats-streaming:0.25.5-alpine3.18` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:b97a488869be5065f218d4742e6514a894c10a58bd1c724056304affdc9fd1fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1a77fe316c388b3888a1e6bc2dbc42d2e107246b223dd518187f7043f8eeea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:55:15 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:55:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:55:18 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:55:18 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:55:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f5dcb09a4588deb1baa2877e03030901f33a5f4ef4650424c36476cebd0c`  
		Last Modified: Sat, 21 Oct 2023 00:55:37 GMT  
		Size: 7.6 MB (7588102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64863620b98334bd938d8926906884d8110812691a985226190f7dd7ba394bf7`  
		Last Modified: Sat, 21 Oct 2023 00:55:36 GMT  
		Size: 422.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-alpine3.18` - linux; arm64 variant v8

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

## `nats-streaming:0.25.5-linux`

```console
$ docker pull nats-streaming@sha256:556ba52cac20d3ac56a9e0a25227feaab2f9dcaf11a226faaeda151db2c46f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.5-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-linux` - linux; arm variant v6

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

### `nats-streaming:0.25.5-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-linux` - linux; arm64 variant v8

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

## `nats-streaming:0.25.5-nanoserver`

```console
$ docker pull nats-streaming@sha256:f3fa9bfcd019cde80a83f2a8e2f9e1e985b7c37692940a245be4adee5f0b17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25.5-nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.5-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:f3fa9bfcd019cde80a83f2a8e2f9e1e985b7c37692940a245be4adee5f0b17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25.5-nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.5-scratch`

```console
$ docker pull nats-streaming@sha256:556ba52cac20d3ac56a9e0a25227feaab2f9dcaf11a226faaeda151db2c46f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.5-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-scratch` - linux; arm variant v6

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

### `nats-streaming:0.25.5-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.5-scratch` - linux; arm64 variant v8

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

## `nats-streaming:0.25.5-windowsservercore`

```console
$ docker pull nats-streaming@sha256:a6d657e66afa846325fb726a3f8587f246c08c5e8a9f960defd40740326165ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25.5-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:4eb649beae9ce26c6ccf0f0dbd3c3e198983dd2c23ff75af13eb3456388c52c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040135445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40986464eb49491748626500020ee674f8d14939636bf5719837a93fb7d67c87`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:42:17 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Wed, 11 Oct 2023 03:42:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.5/nats-streaming-server-v0.25.5-windows-amd64.zip
# Wed, 11 Oct 2023 03:42:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=709b481bfa3537dc7941490365e065554f19c7029830d765ef49e8cd16657b75
# Wed, 11 Oct 2023 03:43:58 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Oct 2023 03:46:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Oct 2023 03:46:31 GMT
EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f30b1f53ee1616f24332acf6cdcca95e017a8ba32e308605859877b9ed83c`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb77616131a4292e9336a73c3285b758675cccf268367732e95f68d705bcba`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a926a9c704cce075dcda274fd7979538a59de5fb16df6eb1b1ec8fc1de42fd07`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02713c5d92e8c7136d3ce18a3eb90deda51b81323e65a7f13f48bc665e154f`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 443.6 KB (443570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda3c2b906ebceedb516bcca46cdf2e1cb8c5dae6c8d9e1eab434c1b1782c761`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 8.1 MB (8089974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a521779f3391f596ac25e9b136ea30296ebb050951a2acbae3f25e65aaed67`  
		Last Modified: Wed, 11 Oct 2023 03:47:10 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d1809820a3e752c85d4a50b42b8287f119da9d82d6a6989374ae4e038348e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9560dcf383eab30612cff911b05b7eebfae68baaae360a3439512b15b86f5`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.5-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:a6d657e66afa846325fb726a3f8587f246c08c5e8a9f960defd40740326165ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:0.25.5-windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:4eb649beae9ce26c6ccf0f0dbd3c3e198983dd2c23ff75af13eb3456388c52c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040135445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40986464eb49491748626500020ee674f8d14939636bf5719837a93fb7d67c87`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:42:17 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Wed, 11 Oct 2023 03:42:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.5/nats-streaming-server-v0.25.5-windows-amd64.zip
# Wed, 11 Oct 2023 03:42:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=709b481bfa3537dc7941490365e065554f19c7029830d765ef49e8cd16657b75
# Wed, 11 Oct 2023 03:43:58 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Oct 2023 03:46:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Oct 2023 03:46:31 GMT
EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f30b1f53ee1616f24332acf6cdcca95e017a8ba32e308605859877b9ed83c`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb77616131a4292e9336a73c3285b758675cccf268367732e95f68d705bcba`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a926a9c704cce075dcda274fd7979538a59de5fb16df6eb1b1ec8fc1de42fd07`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02713c5d92e8c7136d3ce18a3eb90deda51b81323e65a7f13f48bc665e154f`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 443.6 KB (443570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda3c2b906ebceedb516bcca46cdf2e1cb8c5dae6c8d9e1eab434c1b1782c761`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 8.1 MB (8089974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a521779f3391f596ac25e9b136ea30296ebb050951a2acbae3f25e65aaed67`  
		Last Modified: Wed, 11 Oct 2023 03:47:10 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d1809820a3e752c85d4a50b42b8287f119da9d82d6a6989374ae4e038348e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9560dcf383eab30612cff911b05b7eebfae68baaae360a3439512b15b86f5`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:a84199889b9444aa2603c2d5d058c4bd71b0e507c32cfc30c795e0dfe898d646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:de419b7997eac65efd3c69eca61900cbea2360650384e6d9cdaab78293e44386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11348072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ffcfbe9209faf99efdf3c2ee984c6ab372cda6041bbbe875b34e128150962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:41:34 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:41:36 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:41:36 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:41:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03db809068feb487c808151d8744b43434119b95b9c1b8ac4ad777b87015dff`  
		Last Modified: Sat, 21 Oct 2023 02:41:59 GMT  
		Size: 7.9 MB (7945683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f357f72bbb66966a9a66b3687b61fce540b7000f2c1627cb41706563cc7c7`  
		Last Modified: Sat, 21 Oct 2023 02:41:58 GMT  
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
$ docker pull nats-streaming@sha256:b97a488869be5065f218d4742e6514a894c10a58bd1c724056304affdc9fd1fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1a77fe316c388b3888a1e6bc2dbc42d2e107246b223dd518187f7043f8eeea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:55:15 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:55:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:55:18 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:55:18 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:55:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f5dcb09a4588deb1baa2877e03030901f33a5f4ef4650424c36476cebd0c`  
		Last Modified: Sat, 21 Oct 2023 00:55:37 GMT  
		Size: 7.6 MB (7588102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64863620b98334bd938d8926906884d8110812691a985226190f7dd7ba394bf7`  
		Last Modified: Sat, 21 Oct 2023 00:55:36 GMT  
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
$ docker pull nats-streaming@sha256:a84199889b9444aa2603c2d5d058c4bd71b0e507c32cfc30c795e0dfe898d646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.18` - linux; amd64

```console
$ docker pull nats-streaming@sha256:de419b7997eac65efd3c69eca61900cbea2360650384e6d9cdaab78293e44386
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11348072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01ffcfbe9209faf99efdf3c2ee984c6ab372cda6041bbbe875b34e128150962`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:41:34 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 02:41:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 02:41:36 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 02:41:36 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 02:41:37 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03db809068feb487c808151d8744b43434119b95b9c1b8ac4ad777b87015dff`  
		Last Modified: Sat, 21 Oct 2023 02:41:59 GMT  
		Size: 7.9 MB (7945683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33f357f72bbb66966a9a66b3687b61fce540b7000f2c1627cb41706563cc7c7`  
		Last Modified: Sat, 21 Oct 2023 02:41:58 GMT  
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
$ docker pull nats-streaming@sha256:b97a488869be5065f218d4742e6514a894c10a58bd1c724056304affdc9fd1fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10488429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1a77fe316c388b3888a1e6bc2dbc42d2e107246b223dd518187f7043f8eeea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:55:15 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Sat, 21 Oct 2023 00:55:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='937af3f9cdbfe3cb4648cf8c8f505dded2cc175d59ba10e13ec71d1c04e61bf2' ;; 		armhf) natsArch='arm6'; sha256='5bd3a0456054505741b05e5d03acb9f7a5de97cf3ea20cd52d31edbae1c387ea' ;; 		armv7) natsArch='arm7'; sha256='0e643e9881cf3acf3313f84853451d1c4a1e731bc8599d223a40042f9c0c7285' ;; 		x86_64) natsArch='amd64'; sha256='22762f4d0ccfc75947096a14e09566b816113e125a3d39f7914a0c332bee25a7' ;; 		x86) natsArch='386'; sha256='92d8d4460f538883c78e67a334b23b2317e4fe58d46e4fdbbef8b4c09c7b97ae' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Sat, 21 Oct 2023 00:55:18 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Sat, 21 Oct 2023 00:55:18 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 21 Oct 2023 00:55:18 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17f5dcb09a4588deb1baa2877e03030901f33a5f4ef4650424c36476cebd0c`  
		Last Modified: Sat, 21 Oct 2023 00:55:37 GMT  
		Size: 7.6 MB (7588102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64863620b98334bd938d8926906884d8110812691a985226190f7dd7ba394bf7`  
		Last Modified: Sat, 21 Oct 2023 00:55:36 GMT  
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
$ docker pull nats-streaming@sha256:030bf2dd73eac06ff3da645f64c39759268568e6436ce85a61b56da93060a96b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
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
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
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

### `nats-streaming:latest` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:556ba52cac20d3ac56a9e0a25227feaab2f9dcaf11a226faaeda151db2c46f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
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
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
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
$ docker pull nats-streaming@sha256:f3fa9bfcd019cde80a83f2a8e2f9e1e985b7c37692940a245be4adee5f0b17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:f3fa9bfcd019cde80a83f2a8e2f9e1e985b7c37692940a245be4adee5f0b17d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:e297e28417c9eca28e081a9af377259d338ca01ace87847ad589b58f86c82bf5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112255714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134c7684bbd003994e454c9e84f8d4b2c04dcb395994d224d3156b152d559250`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 02 Oct 2023 07:48:04 GMT
RUN Apply image 10.0.17763.4974
# Wed, 11 Oct 2023 03:36:33 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:46:47 GMT
RUN cmd /S /C #(nop) COPY file:0e2c8ba21e47adc90962b46928c928315462bcddaefcbc01f98113f4f66cda4a in C:\nats-streaming-server.exe 
# Wed, 11 Oct 2023 03:46:48 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:49 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:5f8edc2588edb9971a52d53cd4265062614ebb25e94063a4d235376797b0e57a`  
		Last Modified: Tue, 10 Oct 2023 17:24:08 GMT  
		Size: 104.5 MB (104464580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52fe086e7510cd640f31a862cc7ed0aae171d6591241c4eddfbeda3169a718b`  
		Last Modified: Wed, 11 Oct 2023 03:40:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09d7a0fbe43c03a111bc3497f4ecd56125eee81703a31601f5c08e49f6fded`  
		Last Modified: Wed, 11 Oct 2023 03:47:27 GMT  
		Size: 7.8 MB (7786505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d22162cc13bcfe0390f62aea2d7826f50f4ee7a11ee116dc75f5634aedf1e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da5f219106d49348dcf807cb34c99caf0b1763d3fd87a7d6f8185fcbea07490`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4a9c07b5c7c0d51af9e577dd54910a01cea6b0f03506e0ffe3c479d062aa2f`  
		Last Modified: Wed, 11 Oct 2023 03:47:25 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:556ba52cac20d3ac56a9e0a25227feaab2f9dcaf11a226faaeda151db2c46f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:ac48bf7bcafb809e9fb50f7c37d6cc98ff2d6db110b4797ea079690a438fa23d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7659749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537ac3baf877ff3bbc0fc7cf2673a32f3f92e3cc9df60f77c3c9b3e87ea6a3e0`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 02:41:42 GMT
COPY file:670c17c233c7999d9f7b72c2962b221cab4e00da471a75e8679840c939143cfb in /nats-streaming-server 
# Sat, 21 Oct 2023 02:41:42 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 02:41:42 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 02:41:42 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:b7ff958d406306840566ff165f0c34c6017d44a13d4355d5eb8c6cd152c57d64`  
		Last Modified: Wed, 21 Jun 2023 01:11:25 GMT  
		Size: 7.7 MB (7659749 bytes)  
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
$ docker pull nats-streaming@sha256:024133b26fb0fa3ec37b3b3cb5bf6f024917c19a769efd697229e82dbdf3325f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7304325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba095b7f79702fc77948119fe82df535cac466d1a5c97c91065c12ad7a116e4`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Sat, 21 Oct 2023 00:55:23 GMT
COPY file:07846c068b31699c9c9fe9b535ec7c1dcfbda7a16d7d178a50de1f9541deeebf in /nats-streaming-server 
# Sat, 21 Oct 2023 00:55:23 GMT
EXPOSE 4222 8222
# Sat, 21 Oct 2023 00:55:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Sat, 21 Oct 2023 00:55:23 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:039446f9a794527f7060ddd5b9b8a071ffe8816fa5aae791c4bbf01db3656057`  
		Last Modified: Wed, 21 Jun 2023 01:31:55 GMT  
		Size: 7.3 MB (7304325 bytes)  
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
$ docker pull nats-streaming@sha256:a6d657e66afa846325fb726a3f8587f246c08c5e8a9f960defd40740326165ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:4eb649beae9ce26c6ccf0f0dbd3c3e198983dd2c23ff75af13eb3456388c52c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040135445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40986464eb49491748626500020ee674f8d14939636bf5719837a93fb7d67c87`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:42:17 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Wed, 11 Oct 2023 03:42:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.5/nats-streaming-server-v0.25.5-windows-amd64.zip
# Wed, 11 Oct 2023 03:42:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=709b481bfa3537dc7941490365e065554f19c7029830d765ef49e8cd16657b75
# Wed, 11 Oct 2023 03:43:58 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Oct 2023 03:46:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Oct 2023 03:46:31 GMT
EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f30b1f53ee1616f24332acf6cdcca95e017a8ba32e308605859877b9ed83c`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb77616131a4292e9336a73c3285b758675cccf268367732e95f68d705bcba`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a926a9c704cce075dcda274fd7979538a59de5fb16df6eb1b1ec8fc1de42fd07`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02713c5d92e8c7136d3ce18a3eb90deda51b81323e65a7f13f48bc665e154f`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 443.6 KB (443570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda3c2b906ebceedb516bcca46cdf2e1cb8c5dae6c8d9e1eab434c1b1782c761`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 8.1 MB (8089974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a521779f3391f596ac25e9b136ea30296ebb050951a2acbae3f25e65aaed67`  
		Last Modified: Wed, 11 Oct 2023 03:47:10 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d1809820a3e752c85d4a50b42b8287f119da9d82d6a6989374ae4e038348e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9560dcf383eab30612cff911b05b7eebfae68baaae360a3439512b15b86f5`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:a6d657e66afa846325fb726a3f8587f246c08c5e8a9f960defd40740326165ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4974; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.4974; amd64

```console
$ docker pull nats-streaming@sha256:4eb649beae9ce26c6ccf0f0dbd3c3e198983dd2c23ff75af13eb3456388c52c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040135445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40986464eb49491748626500020ee674f8d14939636bf5719837a93fb7d67c87`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:32:17 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 Oct 2023 03:42:17 GMT
ENV NATS_STREAMING_SERVER=0.25.5
# Wed, 11 Oct 2023 03:42:18 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.5/nats-streaming-server-v0.25.5-windows-amd64.zip
# Wed, 11 Oct 2023 03:42:19 GMT
ENV NATS_STREAMING_SERVER_SHASUM=709b481bfa3537dc7941490365e065554f19c7029830d765ef49e8cd16657b75
# Wed, 11 Oct 2023 03:43:58 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 Oct 2023 03:46:30 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 11 Oct 2023 03:46:31 GMT
EXPOSE 4222 8222
# Wed, 11 Oct 2023 03:46:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 11 Oct 2023 03:46:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce27dbaad0cf1a29b13da65c8ec2c9e6b42aaf192bb7138ab6c5b740dbd77b05`  
		Last Modified: Wed, 11 Oct 2023 03:40:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f30b1f53ee1616f24332acf6cdcca95e017a8ba32e308605859877b9ed83c`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb77616131a4292e9336a73c3285b758675cccf268367732e95f68d705bcba`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a926a9c704cce075dcda274fd7979538a59de5fb16df6eb1b1ec8fc1de42fd07`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc02713c5d92e8c7136d3ce18a3eb90deda51b81323e65a7f13f48bc665e154f`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 443.6 KB (443570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda3c2b906ebceedb516bcca46cdf2e1cb8c5dae6c8d9e1eab434c1b1782c761`  
		Last Modified: Wed, 11 Oct 2023 03:47:13 GMT  
		Size: 8.1 MB (8089974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a521779f3391f596ac25e9b136ea30296ebb050951a2acbae3f25e65aaed67`  
		Last Modified: Wed, 11 Oct 2023 03:47:10 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d1809820a3e752c85d4a50b42b8287f119da9d82d6a6989374ae4e038348e2`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9560dcf383eab30612cff911b05b7eebfae68baaae360a3439512b15b86f5`  
		Last Modified: Wed, 11 Oct 2023 03:47:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
