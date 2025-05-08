## `spiped:alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Wed, 02 Apr 2025 22:08:24 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Wed, 02 Apr 2025 21:50:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Wed, 02 Apr 2025 21:51:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Wed, 02 Apr 2025 21:51:29 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Wed, 02 Apr 2025 21:51:31 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Wed, 02 Apr 2025 21:51:04 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Wed, 02 Apr 2025 21:53:16 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Wed, 02 Apr 2025 21:53:04 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json
