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
$ docker pull nats-streaming@sha256:6fdba0b346eabfd4882b99393054713ba14b71115c83aeec8b721642a10f7233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4499; amd64

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

### `nats-streaming:0.25` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine`

```console
$ docker pull nats-streaming@sha256:eaa4dd5fab53cfc59b4c9b9553b849766cfd3a6390d7eb37dbcb3ddaf1030520
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
$ docker pull nats-streaming@sha256:d0fdc549a33bcb12860538f88c24202d00c2d1bcb77265f299f4d78af31a9e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834ceab8479f5741291efe2ed76fc2d50021242adffdd66a8972620ef9165848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:47:16 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 14 Jun 2023 20:47:20 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Jun 2023 20:47:20 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:47:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e298276b6dff1997b0bc8062b2eff603120c26d1cedad97508803e23bd763`  
		Last Modified: Wed, 14 Jun 2023 20:47:35 GMT  
		Size: 7.5 MB (7491737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021e8e0b694634d2595aa29b04e3986aaea1785d6e41b05fa08de25b1251727`  
		Last Modified: Wed, 14 Jun 2023 20:47:33 GMT  
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
$ docker pull nats-streaming@sha256:f8e6bfeb52309f6f3cf515c69e3b246df8af4b50960a9d2895fecbf5866fd2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8260c8eaf416424f37df27ca8be98e21fcfb59dd9113e2b57b8fe6436ee686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:44:37 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Thu, 15 Jun 2023 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 15 Jun 2023 00:44:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Jun 2023 00:44:40 GMT
EXPOSE 4222 8222
# Thu, 15 Jun 2023 00:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:44:40 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d904e31f12f03f713b6543ccfddc3325c3824ef47958a0e47df7d8346f2d7e`  
		Last Modified: Thu, 15 Jun 2023 00:45:12 GMT  
		Size: 7.2 MB (7199481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc30e90e3dd2babab64ba43d1504cacac183c42003674fedfe6cf9771405582`  
		Last Modified: Thu, 15 Jun 2023 00:45:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-alpine3.17`

```console
$ docker pull nats-streaming@sha256:eaa4dd5fab53cfc59b4c9b9553b849766cfd3a6390d7eb37dbcb3ddaf1030520
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
$ docker pull nats-streaming@sha256:d0fdc549a33bcb12860538f88c24202d00c2d1bcb77265f299f4d78af31a9e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834ceab8479f5741291efe2ed76fc2d50021242adffdd66a8972620ef9165848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:47:16 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 14 Jun 2023 20:47:20 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Jun 2023 20:47:20 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:47:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e298276b6dff1997b0bc8062b2eff603120c26d1cedad97508803e23bd763`  
		Last Modified: Wed, 14 Jun 2023 20:47:35 GMT  
		Size: 7.5 MB (7491737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021e8e0b694634d2595aa29b04e3986aaea1785d6e41b05fa08de25b1251727`  
		Last Modified: Wed, 14 Jun 2023 20:47:33 GMT  
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
$ docker pull nats-streaming@sha256:f8e6bfeb52309f6f3cf515c69e3b246df8af4b50960a9d2895fecbf5866fd2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8260c8eaf416424f37df27ca8be98e21fcfb59dd9113e2b57b8fe6436ee686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:44:37 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Thu, 15 Jun 2023 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 15 Jun 2023 00:44:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Jun 2023 00:44:40 GMT
EXPOSE 4222 8222
# Thu, 15 Jun 2023 00:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:44:40 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d904e31f12f03f713b6543ccfddc3325c3824ef47958a0e47df7d8346f2d7e`  
		Last Modified: Thu, 15 Jun 2023 00:45:12 GMT  
		Size: 7.2 MB (7199481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc30e90e3dd2babab64ba43d1504cacac183c42003674fedfe6cf9771405582`  
		Last Modified: Thu, 15 Jun 2023 00:45:11 GMT  
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
$ docker pull nats-streaming@sha256:3b7e4b704f0466c0dfef43e906115252302994de9697c0f0847235f5404ed44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25-nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:3b7e4b704f0466c0dfef43e906115252302994de9697c0f0847235f5404ed44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
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
$ docker pull nats-streaming@sha256:ce274b0f72665a790c69c2f584bae72c2ef1581fe2657aeddea0aabbeec6fbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:ff7aebb7d4bed3fa0235d90e3c48de54317f9454eda913f175b254f1489e43c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1658883092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bacf31d62af3204c751bae87f50d253f351d6368c8f46fa60085915285f2a05`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:20:36 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 14 Jun 2023 20:21:01 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jun 2023 20:22:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jun 2023 20:22:18 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:19 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6300e4464852708aabdb28508ff26b0f9b63d0a23116315568748aa1717bac45`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290e77efe91837df60b69849ab24de8dfebeb4a87e01be82dd1a7fad79397d5`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006319f36fb1612fb68b93dc5c03650c1b1e54042ff20ac584c1c7e031c223a3`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff384ad9b987e578ba589749e925c2eba5356fedc9e0e281220097736d4a9220`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 298.8 KB (298794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f5da9a07f3c9d87c3a8fcfa55b07e9971df3d2f1b0c23322e05746625b06c`  
		Last Modified: Wed, 14 Jun 2023 20:22:59 GMT  
		Size: 8.0 MB (7952706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64359490a0fc9d44344ffdbbec8a5071a30f0673026985067ef40249e03096aa`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e06ddbd74b971b641c9cdbe20f06fc993409f917c04b8a950db4f848973ecdc`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9cf5431741afbfb3387cbcbff88728e2f9f8ea41d943dd4cd6808e4fc2d514`  
		Last Modified: Wed, 14 Jun 2023 20:22:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ce274b0f72665a790c69c2f584bae72c2ef1581fe2657aeddea0aabbeec6fbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:ff7aebb7d4bed3fa0235d90e3c48de54317f9454eda913f175b254f1489e43c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1658883092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bacf31d62af3204c751bae87f50d253f351d6368c8f46fa60085915285f2a05`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:20:36 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 14 Jun 2023 20:21:01 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jun 2023 20:22:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jun 2023 20:22:18 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:19 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6300e4464852708aabdb28508ff26b0f9b63d0a23116315568748aa1717bac45`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290e77efe91837df60b69849ab24de8dfebeb4a87e01be82dd1a7fad79397d5`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006319f36fb1612fb68b93dc5c03650c1b1e54042ff20ac584c1c7e031c223a3`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff384ad9b987e578ba589749e925c2eba5356fedc9e0e281220097736d4a9220`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 298.8 KB (298794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f5da9a07f3c9d87c3a8fcfa55b07e9971df3d2f1b0c23322e05746625b06c`  
		Last Modified: Wed, 14 Jun 2023 20:22:59 GMT  
		Size: 8.0 MB (7952706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64359490a0fc9d44344ffdbbec8a5071a30f0673026985067ef40249e03096aa`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e06ddbd74b971b641c9cdbe20f06fc993409f917c04b8a950db4f848973ecdc`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9cf5431741afbfb3387cbcbff88728e2f9f8ea41d943dd4cd6808e4fc2d514`  
		Last Modified: Wed, 14 Jun 2023 20:22:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4`

```console
$ docker pull nats-streaming@sha256:6fdba0b346eabfd4882b99393054713ba14b71115c83aeec8b721642a10f7233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4499; amd64

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

### `nats-streaming:0.25.4` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-alpine`

```console
$ docker pull nats-streaming@sha256:eaa4dd5fab53cfc59b4c9b9553b849766cfd3a6390d7eb37dbcb3ddaf1030520
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
$ docker pull nats-streaming@sha256:d0fdc549a33bcb12860538f88c24202d00c2d1bcb77265f299f4d78af31a9e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834ceab8479f5741291efe2ed76fc2d50021242adffdd66a8972620ef9165848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:47:16 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 14 Jun 2023 20:47:20 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Jun 2023 20:47:20 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:47:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e298276b6dff1997b0bc8062b2eff603120c26d1cedad97508803e23bd763`  
		Last Modified: Wed, 14 Jun 2023 20:47:35 GMT  
		Size: 7.5 MB (7491737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021e8e0b694634d2595aa29b04e3986aaea1785d6e41b05fa08de25b1251727`  
		Last Modified: Wed, 14 Jun 2023 20:47:33 GMT  
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
$ docker pull nats-streaming@sha256:f8e6bfeb52309f6f3cf515c69e3b246df8af4b50960a9d2895fecbf5866fd2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8260c8eaf416424f37df27ca8be98e21fcfb59dd9113e2b57b8fe6436ee686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:44:37 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Thu, 15 Jun 2023 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 15 Jun 2023 00:44:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Jun 2023 00:44:40 GMT
EXPOSE 4222 8222
# Thu, 15 Jun 2023 00:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:44:40 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d904e31f12f03f713b6543ccfddc3325c3824ef47958a0e47df7d8346f2d7e`  
		Last Modified: Thu, 15 Jun 2023 00:45:12 GMT  
		Size: 7.2 MB (7199481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc30e90e3dd2babab64ba43d1504cacac183c42003674fedfe6cf9771405582`  
		Last Modified: Thu, 15 Jun 2023 00:45:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-alpine3.17`

```console
$ docker pull nats-streaming@sha256:eaa4dd5fab53cfc59b4c9b9553b849766cfd3a6390d7eb37dbcb3ddaf1030520
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
$ docker pull nats-streaming@sha256:d0fdc549a33bcb12860538f88c24202d00c2d1bcb77265f299f4d78af31a9e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834ceab8479f5741291efe2ed76fc2d50021242adffdd66a8972620ef9165848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:47:16 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 14 Jun 2023 20:47:20 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Jun 2023 20:47:20 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:47:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e298276b6dff1997b0bc8062b2eff603120c26d1cedad97508803e23bd763`  
		Last Modified: Wed, 14 Jun 2023 20:47:35 GMT  
		Size: 7.5 MB (7491737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021e8e0b694634d2595aa29b04e3986aaea1785d6e41b05fa08de25b1251727`  
		Last Modified: Wed, 14 Jun 2023 20:47:33 GMT  
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
$ docker pull nats-streaming@sha256:f8e6bfeb52309f6f3cf515c69e3b246df8af4b50960a9d2895fecbf5866fd2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8260c8eaf416424f37df27ca8be98e21fcfb59dd9113e2b57b8fe6436ee686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:44:37 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Thu, 15 Jun 2023 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 15 Jun 2023 00:44:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Jun 2023 00:44:40 GMT
EXPOSE 4222 8222
# Thu, 15 Jun 2023 00:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:44:40 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d904e31f12f03f713b6543ccfddc3325c3824ef47958a0e47df7d8346f2d7e`  
		Last Modified: Thu, 15 Jun 2023 00:45:12 GMT  
		Size: 7.2 MB (7199481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc30e90e3dd2babab64ba43d1504cacac183c42003674fedfe6cf9771405582`  
		Last Modified: Thu, 15 Jun 2023 00:45:11 GMT  
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
$ docker pull nats-streaming@sha256:3b7e4b704f0466c0dfef43e906115252302994de9697c0f0847235f5404ed44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25.4-nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:3b7e4b704f0466c0dfef43e906115252302994de9697c0f0847235f5404ed44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25.4-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
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
$ docker pull nats-streaming@sha256:ce274b0f72665a790c69c2f584bae72c2ef1581fe2657aeddea0aabbeec6fbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25.4-windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:ff7aebb7d4bed3fa0235d90e3c48de54317f9454eda913f175b254f1489e43c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1658883092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bacf31d62af3204c751bae87f50d253f351d6368c8f46fa60085915285f2a05`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:20:36 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 14 Jun 2023 20:21:01 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jun 2023 20:22:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jun 2023 20:22:18 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:19 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6300e4464852708aabdb28508ff26b0f9b63d0a23116315568748aa1717bac45`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290e77efe91837df60b69849ab24de8dfebeb4a87e01be82dd1a7fad79397d5`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006319f36fb1612fb68b93dc5c03650c1b1e54042ff20ac584c1c7e031c223a3`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff384ad9b987e578ba589749e925c2eba5356fedc9e0e281220097736d4a9220`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 298.8 KB (298794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f5da9a07f3c9d87c3a8fcfa55b07e9971df3d2f1b0c23322e05746625b06c`  
		Last Modified: Wed, 14 Jun 2023 20:22:59 GMT  
		Size: 8.0 MB (7952706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64359490a0fc9d44344ffdbbec8a5071a30f0673026985067ef40249e03096aa`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e06ddbd74b971b641c9cdbe20f06fc993409f917c04b8a950db4f848973ecdc`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9cf5431741afbfb3387cbcbff88728e2f9f8ea41d943dd4cd6808e4fc2d514`  
		Last Modified: Wed, 14 Jun 2023 20:22:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:0.25.4-windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ce274b0f72665a790c69c2f584bae72c2ef1581fe2657aeddea0aabbeec6fbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:0.25.4-windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:ff7aebb7d4bed3fa0235d90e3c48de54317f9454eda913f175b254f1489e43c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1658883092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bacf31d62af3204c751bae87f50d253f351d6368c8f46fa60085915285f2a05`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:20:36 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 14 Jun 2023 20:21:01 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jun 2023 20:22:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jun 2023 20:22:18 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:19 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6300e4464852708aabdb28508ff26b0f9b63d0a23116315568748aa1717bac45`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290e77efe91837df60b69849ab24de8dfebeb4a87e01be82dd1a7fad79397d5`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006319f36fb1612fb68b93dc5c03650c1b1e54042ff20ac584c1c7e031c223a3`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff384ad9b987e578ba589749e925c2eba5356fedc9e0e281220097736d4a9220`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 298.8 KB (298794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f5da9a07f3c9d87c3a8fcfa55b07e9971df3d2f1b0c23322e05746625b06c`  
		Last Modified: Wed, 14 Jun 2023 20:22:59 GMT  
		Size: 8.0 MB (7952706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64359490a0fc9d44344ffdbbec8a5071a30f0673026985067ef40249e03096aa`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e06ddbd74b971b641c9cdbe20f06fc993409f917c04b8a950db4f848973ecdc`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9cf5431741afbfb3387cbcbff88728e2f9f8ea41d943dd4cd6808e4fc2d514`  
		Last Modified: Wed, 14 Jun 2023 20:22:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine`

```console
$ docker pull nats-streaming@sha256:eaa4dd5fab53cfc59b4c9b9553b849766cfd3a6390d7eb37dbcb3ddaf1030520
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
$ docker pull nats-streaming@sha256:d0fdc549a33bcb12860538f88c24202d00c2d1bcb77265f299f4d78af31a9e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834ceab8479f5741291efe2ed76fc2d50021242adffdd66a8972620ef9165848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:47:16 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 14 Jun 2023 20:47:20 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Jun 2023 20:47:20 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:47:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e298276b6dff1997b0bc8062b2eff603120c26d1cedad97508803e23bd763`  
		Last Modified: Wed, 14 Jun 2023 20:47:35 GMT  
		Size: 7.5 MB (7491737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021e8e0b694634d2595aa29b04e3986aaea1785d6e41b05fa08de25b1251727`  
		Last Modified: Wed, 14 Jun 2023 20:47:33 GMT  
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
$ docker pull nats-streaming@sha256:f8e6bfeb52309f6f3cf515c69e3b246df8af4b50960a9d2895fecbf5866fd2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8260c8eaf416424f37df27ca8be98e21fcfb59dd9113e2b57b8fe6436ee686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:44:37 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Thu, 15 Jun 2023 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 15 Jun 2023 00:44:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Jun 2023 00:44:40 GMT
EXPOSE 4222 8222
# Thu, 15 Jun 2023 00:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:44:40 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d904e31f12f03f713b6543ccfddc3325c3824ef47958a0e47df7d8346f2d7e`  
		Last Modified: Thu, 15 Jun 2023 00:45:12 GMT  
		Size: 7.2 MB (7199481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc30e90e3dd2babab64ba43d1504cacac183c42003674fedfe6cf9771405582`  
		Last Modified: Thu, 15 Jun 2023 00:45:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:alpine3.17`

```console
$ docker pull nats-streaming@sha256:eaa4dd5fab53cfc59b4c9b9553b849766cfd3a6390d7eb37dbcb3ddaf1030520
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
$ docker pull nats-streaming@sha256:d0fdc549a33bcb12860538f88c24202d00c2d1bcb77265f299f4d78af31a9e34
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834ceab8479f5741291efe2ed76fc2d50021242adffdd66a8972620ef9165848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:47:16 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:47:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Wed, 14 Jun 2023 20:47:20 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Wed, 14 Jun 2023 20:47:20 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 20:47:20 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15e298276b6dff1997b0bc8062b2eff603120c26d1cedad97508803e23bd763`  
		Last Modified: Wed, 14 Jun 2023 20:47:35 GMT  
		Size: 7.5 MB (7491737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021e8e0b694634d2595aa29b04e3986aaea1785d6e41b05fa08de25b1251727`  
		Last Modified: Wed, 14 Jun 2023 20:47:33 GMT  
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
$ docker pull nats-streaming@sha256:f8e6bfeb52309f6f3cf515c69e3b246df8af4b50960a9d2895fecbf5866fd2a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10461041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8260c8eaf416424f37df27ca8be98e21fcfb59dd9113e2b57b8fe6436ee686e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:44:37 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Thu, 15 Jun 2023 00:44:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b1305186b5df32f9c9bef66fee79731b163d1cd4e682f66829e7243e8ae405e7' ;; 		armhf) natsArch='arm6'; sha256='2a83fc9a854d4d5d3c77f24ff1bee31eba9995c636a924ed2f73abc4119f6b4d' ;; 		armv7) natsArch='arm7'; sha256='a75e420054361230f7e07673df2b3a32a8096aa3d67b1fc9d6d34554c88a3f44' ;; 		x86_64) natsArch='amd64'; sha256='80a6fdff0f1f6d44f8f8e6d2b4c3922ec430bcf14410a20f9b3dba107c6935df' ;; 		x86) natsArch='386'; sha256='e57a570ca006ddff8a23c02a90d0f71d97817e96a21b2e20dffcdc2bd36ce91b' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-streaming-server.tar.gz "https://github.com/nats-io/nats-streaming-server/releases/download/v${NATS_STREAMING_SERVER}/nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-streaming-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-streaming-server.tar.gz; 	rm nats-streaming-server.tar.gz; 	mv "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}/nats-streaming-server" /usr/local/bin; 	rm -rf "nats-streaming-server-v${NATS_STREAMING_SERVER}-linux-${natsArch}"
# Thu, 15 Jun 2023 00:44:40 GMT
COPY file:528000310df8681fb95f43d3bcf7c8086cd514c78673b1aadb984b1db3331559 in /usr/local/bin 
# Thu, 15 Jun 2023 00:44:40 GMT
EXPOSE 4222 8222
# Thu, 15 Jun 2023 00:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 00:44:40 GMT
CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d904e31f12f03f713b6543ccfddc3325c3824ef47958a0e47df7d8346f2d7e`  
		Last Modified: Thu, 15 Jun 2023 00:45:12 GMT  
		Size: 7.2 MB (7199481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc30e90e3dd2babab64ba43d1504cacac183c42003674fedfe6cf9771405582`  
		Last Modified: Thu, 15 Jun 2023 00:45:11 GMT  
		Size: 421.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:latest`

```console
$ docker pull nats-streaming@sha256:6fdba0b346eabfd4882b99393054713ba14b71115c83aeec8b721642a10f7233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.4499; amd64

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

### `nats-streaming:latest` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
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
$ docker pull nats-streaming@sha256:3b7e4b704f0466c0dfef43e906115252302994de9697c0f0847235f5404ed44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:3b7e4b704f0466c0dfef43e906115252302994de9697c0f0847235f5404ed44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:3ae78c725a624f358aef7f98633bb87839985fac9586164bbc78aac4bb1637ba
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.1 MB (112082027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5991cab881d07e9f4b2e5c96e4259daca7a94359703ef45f9c8e48462713297`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 20:19:03 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:22:34 GMT
RUN cmd /S /C #(nop) COPY file:0e00517c0cd7c30ea7241b4f7d1c93e706f8f35958d1ed6c5b70afff806c7e8b in C:\nats-streaming-server.exe 
# Wed, 14 Jun 2023 20:22:35 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:36 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:37 GMT
RUN cmd /S /C #(nop)  CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad82a63ae84196afc54c5956c7877278d6c0b6a91e47222a50d790c2d9e07f5e`  
		Last Modified: Wed, 14 Jun 2023 20:19:50 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec4d45515e12b08a256b689890102635738479945e8de553d51fe6fe7a0ddc1`  
		Last Modified: Wed, 14 Jun 2023 20:23:13 GMT  
		Size: 7.7 MB (7679571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdf40c64f69395fb8e51113eda6f5024244cfd5c050d4ca16405e77e90c6af4`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5aa9d322fa16d07cdf54ab3bf2d64c8009998b5ee201c5e0ae4e21e3af7edb`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3146ca21f73699726c7a5810a9394aed14c032d25b40ca2a43fe505fa9ce371f`  
		Last Modified: Wed, 14 Jun 2023 20:23:11 GMT  
		Size: 1.2 KB (1164 bytes)  
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
$ docker pull nats-streaming@sha256:ce274b0f72665a790c69c2f584bae72c2ef1581fe2657aeddea0aabbeec6fbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:ff7aebb7d4bed3fa0235d90e3c48de54317f9454eda913f175b254f1489e43c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1658883092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bacf31d62af3204c751bae87f50d253f351d6368c8f46fa60085915285f2a05`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:20:36 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 14 Jun 2023 20:21:01 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jun 2023 20:22:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jun 2023 20:22:18 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:19 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6300e4464852708aabdb28508ff26b0f9b63d0a23116315568748aa1717bac45`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290e77efe91837df60b69849ab24de8dfebeb4a87e01be82dd1a7fad79397d5`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006319f36fb1612fb68b93dc5c03650c1b1e54042ff20ac584c1c7e031c223a3`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff384ad9b987e578ba589749e925c2eba5356fedc9e0e281220097736d4a9220`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 298.8 KB (298794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f5da9a07f3c9d87c3a8fcfa55b07e9971df3d2f1b0c23322e05746625b06c`  
		Last Modified: Wed, 14 Jun 2023 20:22:59 GMT  
		Size: 8.0 MB (7952706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64359490a0fc9d44344ffdbbec8a5071a30f0673026985067ef40249e03096aa`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e06ddbd74b971b641c9cdbe20f06fc993409f917c04b8a950db4f848973ecdc`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9cf5431741afbfb3387cbcbff88728e2f9f8ea41d943dd4cd6808e4fc2d514`  
		Last Modified: Wed, 14 Jun 2023 20:22:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats-streaming:windowsservercore-1809`

```console
$ docker pull nats-streaming@sha256:ce274b0f72665a790c69c2f584bae72c2ef1581fe2657aeddea0aabbeec6fbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `nats-streaming:windowsservercore-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull nats-streaming@sha256:ff7aebb7d4bed3fa0235d90e3c48de54317f9454eda913f175b254f1489e43c3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1658883092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bacf31d62af3204c751bae87f50d253f351d6368c8f46fa60085915285f2a05`
-	Entrypoint: `["C:\\nats-streaming-server.exe"]`
-	Default Command: `["-m","8222"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 19:18:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 20:17:19 GMT
ENV NATS_DOCKERIZED=1
# Wed, 14 Jun 2023 20:20:36 GMT
ENV NATS_STREAMING_SERVER=0.25.4
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_DOWNLOAD=https://github.com/nats-io/nats-streaming-server/releases/download/v0.25.4/nats-streaming-server-v0.25.4-windows-amd64.zip
# Wed, 14 Jun 2023 20:20:37 GMT
ENV NATS_STREAMING_SERVER_SHASUM=78e72b73ff15f566c7f8a9a326c189efe04fa9dc3a16d7b8c71c6c1f1ecf818f
# Wed, 14 Jun 2023 20:21:01 GMT
RUN Set-PSDebug -Trace 2
# Wed, 14 Jun 2023 20:22:17 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_STREAMING_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_STREAMING_SERVER_DOWNLOAD -OutFile nats-streaming.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_STREAMING_SERVER_SHASUM); 	if ((Get-FileHash nats-streaming.zip -Algorithm sha256).Hash -ne $env:NATS_STREAMING_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats-streaming.zip'; 	Expand-Archive -Path 'nats-streaming.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-streaming-server-v*/nats-streaming-server.exe -Destination C:\\nats-streaming-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats-streaming.zip; 	Remove-Item -Recurse -Force nats-streaming-server-v*; 		Write-Host 'complete.';
# Wed, 14 Jun 2023 20:22:18 GMT
EXPOSE 4222 8222
# Wed, 14 Jun 2023 20:22:19 GMT
ENTRYPOINT ["C:\\nats-streaming-server.exe"]
# Wed, 14 Jun 2023 20:22:19 GMT
CMD ["-m" "8222"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3929a070e5d6b9cb95587cf41492d8ef77aaa7e9f90fa3cd1b32619fae5debc2`  
		Last Modified: Wed, 14 Jun 2023 19:51:36 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc032b2e13168aa149afc2fa80f0046e2522b46496b0b11ae5e6e6cde6afec87`  
		Last Modified: Wed, 14 Jun 2023 20:19:35 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6300e4464852708aabdb28508ff26b0f9b63d0a23116315568748aa1717bac45`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290e77efe91837df60b69849ab24de8dfebeb4a87e01be82dd1a7fad79397d5`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006319f36fb1612fb68b93dc5c03650c1b1e54042ff20ac584c1c7e031c223a3`  
		Last Modified: Wed, 14 Jun 2023 20:22:58 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff384ad9b987e578ba589749e925c2eba5356fedc9e0e281220097736d4a9220`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 298.8 KB (298794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5f5da9a07f3c9d87c3a8fcfa55b07e9971df3d2f1b0c23322e05746625b06c`  
		Last Modified: Wed, 14 Jun 2023 20:22:59 GMT  
		Size: 8.0 MB (7952706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64359490a0fc9d44344ffdbbec8a5071a30f0673026985067ef40249e03096aa`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e06ddbd74b971b641c9cdbe20f06fc993409f917c04b8a950db4f848973ecdc`  
		Last Modified: Wed, 14 Jun 2023 20:22:57 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9cf5431741afbfb3387cbcbff88728e2f9f8ea41d943dd4cd6808e4fc2d514`  
		Last Modified: Wed, 14 Jun 2023 20:22:56 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
