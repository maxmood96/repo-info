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
-	[`nats-streaming:0.25.4`](#nats-streaming0254)
-	[`nats-streaming:0.25.4-alpine`](#nats-streaming0254-alpine)
-	[`nats-streaming:0.25.4-alpine3.17`](#nats-streaming0254-alpine317)
-	[`nats-streaming:0.25.4-linux`](#nats-streaming0254-linux)
-	[`nats-streaming:0.25.4-nanoserver`](#nats-streaming0254-nanoserver)
-	[`nats-streaming:0.25.4-nanoserver-1809`](#nats-streaming0254-nanoserver-1809)
-	[`nats-streaming:0.25.4-scratch`](#nats-streaming0254-scratch)
-	[`nats-streaming:0.25.4-windowsservercore`](#nats-streaming0254-windowsservercore)
-	[`nats-streaming:0.25.4-windowsservercore-1809`](#nats-streaming0254-windowsservercore-1809)
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
$ docker pull nats-streaming@sha256:a0960dd140b5d38ca1a554e1fcc3fe0a227cf0781e33543b731f95de47d840c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:ecccfb48ab240f9233e5ba8e29d9ddc48efe5648110e5d516ca01c0d82fe0ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:38e999f0beff0f967a2c9dfcd27d0d6312b326ea5916ec7fc06432c79e8d5325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11212783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257459de7895aa3b0b6c9ffd61540a25cf1c254f1e1fb72e8dcea641f717a70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:49:00 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:49:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:49:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:49:02 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:49:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f0977712b6ef4b0c31618b2e983a6918f2c1245a6c8970b9bcda9d051b0d4c`  
		Last Modified: Mon, 17 Apr 2023 22:49:25 GMT  
		Size: 7.8 MB (7837799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd1bec7f634145a47b852f024f0c35354024cac3005c9cd5fa3d20b53ba1e`  
		Last Modified: Mon, 17 Apr 2023 22:49:24 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:ef9bb0b9244b692b7b534a997c5be972871b7c792f3f9fade0e77e4e5cda181a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10602928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba7d7bb097de56fc960b525b28cb110b44b7f2c8a615fa13f3ed0a190e0b50a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 21:58:58 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 21:59:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 21:59:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 21:59:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 21:59:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a40484610b2ac8f41acc1cb5dd1a278098913d9905e628b53ed6d553fcbbd6`  
		Last Modified: Mon, 17 Apr 2023 21:59:20 GMT  
		Size: 7.5 MB (7491706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d02692e82a02f91b002b8375af0842ffad1265b95e3c6d049ce38a1389ef8`  
		Last Modified: Mon, 17 Apr 2023 21:59:19 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:1e9f7903b6b85971559c83f9fc039169995faab25f0fe416b571e289d21dc703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10350660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c31a40481af64a40c25a5d578626fbd8d7131bd65cb79588c83dd8ec76c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:28:14 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:28:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:28:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:28:17 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:28:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b90af4e1497c880b071dff095f8f5705247228f7bc236d9718758592e8156`  
		Last Modified: Mon, 17 Apr 2023 22:28:37 GMT  
		Size: 7.5 MB (7481718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74f6c47ace3d3147e03c8be1970cb571272d1118bae88c4d435486b653f40ed`  
		Last Modified: Mon, 17 Apr 2023 22:28:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:6c5fb27f7b451f3be83d033edea067759ac2707b96af06a104a93b9d00d4bda9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece55399c70f82e7268398ad0fcae1f5787e49908bbef6b1f47b61b2a9a665d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:41:54 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:41:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:41:57 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:41:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afeb857e7e07c31a53e54d0bdbf099761d6ed2d23a0a2e957c4a166c69da69f`  
		Last Modified: Mon, 17 Apr 2023 22:42:14 GMT  
		Size: 7.2 MB (7199488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87284d207faa077c1a6041863a07c7012037d1e4d3994b050698e3ec3710f7b9`  
		Last Modified: Mon, 17 Apr 2023 22:42:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.17`

```console
$ docker pull nats-streaming@sha256:ecccfb48ab240f9233e5ba8e29d9ddc48efe5648110e5d516ca01c0d82fe0ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-alpine3.17` - linux; amd64

```console
$ docker pull nats-streaming@sha256:38e999f0beff0f967a2c9dfcd27d0d6312b326ea5916ec7fc06432c79e8d5325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11212783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257459de7895aa3b0b6c9ffd61540a25cf1c254f1e1fb72e8dcea641f717a70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:49:00 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:49:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:49:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:49:02 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:49:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f0977712b6ef4b0c31618b2e983a6918f2c1245a6c8970b9bcda9d051b0d4c`  
		Last Modified: Mon, 17 Apr 2023 22:49:25 GMT  
		Size: 7.8 MB (7837799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd1bec7f634145a47b852f024f0c35354024cac3005c9cd5fa3d20b53ba1e`  
		Last Modified: Mon, 17 Apr 2023 22:49:24 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:ef9bb0b9244b692b7b534a997c5be972871b7c792f3f9fade0e77e4e5cda181a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10602928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba7d7bb097de56fc960b525b28cb110b44b7f2c8a615fa13f3ed0a190e0b50a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 21:58:58 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 21:59:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 21:59:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 21:59:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 21:59:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a40484610b2ac8f41acc1cb5dd1a278098913d9905e628b53ed6d553fcbbd6`  
		Last Modified: Mon, 17 Apr 2023 21:59:20 GMT  
		Size: 7.5 MB (7491706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d02692e82a02f91b002b8375af0842ffad1265b95e3c6d049ce38a1389ef8`  
		Last Modified: Mon, 17 Apr 2023 21:59:19 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:1e9f7903b6b85971559c83f9fc039169995faab25f0fe416b571e289d21dc703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10350660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c31a40481af64a40c25a5d578626fbd8d7131bd65cb79588c83dd8ec76c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:28:14 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:28:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:28:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:28:17 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:28:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b90af4e1497c880b071dff095f8f5705247228f7bc236d9718758592e8156`  
		Last Modified: Mon, 17 Apr 2023 22:28:37 GMT  
		Size: 7.5 MB (7481718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74f6c47ace3d3147e03c8be1970cb571272d1118bae88c4d435486b653f40ed`  
		Last Modified: Mon, 17 Apr 2023 22:28:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:6c5fb27f7b451f3be83d033edea067759ac2707b96af06a104a93b9d00d4bda9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece55399c70f82e7268398ad0fcae1f5787e49908bbef6b1f47b61b2a9a665d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:41:54 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:41:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:41:57 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:41:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afeb857e7e07c31a53e54d0bdbf099761d6ed2d23a0a2e957c4a166c69da69f`  
		Last Modified: Mon, 17 Apr 2023 22:42:14 GMT  
		Size: 7.2 MB (7199488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87284d207faa077c1a6041863a07c7012037d1e4d3994b050698e3ec3710f7b9`  
		Last Modified: Mon, 17 Apr 2023 22:42:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-linux`

```console
$ docker pull nats-streaming@sha256:15089c7420253cb51a7c9a1760a8d9f8ef66671b217064f781eebe96ae7805eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver`

```console
$ docker pull nats-streaming@sha256:8339b8cee3c3c1832a81b157e582f94eba09ec60af19fe6cf5d930f321f350a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:8339b8cee3c3c1832a81b157e582f94eba09ec60af19fe6cf5d930f321f350a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-scratch`

```console
$ docker pull nats-streaming@sha256:15089c7420253cb51a7c9a1760a8d9f8ef66671b217064f781eebe96ae7805eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore`

```console
$ docker pull nats-streaming@sha256:ba4b48de17ea4bf3dd45a183af928cb7cbea4686b5c20b8a2bb2142b1915ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:c9d3520c171dd02c0d97416eb27c7c643ca56cef5f496c171ec59ae0c548f4d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080443117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708bba3694fbfcc1923767269f4308324f4f942b5a0a39dddd01d843d37c15f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:44:29 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 10 May 2023 02:44:30 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 10 May 2023 02:44:31 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 10 May 2023 02:45:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:48:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:48:32 GMT
EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5856405e72972496afbf612f06bd9c56483b3ffdcc1f1f765a39b96373db164`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f34a19213ebbfd3e71144d5a8ca3ed8d42f0b17b50d998fc496d16828c830b`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ea34cc555f2d95a16c0b18af06b76a789b93880c77e9f95b3a7472f4dbec62`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a347fb78d623251d604dd61bc05b7dcbe9d8f08593aae32ecc84762a7a9a1`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 424.7 KB (424664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de400e4f555d84e45ee3fc33ae8599c0d8b5d48accb86db6ca1abad19479546`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 8.0 MB (7971913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c10a5c8c435e5a841c49d51114c544a1c657deb0b6aa76fae32211bece286`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079014b7aa61da27a4c38e1027fd7939ff72e0b76977b2a30bd941a3cff01f4`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e78054f97dafd0ca0b369edd7447dd3ab27d54e1d5455754a3a33d48516fc7`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ba4b48de17ea4bf3dd45a183af928cb7cbea4686b5c20b8a2bb2142b1915ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:c9d3520c171dd02c0d97416eb27c7c643ca56cef5f496c171ec59ae0c548f4d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080443117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708bba3694fbfcc1923767269f4308324f4f942b5a0a39dddd01d843d37c15f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:44:29 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 10 May 2023 02:44:30 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 10 May 2023 02:44:31 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 10 May 2023 02:45:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:48:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:48:32 GMT
EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5856405e72972496afbf612f06bd9c56483b3ffdcc1f1f765a39b96373db164`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f34a19213ebbfd3e71144d5a8ca3ed8d42f0b17b50d998fc496d16828c830b`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ea34cc555f2d95a16c0b18af06b76a789b93880c77e9f95b3a7472f4dbec62`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a347fb78d623251d604dd61bc05b7dcbe9d8f08593aae32ecc84762a7a9a1`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 424.7 KB (424664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de400e4f555d84e45ee3fc33ae8599c0d8b5d48accb86db6ca1abad19479546`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 8.0 MB (7971913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c10a5c8c435e5a841c49d51114c544a1c657deb0b6aa76fae32211bece286`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079014b7aa61da27a4c38e1027fd7939ff72e0b76977b2a30bd941a3cff01f4`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e78054f97dafd0ca0b369edd7447dd3ab27d54e1d5455754a3a33d48516fc7`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4`

```console
$ docker pull nats-streaming@sha256:a0960dd140b5d38ca1a554e1fcc3fe0a227cf0781e33543b731f95de47d840c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25.4` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-alpine`

```console
$ docker pull nats-streaming@sha256:ecccfb48ab240f9233e5ba8e29d9ddc48efe5648110e5d516ca01c0d82fe0ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.4-alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:38e999f0beff0f967a2c9dfcd27d0d6312b326ea5916ec7fc06432c79e8d5325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11212783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257459de7895aa3b0b6c9ffd61540a25cf1c254f1e1fb72e8dcea641f717a70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:49:00 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:49:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:49:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:49:02 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:49:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f0977712b6ef4b0c31618b2e983a6918f2c1245a6c8970b9bcda9d051b0d4c`  
		Last Modified: Mon, 17 Apr 2023 22:49:25 GMT  
		Size: 7.8 MB (7837799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd1bec7f634145a47b852f024f0c35354024cac3005c9cd5fa3d20b53ba1e`  
		Last Modified: Mon, 17 Apr 2023 22:49:24 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:ef9bb0b9244b692b7b534a997c5be972871b7c792f3f9fade0e77e4e5cda181a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10602928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba7d7bb097de56fc960b525b28cb110b44b7f2c8a615fa13f3ed0a190e0b50a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 21:58:58 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 21:59:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 21:59:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 21:59:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 21:59:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a40484610b2ac8f41acc1cb5dd1a278098913d9905e628b53ed6d553fcbbd6`  
		Last Modified: Mon, 17 Apr 2023 21:59:20 GMT  
		Size: 7.5 MB (7491706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d02692e82a02f91b002b8375af0842ffad1265b95e3c6d049ce38a1389ef8`  
		Last Modified: Mon, 17 Apr 2023 21:59:19 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:1e9f7903b6b85971559c83f9fc039169995faab25f0fe416b571e289d21dc703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10350660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c31a40481af64a40c25a5d578626fbd8d7131bd65cb79588c83dd8ec76c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:28:14 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:28:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:28:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:28:17 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:28:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b90af4e1497c880b071dff095f8f5705247228f7bc236d9718758592e8156`  
		Last Modified: Mon, 17 Apr 2023 22:28:37 GMT  
		Size: 7.5 MB (7481718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74f6c47ace3d3147e03c8be1970cb571272d1118bae88c4d435486b653f40ed`  
		Last Modified: Mon, 17 Apr 2023 22:28:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:6c5fb27f7b451f3be83d033edea067759ac2707b96af06a104a93b9d00d4bda9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece55399c70f82e7268398ad0fcae1f5787e49908bbef6b1f47b61b2a9a665d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:41:54 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:41:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:41:57 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:41:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afeb857e7e07c31a53e54d0bdbf099761d6ed2d23a0a2e957c4a166c69da69f`  
		Last Modified: Mon, 17 Apr 2023 22:42:14 GMT  
		Size: 7.2 MB (7199488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87284d207faa077c1a6041863a07c7012037d1e4d3994b050698e3ec3710f7b9`  
		Last Modified: Mon, 17 Apr 2023 22:42:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-alpine3.17`

```console
$ docker pull nats-streaming@sha256:ecccfb48ab240f9233e5ba8e29d9ddc48efe5648110e5d516ca01c0d82fe0ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.4-alpine3.17` - linux; amd64

```console
$ docker pull nats-streaming@sha256:38e999f0beff0f967a2c9dfcd27d0d6312b326ea5916ec7fc06432c79e8d5325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11212783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257459de7895aa3b0b6c9ffd61540a25cf1c254f1e1fb72e8dcea641f717a70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:49:00 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:49:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:49:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:49:02 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:49:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f0977712b6ef4b0c31618b2e983a6918f2c1245a6c8970b9bcda9d051b0d4c`  
		Last Modified: Mon, 17 Apr 2023 22:49:25 GMT  
		Size: 7.8 MB (7837799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd1bec7f634145a47b852f024f0c35354024cac3005c9cd5fa3d20b53ba1e`  
		Last Modified: Mon, 17 Apr 2023 22:49:24 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:ef9bb0b9244b692b7b534a997c5be972871b7c792f3f9fade0e77e4e5cda181a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10602928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba7d7bb097de56fc960b525b28cb110b44b7f2c8a615fa13f3ed0a190e0b50a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 21:58:58 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 21:59:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 21:59:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 21:59:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 21:59:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a40484610b2ac8f41acc1cb5dd1a278098913d9905e628b53ed6d553fcbbd6`  
		Last Modified: Mon, 17 Apr 2023 21:59:20 GMT  
		Size: 7.5 MB (7491706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d02692e82a02f91b002b8375af0842ffad1265b95e3c6d049ce38a1389ef8`  
		Last Modified: Mon, 17 Apr 2023 21:59:19 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:1e9f7903b6b85971559c83f9fc039169995faab25f0fe416b571e289d21dc703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10350660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c31a40481af64a40c25a5d578626fbd8d7131bd65cb79588c83dd8ec76c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:28:14 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:28:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:28:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:28:17 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:28:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b90af4e1497c880b071dff095f8f5705247228f7bc236d9718758592e8156`  
		Last Modified: Mon, 17 Apr 2023 22:28:37 GMT  
		Size: 7.5 MB (7481718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74f6c47ace3d3147e03c8be1970cb571272d1118bae88c4d435486b653f40ed`  
		Last Modified: Mon, 17 Apr 2023 22:28:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:6c5fb27f7b451f3be83d033edea067759ac2707b96af06a104a93b9d00d4bda9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece55399c70f82e7268398ad0fcae1f5787e49908bbef6b1f47b61b2a9a665d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:41:54 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:41:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:41:57 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:41:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afeb857e7e07c31a53e54d0bdbf099761d6ed2d23a0a2e957c4a166c69da69f`  
		Last Modified: Mon, 17 Apr 2023 22:42:14 GMT  
		Size: 7.2 MB (7199488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87284d207faa077c1a6041863a07c7012037d1e4d3994b050698e3ec3710f7b9`  
		Last Modified: Mon, 17 Apr 2023 22:42:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-linux`

```console
$ docker pull nats-streaming@sha256:15089c7420253cb51a7c9a1760a8d9f8ef66671b217064f781eebe96ae7805eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.4-linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-nanoserver`

```console
$ docker pull nats-streaming@sha256:8339b8cee3c3c1832a81b157e582f94eba09ec60af19fe6cf5d930f321f350a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25.4-nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:8339b8cee3c3c1832a81b157e582f94eba09ec60af19fe6cf5d930f321f350a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25.4-nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-scratch`

```console
$ docker pull nats-streaming@sha256:15089c7420253cb51a7c9a1760a8d9f8ef66671b217064f781eebe96ae7805eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:0.25.4-scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:0.25.4-scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-windowsservercore`

```console
$ docker pull nats-streaming@sha256:ba4b48de17ea4bf3dd45a183af928cb7cbea4686b5c20b8a2bb2142b1915ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25.4-windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:c9d3520c171dd02c0d97416eb27c7c643ca56cef5f496c171ec59ae0c548f4d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080443117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708bba3694fbfcc1923767269f4308324f4f942b5a0a39dddd01d843d37c15f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:44:29 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 10 May 2023 02:44:30 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 10 May 2023 02:44:31 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 10 May 2023 02:45:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:48:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:48:32 GMT
EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5856405e72972496afbf612f06bd9c56483b3ffdcc1f1f765a39b96373db164`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f34a19213ebbfd3e71144d5a8ca3ed8d42f0b17b50d998fc496d16828c830b`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ea34cc555f2d95a16c0b18af06b76a789b93880c77e9f95b3a7472f4dbec62`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a347fb78d623251d604dd61bc05b7dcbe9d8f08593aae32ecc84762a7a9a1`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 424.7 KB (424664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de400e4f555d84e45ee3fc33ae8599c0d8b5d48accb86db6ca1abad19479546`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 8.0 MB (7971913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c10a5c8c435e5a841c49d51114c544a1c657deb0b6aa76fae32211bece286`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079014b7aa61da27a4c38e1027fd7939ff72e0b76977b2a30bd941a3cff01f4`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e78054f97dafd0ca0b369edd7447dd3ab27d54e1d5455754a3a33d48516fc7`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ba4b48de17ea4bf3dd45a183af928cb7cbea4686b5c20b8a2bb2142b1915ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:0.25.4-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:c9d3520c171dd02c0d97416eb27c7c643ca56cef5f496c171ec59ae0c548f4d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080443117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708bba3694fbfcc1923767269f4308324f4f942b5a0a39dddd01d843d37c15f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:44:29 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 10 May 2023 02:44:30 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 10 May 2023 02:44:31 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 10 May 2023 02:45:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:48:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:48:32 GMT
EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5856405e72972496afbf612f06bd9c56483b3ffdcc1f1f765a39b96373db164`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f34a19213ebbfd3e71144d5a8ca3ed8d42f0b17b50d998fc496d16828c830b`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ea34cc555f2d95a16c0b18af06b76a789b93880c77e9f95b3a7472f4dbec62`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a347fb78d623251d604dd61bc05b7dcbe9d8f08593aae32ecc84762a7a9a1`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 424.7 KB (424664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de400e4f555d84e45ee3fc33ae8599c0d8b5d48accb86db6ca1abad19479546`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 8.0 MB (7971913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c10a5c8c435e5a841c49d51114c544a1c657deb0b6aa76fae32211bece286`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079014b7aa61da27a4c38e1027fd7939ff72e0b76977b2a30bd941a3cff01f4`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e78054f97dafd0ca0b369edd7447dd3ab27d54e1d5455754a3a33d48516fc7`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:ecccfb48ab240f9233e5ba8e29d9ddc48efe5648110e5d516ca01c0d82fe0ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine` - linux; amd64

```console
$ docker pull nats-streaming@sha256:38e999f0beff0f967a2c9dfcd27d0d6312b326ea5916ec7fc06432c79e8d5325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11212783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257459de7895aa3b0b6c9ffd61540a25cf1c254f1e1fb72e8dcea641f717a70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:49:00 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:49:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:49:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:49:02 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:49:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f0977712b6ef4b0c31618b2e983a6918f2c1245a6c8970b9bcda9d051b0d4c`  
		Last Modified: Mon, 17 Apr 2023 22:49:25 GMT  
		Size: 7.8 MB (7837799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd1bec7f634145a47b852f024f0c35354024cac3005c9cd5fa3d20b53ba1e`  
		Last Modified: Mon, 17 Apr 2023 22:49:24 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:ef9bb0b9244b692b7b534a997c5be972871b7c792f3f9fade0e77e4e5cda181a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10602928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba7d7bb097de56fc960b525b28cb110b44b7f2c8a615fa13f3ed0a190e0b50a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 21:58:58 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 21:59:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 21:59:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 21:59:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 21:59:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a40484610b2ac8f41acc1cb5dd1a278098913d9905e628b53ed6d553fcbbd6`  
		Last Modified: Mon, 17 Apr 2023 21:59:20 GMT  
		Size: 7.5 MB (7491706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d02692e82a02f91b002b8375af0842ffad1265b95e3c6d049ce38a1389ef8`  
		Last Modified: Mon, 17 Apr 2023 21:59:19 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:1e9f7903b6b85971559c83f9fc039169995faab25f0fe416b571e289d21dc703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10350660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c31a40481af64a40c25a5d578626fbd8d7131bd65cb79588c83dd8ec76c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:28:14 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:28:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:28:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:28:17 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:28:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b90af4e1497c880b071dff095f8f5705247228f7bc236d9718758592e8156`  
		Last Modified: Mon, 17 Apr 2023 22:28:37 GMT  
		Size: 7.5 MB (7481718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74f6c47ace3d3147e03c8be1970cb571272d1118bae88c4d435486b653f40ed`  
		Last Modified: Mon, 17 Apr 2023 22:28:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:6c5fb27f7b451f3be83d033edea067759ac2707b96af06a104a93b9d00d4bda9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece55399c70f82e7268398ad0fcae1f5787e49908bbef6b1f47b61b2a9a665d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:41:54 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:41:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:41:57 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:41:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afeb857e7e07c31a53e54d0bdbf099761d6ed2d23a0a2e957c4a166c69da69f`  
		Last Modified: Mon, 17 Apr 2023 22:42:14 GMT  
		Size: 7.2 MB (7199488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87284d207faa077c1a6041863a07c7012037d1e4d3994b050698e3ec3710f7b9`  
		Last Modified: Mon, 17 Apr 2023 22:42:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.17`

```console
$ docker pull nats-streaming@sha256:ecccfb48ab240f9233e5ba8e29d9ddc48efe5648110e5d516ca01c0d82fe0ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:alpine3.17` - linux; amd64

```console
$ docker pull nats-streaming@sha256:38e999f0beff0f967a2c9dfcd27d0d6312b326ea5916ec7fc06432c79e8d5325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11212783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257459de7895aa3b0b6c9ffd61540a25cf1c254f1e1fb72e8dcea641f717a70a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:49:00 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:49:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:49:02 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:49:02 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:49:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f0977712b6ef4b0c31618b2e983a6918f2c1245a6c8970b9bcda9d051b0d4c`  
		Last Modified: Mon, 17 Apr 2023 22:49:25 GMT  
		Size: 7.8 MB (7837799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506cd1bec7f634145a47b852f024f0c35354024cac3005c9cd5fa3d20b53ba1e`  
		Last Modified: Mon, 17 Apr 2023 22:49:24 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.17` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:ef9bb0b9244b692b7b534a997c5be972871b7c792f3f9fade0e77e4e5cda181a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10602928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba7d7bb097de56fc960b525b28cb110b44b7f2c8a615fa13f3ed0a190e0b50a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 21:58:58 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 21:59:01 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 21:59:01 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 21:59:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 21:59:02 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a40484610b2ac8f41acc1cb5dd1a278098913d9905e628b53ed6d553fcbbd6`  
		Last Modified: Mon, 17 Apr 2023 21:59:20 GMT  
		Size: 7.5 MB (7491706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d02692e82a02f91b002b8375af0842ffad1265b95e3c6d049ce38a1389ef8`  
		Last Modified: Mon, 17 Apr 2023 21:59:19 GMT  
		Size: 420.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.17` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:1e9f7903b6b85971559c83f9fc039169995faab25f0fe416b571e289d21dc703
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10350660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257c31a40481af64a40c25a5d578626fbd8d7131bd65cb79588c83dd8ec76c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 18:03:38 GMT
ADD file:959fa0ffb60c37c4fdc0d32ac31511f8dead32ef7f4bd848b11ff144a6b37012 in / 
# Wed, 29 Mar 2023 18:03:38 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:28:14 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:28:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:28:17 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:28:17 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:28:17 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:fd4b2aeb476b6c2c0c3049dae919de20fe09e90deac95e3181d717055cbe6707`  
		Last Modified: Wed, 29 Mar 2023 18:06:56 GMT  
		Size: 2.9 MB (2868519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b90af4e1497c880b071dff095f8f5705247228f7bc236d9718758592e8156`  
		Last Modified: Mon, 17 Apr 2023 22:28:37 GMT  
		Size: 7.5 MB (7481718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74f6c47ace3d3147e03c8be1970cb571272d1118bae88c4d435486b653f40ed`  
		Last Modified: Mon, 17 Apr 2023 22:28:35 GMT  
		Size: 423.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:6c5fb27f7b451f3be83d033edea067759ac2707b96af06a104a93b9d00d4bda9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece55399c70f82e7268398ad0fcae1f5787e49908bbef6b1f47b61b2a9a665d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Mon, 17 Apr 2023 22:41:54 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:41:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Mon, 17 Apr 2023 22:41:57 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Mon, 17 Apr 2023 22:41:57 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 17 Apr 2023 22:41:57 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afeb857e7e07c31a53e54d0bdbf099761d6ed2d23a0a2e957c4a166c69da69f`  
		Last Modified: Mon, 17 Apr 2023 22:42:14 GMT  
		Size: 7.2 MB (7199488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87284d207faa077c1a6041863a07c7012037d1e4d3994b050698e3ec3710f7b9`  
		Last Modified: Mon, 17 Apr 2023 22:42:13 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:a0960dd140b5d38ca1a554e1fcc3fe0a227cf0781e33543b731f95de47d840c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:latest` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:latest` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:linux`

```console
$ docker pull nats-streaming@sha256:15089c7420253cb51a7c9a1760a8d9f8ef66671b217064f781eebe96ae7805eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:linux` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:linux` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver`

```console
$ docker pull nats-streaming@sha256:8339b8cee3c3c1832a81b157e582f94eba09ec60af19fe6cf5d930f321f350a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:8339b8cee3c3c1832a81b157e582f94eba09ec60af19fe6cf5d930f321f350a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:daa15d353f041c6c8e114618818b48f65a01880fe439c922dd98ed4ba3a3c6c4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112068135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2ede61ab681dc0a43623c3b26b0eabc6558afa7234c3a6f0196c922a58f9a3`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Fri, 05 May 2023 11:29:01 GMT
RUN Apply image 10.0.17763.4377
# Wed, 10 May 2023 02:43:57 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:48:46 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 10 May 2023 02:48:49 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:50 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:51 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:f7885e3a2dfeae5eea125d00da688c29930a05e4d904884fe43e093ce6223664`  
		Last Modified: Wed, 10 May 2023 01:49:01 GMT  
		Size: 104.4 MB (104383998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9af27dd7e62b7d94fa31a7c9efd9a532c42db89ec01fdb7fe430043ceabc5b4`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96709c00e6b3cfe56128a9cd7ad07abb6bb176875aebb4b403502a9e98aece44`  
		Last Modified: Wed, 10 May 2023 02:49:29 GMT  
		Size: 7.7 MB (7679558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cadd956c849bd9f25ff56ca84608ab65cba215fded14949b9d3ed8bf342ffa`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad05cd39ae11ebb694841718b69e7a856501b17eae91d1093c42a745a89acd1`  
		Last Modified: Wed, 10 May 2023 02:49:27 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97482c1556d4f84af21538b6a17f418756b500348807666d70d7a1fc6b874840`  
		Last Modified: Wed, 10 May 2023 02:49:26 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:scratch`

```console
$ docker pull nats-streaming@sha256:15089c7420253cb51a7c9a1760a8d9f8ef66671b217064f781eebe96ae7805eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats-streaming:scratch` - linux; amd64

```console
$ docker pull nats-streaming@sha256:8f219318fece55317574298cb7f970d31ed1e553d7b059d36015b0cc768bb48b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7553888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d73e165667cc10b05dbad88fac3566311079d4ceb1a0a2daa0b1a7d0e5dc2f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:49:09 GMT
COPY file:5ac616c5a60e71e58431a96c3a4d710f77abbae72b163151c0b800798a693e6e in /nats-streaming-server 
# Mon, 17 Apr 2023 22:49:09 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:49:09 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:49:09 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:cfb6c977a0eec5bb9cc5e5257a26e70fae30698ff12a7baecefd4088d57b5be9`  
		Last Modified: Mon, 17 Apr 2023 22:49:42 GMT  
		Size: 7.6 MB (7553888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v6

```console
$ docker pull nats-streaming@sha256:4e885fec2085aaed30489d10934af3b0b4166d8f8c839d7026b4edf2b8c79716
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7201921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad0b6cc06f140648f388a6e9366a026925dc2bd02d37897824abb681755774f`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 21:59:05 GMT
COPY file:3255864650458d4de1b6cf5163bf31d1a443358d07fd422dbee0573fefbfa26d in /nats-streaming-server 
# Mon, 17 Apr 2023 21:59:05 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 21:59:06 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 21:59:06 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7738682950a04fadd9a82a6d85ff413291b711a3dd1cd63eebf7044be2e16243`  
		Last Modified: Mon, 17 Apr 2023 21:59:35 GMT  
		Size: 7.2 MB (7201921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm variant v7

```console
$ docker pull nats-streaming@sha256:d1e78c446c8f20a06e68f393fc13289f669384dfc968c8be7cbc989430b541cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584df08e20350ba7485e8db958c0b1c2df50457b4e512ade98141a9d8e547693`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:28:23 GMT
COPY file:4e4c90dd6f9a06a3b172a41a1e46f5c947087509cc7b4a5f3ed2fff18d673649 in /nats-streaming-server 
# Mon, 17 Apr 2023 22:28:23 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:28:23 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:28:24 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:2e252fc3c0e247a75d040f85309e3945edd13fc22ff23d8fd225f8b360537fbf`  
		Last Modified: Mon, 17 Apr 2023 22:28:53 GMT  
		Size: 7.2 MB (7196501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats-streaming:scratch` - linux; arm64 variant v8

```console
$ docker pull nats-streaming@sha256:4d896320c84b70a3c46f53a9a2c9ffbe09f9d3bf87dc484d5d4f8b0be74cca57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6914400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b33032bdc6fb330e18873bd6e73821e8303e1c62a0c2a817b46524a232533ad`
-	Entrypoint: `["\/nats-streaming-server"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Mon, 17 Apr 2023 22:42:01 GMT
COPY file:5086fdbb43de8d21fda01e28313e8f9b8ea1d40c150c3f6da20dca31deec8aec in /nats-streaming-server 
# Mon, 17 Apr 2023 22:42:01 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:42:01 GMT
ENTRYPOINT ["/nats-streaming-server"]
# Mon, 17 Apr 2023 22:42:01 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:7e26e6f6baa768107b8ec8ae5c74287a1f0f7966eccc3dafd25d9ab14e648949`  
		Last Modified: Mon, 17 Apr 2023 22:42:30 GMT  
		Size: 6.9 MB (6914400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:ba4b48de17ea4bf3dd45a183af928cb7cbea4686b5c20b8a2bb2142b1915ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:c9d3520c171dd02c0d97416eb27c7c643ca56cef5f496c171ec59ae0c548f4d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080443117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708bba3694fbfcc1923767269f4308324f4f942b5a0a39dddd01d843d37c15f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:44:29 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 10 May 2023 02:44:30 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 10 May 2023 02:44:31 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 10 May 2023 02:45:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:48:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:48:32 GMT
EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5856405e72972496afbf612f06bd9c56483b3ffdcc1f1f765a39b96373db164`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f34a19213ebbfd3e71144d5a8ca3ed8d42f0b17b50d998fc496d16828c830b`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ea34cc555f2d95a16c0b18af06b76a789b93880c77e9f95b3a7472f4dbec62`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a347fb78d623251d604dd61bc05b7dcbe9d8f08593aae32ecc84762a7a9a1`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 424.7 KB (424664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de400e4f555d84e45ee3fc33ae8599c0d8b5d48accb86db6ca1abad19479546`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 8.0 MB (7971913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c10a5c8c435e5a841c49d51114c544a1c657deb0b6aa76fae32211bece286`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079014b7aa61da27a4c38e1027fd7939ff72e0b76977b2a30bd941a3cff01f4`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e78054f97dafd0ca0b369edd7447dd3ab27d54e1d5455754a3a33d48516fc7`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ba4b48de17ea4bf3dd45a183af928cb7cbea4686b5c20b8a2bb2142b1915ddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull nats-streaming@sha256:c9d3520c171dd02c0d97416eb27c7c643ca56cef5f496c171ec59ae0c548f4d2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080443117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708bba3694fbfcc1923767269f4308324f4f942b5a0a39dddd01d843d37c15f`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 01:56:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 May 2023 02:40:26 GMT
ENV NATS_DOCKERIZED=1
# Wed, 10 May 2023 02:44:29 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 10 May 2023 02:44:30 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 10 May 2023 02:44:31 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 10 May 2023 02:45:56 GMT
RUN Set-PSDebug -Trace 2
# Wed, 10 May 2023 02:48:28 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 10 May 2023 02:48:32 GMT
EXPOSE 4222 8222
# Wed, 10 May 2023 02:48:32 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 10 May 2023 02:48:33 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a89be60a77cd8d520ec5f03d703ddbc15675dd1df4d95e041032cf08960af5`  
		Last Modified: Wed, 10 May 2023 02:23:36 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446cee93ab2781cfc08e135a3a7ab166e5342ee6817c34fb47e0662c085bbc29`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5856405e72972496afbf612f06bd9c56483b3ffdcc1f1f765a39b96373db164`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f34a19213ebbfd3e71144d5a8ca3ed8d42f0b17b50d998fc496d16828c830b`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ea34cc555f2d95a16c0b18af06b76a789b93880c77e9f95b3a7472f4dbec62`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364a347fb78d623251d604dd61bc05b7dcbe9d8f08593aae32ecc84762a7a9a1`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 424.7 KB (424664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de400e4f555d84e45ee3fc33ae8599c0d8b5d48accb86db6ca1abad19479546`  
		Last Modified: Wed, 10 May 2023 02:49:15 GMT  
		Size: 8.0 MB (7971913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815c10a5c8c435e5a841c49d51114c544a1c657deb0b6aa76fae32211bece286`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7079014b7aa61da27a4c38e1027fd7939ff72e0b76977b2a30bd941a3cff01f4`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e78054f97dafd0ca0b369edd7447dd3ab27d54e1d5455754a3a33d48516fc7`  
		Last Modified: Wed, 10 May 2023 02:49:13 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
