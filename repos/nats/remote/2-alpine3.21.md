## `nats:2-alpine3.21`

```console
$ docker pull nats@sha256:0451ec62031943afa591cf4e5f9404bce65b55a8671ab93a7d581d8028fc12a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine3.21` - linux; amd64

```console
$ docker pull nats@sha256:78c1052292c8d1bdabeca33c5cde417bb3b56c9a9a6707afd896ac74f8010e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10425424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e752c0a111d15eafa05314d85b32bdfc63c7a5190ba26712078e014ad5c12906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc83d3e520670ed878bfe5964638db9895fc2873acb2a25b7bd3a8b2916c3e`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 6.8 MB (6782209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1065a99208ad32f21adf1cc2983a318f6d19b678ce12103514758c5e75a1359`  
		Last Modified: Tue, 03 Jun 2025 13:30:31 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dc1d69fb3bb313c6fce126295baf9e644c735c5b709cb57462cf134d8b7535`  
		Last Modified: Tue, 03 Jun 2025 13:30:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:6425e7c42e8f01aed46c0c5a2c0e1538c4703e432be6a853fe400d6c070c46b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd03d3d4671688731cc2113bd6bce676daf486062cf7bf8a0ad509235b375b3`

```dockerfile
```

-	Layers:
	-	`sha256:8d13d777cfed6af6d839ab64cb7dc1dd2e3b2e7c64170ca5695c3a937b560432`  
		Last Modified: Thu, 22 May 2025 16:43:17 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v6

```console
$ docker pull nats@sha256:e9129c76ec8b39cfb61261ea43a529d2b048a22bd43dde23405476211d952fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fa20ad8f845d52ef2ede0cc269b4ade46343bd8ae9d91e0f89a101e164019a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedc41dc7d645196f64f183990aac84922d7dfeca30cdd62cc58afacced1e53e`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 6.5 MB (6500243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f84ca9e26add3645800a5d8875d035548ece025cd495d093506600b5fa3639`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a0bc1a6e6b564bac3444b012da7c2bd95b00fc4b30e2183f58fdfe67a29efc`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:cfc622005d6c0083932d3a442389e5ba0fed2eee0d382384117e632be9d2cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98224cc21fc700a931065a4257f0f576cb24d83f9f4cf3a756dbb8cfc211de84`

```dockerfile
```

-	Layers:
	-	`sha256:5b980a9b2e5b75054cfabe65a0bb0ca426c2aeb5cb4d1d0a7b3616d6b089aba1`  
		Last Modified: Thu, 22 May 2025 16:42:35 GMT  
		Size: 14.4 KB (14425 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm variant v7

```console
$ docker pull nats@sha256:f51b3ede38c787e45a1c58fe1758aa726cfc126eed5ef13dc9a66dbcfe4d8e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 MB (9587301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fcc07ad9637e3d6023e9c3faf8df41d76537efd7136923fe276ce3124a21f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da9afbd37259973c94e964e514f1fd5331fdff7c8a20c358c64209a54939892`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 6.5 MB (6488204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e46bef85887a3ca7141cdb651fb0907947c31453e3dd12d5f2e75d659f9bb81`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 562.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354ada5b8ea797d2e67d9817b4735e298f9e4328503c9b4faff09c816dd2a3fe`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 412.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:43fb4c5979976f655a571482f2fb7c95bdcfe76ea5c3d03822e834dba8c8ba43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103eb0538b45ceeaf49344cd2e475459141bba59c3b68cfa4b3f8c81bfaa0292`

```dockerfile
```

-	Layers:
	-	`sha256:48a6d4944ad8da069b2dcc13b6bf204e8ba6994953e03cdc717459fc9bec1bbc`  
		Last Modified: Fri, 23 May 2025 03:52:38 GMT  
		Size: 14.4 KB (14424 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:361d07db47a72d53a1159ce806effcfaacddb5c24254dc346aa6ed24d2eaff6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10265428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4a01a93d1901d7daaa7ad147102df5dc250516eb1b935b673cb01b2de9436`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28900756089c34ef75f78f9bc43820aee795ebced2ef164f4371a469020c319`  
		Last Modified: Tue, 03 Jun 2025 14:00:40 GMT  
		Size: 6.3 MB (6271430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a19d69a59c9c3d035125ee920379ce8b337cb0de1eb1646fa3b37bcc5bd4eca`  
		Last Modified: Tue, 03 Jun 2025 14:00:40 GMT  
		Size: 559.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002df6ee873e4c8b8c2d32bc19571ba115cbaeeaa22dbe5e19ea24a00121560a`  
		Last Modified: Tue, 03 Jun 2025 14:00:42 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:eeec07d9dba12fff9a629635d9822e295cbd2866800be7c10ae0f0eda767c376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eceb57113d3b7d11444b789b3d12801ddfaf3eadc8944e2457447d1469cc94db`

```dockerfile
```

-	Layers:
	-	`sha256:cac3279af5a354235660e8ed87c54fddc39e37fe276433cdd00c7a04a3f5877c`  
		Last Modified: Thu, 22 May 2025 20:04:28 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; ppc64le

```console
$ docker pull nats@sha256:6c62a05e9d2c74252f7e85ca263ff11fa47ca8d6a2314c95ef35830ca7dd5947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9829497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c4f82ed4f59bb1fc3f2bb1bf520c03a108a4b1201a308129e9f9c437eb69d20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab090fb5974c5fbc532a324c8b6ff89147f7b095e88f59c95200ff29b503d4ed`  
		Last Modified: Thu, 22 May 2025 16:46:06 GMT  
		Size: 6.3 MB (6254178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9ffdff7943fa553d5c46cd9bfd7cdb0aaf807fd213df6a3be9c0f47276b45d`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b243223ddfaabf20dea42482c30a57a1960b976113f905a07742d49e8fd76`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:209d5ce0eb3e58f76c4baefc159b91c7c24036c43252c4c06634f4218bfc2ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc856abe1e071c3b5e0dd0ac6a265939b68986e20ed0a612a3577747ed39b949`

```dockerfile
```

-	Layers:
	-	`sha256:9d5d8fc63a7e90cae4235128e35cce1f4b9143f897cba2831823fdf635d1c1a3`  
		Last Modified: Thu, 22 May 2025 16:46:05 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine3.21` - linux; s390x

```console
$ docker pull nats@sha256:113aca5863f11d04e9dcafd0a79496a1ecc86cdc2ccf02b720467c79eb2c1b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10087904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a783e13b44bb39120f57f582d383ada710ad715fc963f625760233ace3e4ab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 22 May 2025 13:53:13 GMT
ENV NATS_SERVER=2.11.4
# Thu, 22 May 2025 13:53:13 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='66b1ec828d78c3d24e207ad77239b2208d939c6bebd88fe0656be5eae325442c' ;; 		armhf) natsArch='arm6'; sha256='89a2a3525e9c1882e69a3b8c7413887b35bce6badc7ed52434237e6f4201d6ca' ;; 		armv7) natsArch='arm7'; sha256='244b122197847bce9ac8734d85a4e0d340e9eb6683903b74adf5d1e54e840b11' ;; 		x86_64) natsArch='amd64'; sha256='84192cee46c62760d9c259a97f373b73bccadc41be779c26ef676542ae15daf6' ;; 		x86) natsArch='386'; sha256='3f6bbd7ee8537e364681d60854f7c443b1395942cbf50cafa23b28d0e1e9b697' ;; 		s390x) natsArch='s390x'; sha256='f04399991c43feed206d8ec77b748d3d4fdba2503f5153743f6f5f1937d1b1fc' ;; 		ppc64le) natsArch='ppc64le'; sha256='8867a9368f2bdc12bf2ad9fbb7bb63c4c5ba32434a17b57175b443805b2c5900' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 22 May 2025 13:53:13 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 22 May 2025 13:53:13 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 22 May 2025 13:53:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 May 2025 13:53:13 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f6217bb5b7f1a95efe567548c35356165dc66ae69bfe675bd4d750bb78b516`  
		Last Modified: Thu, 22 May 2025 17:33:09 GMT  
		Size: 6.6 MB (6619363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9020a2695371d3927fa6fb04d07c6ee8cfdbdf0c94ab360a4d3e121df860ce`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9b02a9ab09a6778612e627ead79927f9eab9b1f58a792a27d86b207e883eb`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine3.21` - unknown; unknown

```console
$ docker pull nats@sha256:2adcfab66a18b065b7c3a97ae3a3a6266b23138c34d08229363bae6d3eb99f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b88a3ff73d885d4df2ea9e8203001daa5832c33dbba49d1127c7ded5b3724`

```dockerfile
```

-	Layers:
	-	`sha256:2e6f543ee243ec43d02935e873e329d235728c7301898d56b1cc48bf41df88aa`  
		Last Modified: Thu, 22 May 2025 17:33:08 GMT  
		Size: 14.3 KB (14317 bytes)  
		MIME: application/vnd.in-toto+json
