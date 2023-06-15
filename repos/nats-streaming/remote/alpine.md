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
