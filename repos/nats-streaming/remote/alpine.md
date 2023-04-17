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
