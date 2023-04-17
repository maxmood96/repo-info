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
$ docker pull nats-streaming@sha256:98341c026f748a11eef0e656587466d519d6de78967276468b53f3afbcd1c38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4252; amd64

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

### `nats-streaming:0.25` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
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
$ docker pull nats-streaming@sha256:7fe77682189a10e23153f5857af180798045a9f934adade6140129d94d10062c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:7fe77682189a10e23153f5857af180798045a9f934adade6140129d94d10062c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
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
$ docker pull nats-streaming@sha256:87ce70f188f30d54c757448a2d4761e74b6c85757b1ebbf2a49a5a11d531bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:1dc5517bf09a9976e68dba7f6b6ea78fd33b4a4a3070fe90d617b0570aa47173
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2079834049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bf2a307447c1295467439bcba3e509c3f9df212705ee65a1b3a6d357960492`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Wed, 12 Apr 2023 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 02:41:25 GMT
ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:14:59 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:15:00 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Mon, 17 Apr 2023 22:15:01 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Mon, 17 Apr 2023 22:16:00 GMT
RUN Set-PSDebug -Trace 2
# Mon, 17 Apr 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 17 Apr 2023 22:17:47 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:47 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:48 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81203863a516fb636d8e06e71cc938e6621b372bd98921ce87d23012f6c9e4c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22e5d770cd81ae0b8d0e969f23155d2900d6270b1dd31877d3d940112d6c37c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc841f754a472cda0e0f75c9523334bf9fb155e04c1ce60486570040a1166b`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea02d39a95a4cf603d67e16b2f566298828ec45bd90bb59e1341efa0755759db`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a635439225671b7d0e53edccbd35a17a9c7b0857ea2259a97403dc03bdff85d1`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43df1ec113e9d95a6832cd2167fbfeeb21a265c91d275909df6416b533ef3b`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 502.8 KB (502765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de3e6f381be0716e1c23274b6d3965933128ca0fd0e37dbc6f1d83e7815ee8`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 8.0 MB (8028921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899ade839a203c60611f8a3af7d80de24fb2ea6c51074f56beb43bd3124af77a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45915970ae7d164ffe4bb07eeddb64fa07a47ed58b7810cfd1f54ea3963d73`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ae35753e32834cf86462290373d736fb55b99c7244dcb9d4a500d6e151e4a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:87ce70f188f30d54c757448a2d4761e74b6c85757b1ebbf2a49a5a11d531bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:1dc5517bf09a9976e68dba7f6b6ea78fd33b4a4a3070fe90d617b0570aa47173
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2079834049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bf2a307447c1295467439bcba3e509c3f9df212705ee65a1b3a6d357960492`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Wed, 12 Apr 2023 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 02:41:25 GMT
ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:14:59 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:15:00 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Mon, 17 Apr 2023 22:15:01 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Mon, 17 Apr 2023 22:16:00 GMT
RUN Set-PSDebug -Trace 2
# Mon, 17 Apr 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 17 Apr 2023 22:17:47 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:47 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:48 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81203863a516fb636d8e06e71cc938e6621b372bd98921ce87d23012f6c9e4c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22e5d770cd81ae0b8d0e969f23155d2900d6270b1dd31877d3d940112d6c37c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc841f754a472cda0e0f75c9523334bf9fb155e04c1ce60486570040a1166b`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea02d39a95a4cf603d67e16b2f566298828ec45bd90bb59e1341efa0755759db`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a635439225671b7d0e53edccbd35a17a9c7b0857ea2259a97403dc03bdff85d1`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43df1ec113e9d95a6832cd2167fbfeeb21a265c91d275909df6416b533ef3b`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 502.8 KB (502765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de3e6f381be0716e1c23274b6d3965933128ca0fd0e37dbc6f1d83e7815ee8`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 8.0 MB (8028921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899ade839a203c60611f8a3af7d80de24fb2ea6c51074f56beb43bd3124af77a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45915970ae7d164ffe4bb07eeddb64fa07a47ed58b7810cfd1f54ea3963d73`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ae35753e32834cf86462290373d736fb55b99c7244dcb9d4a500d6e151e4a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4`

```console
$ docker pull nats-streaming@sha256:98341c026f748a11eef0e656587466d519d6de78967276468b53f3afbcd1c38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4252; amd64

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

### `nats-streaming:0.25.4` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
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
$ docker pull nats-streaming@sha256:7fe77682189a10e23153f5857af180798045a9f934adade6140129d94d10062c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25.4-nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:7fe77682189a10e23153f5857af180798045a9f934adade6140129d94d10062c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25.4-nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
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
$ docker pull nats-streaming@sha256:87ce70f188f30d54c757448a2d4761e74b6c85757b1ebbf2a49a5a11d531bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25.4-windowsservercore` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:1dc5517bf09a9976e68dba7f6b6ea78fd33b4a4a3070fe90d617b0570aa47173
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2079834049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bf2a307447c1295467439bcba3e509c3f9df212705ee65a1b3a6d357960492`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Wed, 12 Apr 2023 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 02:41:25 GMT
ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:14:59 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:15:00 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Mon, 17 Apr 2023 22:15:01 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Mon, 17 Apr 2023 22:16:00 GMT
RUN Set-PSDebug -Trace 2
# Mon, 17 Apr 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 17 Apr 2023 22:17:47 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:47 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:48 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81203863a516fb636d8e06e71cc938e6621b372bd98921ce87d23012f6c9e4c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22e5d770cd81ae0b8d0e969f23155d2900d6270b1dd31877d3d940112d6c37c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc841f754a472cda0e0f75c9523334bf9fb155e04c1ce60486570040a1166b`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea02d39a95a4cf603d67e16b2f566298828ec45bd90bb59e1341efa0755759db`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a635439225671b7d0e53edccbd35a17a9c7b0857ea2259a97403dc03bdff85d1`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43df1ec113e9d95a6832cd2167fbfeeb21a265c91d275909df6416b533ef3b`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 502.8 KB (502765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de3e6f381be0716e1c23274b6d3965933128ca0fd0e37dbc6f1d83e7815ee8`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 8.0 MB (8028921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899ade839a203c60611f8a3af7d80de24fb2ea6c51074f56beb43bd3124af77a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45915970ae7d164ffe4bb07eeddb64fa07a47ed58b7810cfd1f54ea3963d73`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ae35753e32834cf86462290373d736fb55b99c7244dcb9d4a500d6e151e4a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:87ce70f188f30d54c757448a2d4761e74b6c85757b1ebbf2a49a5a11d531bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:0.25.4-windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:1dc5517bf09a9976e68dba7f6b6ea78fd33b4a4a3070fe90d617b0570aa47173
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2079834049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bf2a307447c1295467439bcba3e509c3f9df212705ee65a1b3a6d357960492`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Wed, 12 Apr 2023 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 02:41:25 GMT
ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:14:59 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:15:00 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Mon, 17 Apr 2023 22:15:01 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Mon, 17 Apr 2023 22:16:00 GMT
RUN Set-PSDebug -Trace 2
# Mon, 17 Apr 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 17 Apr 2023 22:17:47 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:47 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:48 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81203863a516fb636d8e06e71cc938e6621b372bd98921ce87d23012f6c9e4c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22e5d770cd81ae0b8d0e969f23155d2900d6270b1dd31877d3d940112d6c37c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc841f754a472cda0e0f75c9523334bf9fb155e04c1ce60486570040a1166b`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea02d39a95a4cf603d67e16b2f566298828ec45bd90bb59e1341efa0755759db`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a635439225671b7d0e53edccbd35a17a9c7b0857ea2259a97403dc03bdff85d1`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43df1ec113e9d95a6832cd2167fbfeeb21a265c91d275909df6416b533ef3b`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 502.8 KB (502765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de3e6f381be0716e1c23274b6d3965933128ca0fd0e37dbc6f1d83e7815ee8`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 8.0 MB (8028921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899ade839a203c60611f8a3af7d80de24fb2ea6c51074f56beb43bd3124af77a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45915970ae7d164ffe4bb07eeddb64fa07a47ed58b7810cfd1f54ea3963d73`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ae35753e32834cf86462290373d736fb55b99c7244dcb9d4a500d6e151e4a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1383 bytes)  
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
$ docker pull nats-streaming@sha256:98341c026f748a11eef0e656587466d519d6de78967276468b53f3afbcd1c38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4252; amd64

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

### `nats-streaming:latest` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
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
$ docker pull nats-streaming@sha256:7fe77682189a10e23153f5857af180798045a9f934adade6140129d94d10062c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:7fe77682189a10e23153f5857af180798045a9f934adade6140129d94d10062c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:266e8b0dfd483c8e6eed9d4510bd4dc0f27320bacf0c544a43f6d8386d09e532
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.5 MB (114473097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78287e731941eed749be931133731598b12790e9e05b14a4a44f7a5325999b9`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Wed, 05 Apr 2023 00:14:49 GMT
RUN Apply image 10.0.17763.4252
# Wed, 12 Apr 2023 02:46:54 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Mon, 17 Apr 2023 22:17:58 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:59 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:af799fb2ff133c89311c6a42d34b8cb6c9b11d775f52e04ab08389d05e64ed1c`  
		Last Modified: Wed, 12 Apr 2023 00:53:10 GMT  
		Size: 106.8 MB (106788951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfc7d128fe5c7171551f4a377b11c36a7622d87a3d7acc003e8144ead046dbf`  
		Last Modified: Wed, 12 Apr 2023 02:48:07 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6275a1616e17d9c0585bf2ccb1e0487068aae579a0d9df43f494b3c0f04cf7`  
		Last Modified: Mon, 17 Apr 2023 22:18:39 GMT  
		Size: 7.7 MB (7679502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5626b5a05af1c5fbaf773ca0a29f435845e102703126a035695ed0c7a0ef52`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b086f5dbcd94ce89896946ff27f5080cabe21286ee2d29215158949a1b08f0`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1cd8a0e6413c49570a03f5f49e3226fe2210164c31fc1ad114d76e74cd66a6`  
		Last Modified: Mon, 17 Apr 2023 22:18:37 GMT  
		Size: 1.2 KB (1160 bytes)  
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
$ docker pull nats-streaming@sha256:87ce70f188f30d54c757448a2d4761e74b6c85757b1ebbf2a49a5a11d531bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:1dc5517bf09a9976e68dba7f6b6ea78fd33b4a4a3070fe90d617b0570aa47173
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2079834049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bf2a307447c1295467439bcba3e509c3f9df212705ee65a1b3a6d357960492`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Wed, 12 Apr 2023 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 02:41:25 GMT
ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:14:59 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:15:00 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Mon, 17 Apr 2023 22:15:01 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Mon, 17 Apr 2023 22:16:00 GMT
RUN Set-PSDebug -Trace 2
# Mon, 17 Apr 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 17 Apr 2023 22:17:47 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:47 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:48 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81203863a516fb636d8e06e71cc938e6621b372bd98921ce87d23012f6c9e4c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22e5d770cd81ae0b8d0e969f23155d2900d6270b1dd31877d3d940112d6c37c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc841f754a472cda0e0f75c9523334bf9fb155e04c1ce60486570040a1166b`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea02d39a95a4cf603d67e16b2f566298828ec45bd90bb59e1341efa0755759db`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a635439225671b7d0e53edccbd35a17a9c7b0857ea2259a97403dc03bdff85d1`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43df1ec113e9d95a6832cd2167fbfeeb21a265c91d275909df6416b533ef3b`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 502.8 KB (502765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de3e6f381be0716e1c23274b6d3965933128ca0fd0e37dbc6f1d83e7815ee8`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 8.0 MB (8028921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899ade839a203c60611f8a3af7d80de24fb2ea6c51074f56beb43bd3124af77a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45915970ae7d164ffe4bb07eeddb64fa07a47ed58b7810cfd1f54ea3963d73`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ae35753e32834cf86462290373d736fb55b99c7244dcb9d4a500d6e151e4a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:87ce70f188f30d54c757448a2d4761e74b6c85757b1ebbf2a49a5a11d531bb0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4252; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.4252; amd64

```console
$ docker pull nats-streaming@sha256:1dc5517bf09a9976e68dba7f6b6ea78fd33b4a4a3070fe90d617b0570aa47173
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2079834049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88bf2a307447c1295467439bcba3e509c3f9df212705ee65a1b3a6d357960492`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Wed, 05 Apr 2023 00:41:54 GMT
RUN Install update 10.0.17763.4252
# Wed, 12 Apr 2023 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Apr 2023 02:41:25 GMT
ENV NATS_DOCKERIZED=1
# Mon, 17 Apr 2023 22:14:59 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Mon, 17 Apr 2023 22:15:00 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Mon, 17 Apr 2023 22:15:01 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Mon, 17 Apr 2023 22:16:00 GMT
RUN Set-PSDebug -Trace 2
# Mon, 17 Apr 2023 22:17:46 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Mon, 17 Apr 2023 22:17:47 GMT
EXPOSE 4222 8222
# Mon, 17 Apr 2023 22:17:47 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Mon, 17 Apr 2023 22:17:48 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9094c39c4b36a86359abb3da9e9d0d9c69b6930e9c7b308120310d43d63f693`  
		Last Modified: Wed, 12 Apr 2023 00:52:10 GMT  
		Size: 363.3 MB (363347289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81203863a516fb636d8e06e71cc938e6621b372bd98921ce87d23012f6c9e4c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22e5d770cd81ae0b8d0e969f23155d2900d6270b1dd31877d3d940112d6c37c`  
		Last Modified: Wed, 12 Apr 2023 02:47:45 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc841f754a472cda0e0f75c9523334bf9fb155e04c1ce60486570040a1166b`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea02d39a95a4cf603d67e16b2f566298828ec45bd90bb59e1341efa0755759db`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a635439225671b7d0e53edccbd35a17a9c7b0857ea2259a97403dc03bdff85d1`  
		Last Modified: Mon, 17 Apr 2023 22:18:25 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43df1ec113e9d95a6832cd2167fbfeeb21a265c91d275909df6416b533ef3b`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 502.8 KB (502765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03de3e6f381be0716e1c23274b6d3965933128ca0fd0e37dbc6f1d83e7815ee8`  
		Last Modified: Mon, 17 Apr 2023 22:18:26 GMT  
		Size: 8.0 MB (8028921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899ade839a203c60611f8a3af7d80de24fb2ea6c51074f56beb43bd3124af77a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd45915970ae7d164ffe4bb07eeddb64fa07a47ed58b7810cfd1f54ea3963d73`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ae35753e32834cf86462290373d736fb55b99c7244dcb9d4a500d6e151e4a`  
		Last Modified: Mon, 17 Apr 2023 22:18:24 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
