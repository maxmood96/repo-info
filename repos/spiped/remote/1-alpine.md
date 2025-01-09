## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:1cc3af56b225b4ad0efdbe4b77f07824c3cfc30e33643acb8beae53d97ae6e11
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:924e7f71ff8a6210c218250cadec128119d344f463da73b7435727f3b79f8b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3860004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002ee6ce7d381016e688df520b2d8e452892442cc9dd7d7fe4f2fd27e10bd9cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4d648a75810ee71e4a811a07ea0f0ac2c721e73e72187e9a1516d4c4c5ee6f`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe07a72f4be9ce0f108da046cf545981624f6b49403d76321af17c0c395f286d`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda92c005435cc07d0f9aeede336b39adeacb3d2b63892bd145844c2ffdee52b`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 224.8 KB (224801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d408faf96bb5ca591f0228176fd9fe8fcadf008b4a1d270852fc8c6e4ba93ef1`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e29defa7a55825f8f61eda130cb04ee394d66bd712f70709ac7053a248548`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:bbb6e45e7eb3500533fd5eb9b6e02cbb71696097c25c94d70ad5011ff89719b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ed9b89a1c4bf4f119be92f17b9244feb5432b0aa95a99a543b91711e64d2ff`

```dockerfile
```

-	Layers:
	-	`sha256:d6dbec5f27c384596dd421778e731d1e085e3759f6d847458fe59a756fb7ac42`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 74.1 KB (74096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb9a321a7ee93632ee08168238d08c393bd8977dc0b90058743b7578fd3ffc57`  
		Last Modified: Wed, 08 Jan 2025 18:12:47 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:3b33305e723d928de0ceb007a192d635fbcead1966adcef42495013c151ab1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3908b8302a74d29d2ba4f9fad53ec5dae4d694c59ef5e425f9d3b4ae6f8e82c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3f0630555eb148818822fb59b573ef21353f360d8de1a31a9d923807ee4cd`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779a48568101672a32588570e7ceef7c0674397cbfa25ee720cde2859ab94873`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 7.5 KB (7549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a21818ff816934f603fcd2d4cba9f12db282bab07e3069da21d7578259ccec`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 209.4 KB (209360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908425f61ccde4470882b7fc3250f120af7e457373de37561ca1bc2c428156fb`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d99959ccf8e07e46905c21480b4a1efde735673420d31417427ecef2146095`  
		Last Modified: Wed, 08 Jan 2025 21:50:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b7cb53f249d979d695f81563768605e871ddd1ea8a0819dd8dd81dc4987a573f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:755f963c27fded64f7e3f6ff08da27dc1fd056f8030a81de4cb41f27e65d037b`

```dockerfile
```

-	Layers:
	-	`sha256:696c936ae51f846bce7be1a6d2dde5c03aa3b71ffda41e1e6b2cf2a621f6cd97`  
		Last Modified: Wed, 08 Jan 2025 21:50:16 GMT  
		Size: 14.2 KB (14189 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:ae8dad9afbb0cc8a3d199d4f081244152b6bb25a314d1c1b53d2015cb7a3148c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3307454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db4e1533dc661a40478a134b3fe58301335db42d8f87ae18e6918ff38e81ae91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7fdb315d3c34eb6935e1b7deb703093f5317800ff4d8b3936d5f771137cb79`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3360ef971eae752027c0ac2e924cac0c91b7f45b5099026b2a8f4be3279f6b5`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70480e7090e82ed5e217b413501ec1d1ac188d14349be7aa351d6ebc4bfa572b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 203.0 KB (202981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa024b8e7a4dcd96a95ba7c408a6b6bf086e89742d975c9ce4fdfcfc7cabc1b`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4350bd55dee2c6c0b00a05b33f36a79b911cbfa491acf490c5bdc593d8e3e547`  
		Last Modified: Wed, 08 Jan 2025 21:55:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:374da430416cd603b6845710a7b6b98de8856fb9d596f167daa655438d68910f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb7685b3853e3be4a1172afeae58a3bd43dbc7f6bf21565a8d6843e6b79559`

```dockerfile
```

-	Layers:
	-	`sha256:d4af9f6a3307489ccc6bd25b80644c322c26bf5739a42dab919b2dc03edff9ab`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 74.1 KB (74132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d585d482698adea511246e8d288a1602e3c63dc4f235cfa0915b12ae4b080f64`  
		Last Modified: Wed, 08 Jan 2025 21:55:29 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:fdbb12824b88c7b18859c04cc8fbd31d6ccc84c135af3e8a2df261b38a10057f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4308713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c767cc3f98c29c28297080fd7c1d27c661584beb88a486df47d28053b48a455b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b19e3d04ec2b9d3001f2787d68b4b449f3e689a0d6f2f471a0386c4cfec4b1e`  
		Last Modified: Tue, 07 Jan 2025 07:09:34 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc909cbe9bc37ee1c83cc781499991aaf16f74091b8b3dc10087ccdb9cd8bbc1`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b65ae735ee44407b76890196851e37d2728197b6a257a567737116e76a178885`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 213.1 KB (213077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac91bc929cadefcfdb1a75a0f2f5c44be39a2a126e2316a777d34e777cf25c0`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b00577687504dcf1da7210e90b7144500242cd716a98cd945aee7317ff2b853`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:278cb7494adb7b010caaa0fc5a6d18b19dde2a17677fef36fc1ba4852e0163a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63b31a8595fc81a7abeaa1742e609cb7d6ddfa29e8382e0f625ebf7511d3679`

```dockerfile
```

-	Layers:
	-	`sha256:62af3aeae92f48ea868503a424e93b9c08260ae07dca8e88bddfca56b1593592`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3ca283b7fa2827d2d9cde0670b6d868f61d5adc4b68bc70bafc06cf1935e83b`  
		Last Modified: Tue, 07 Jan 2025 07:09:35 GMT  
		Size: 14.4 KB (14435 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:92342ba21763b953dae5124e2470d7b310cdec0e1aa1c278c715dda9eb6c5a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3715310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a710174a0b36bde4dc08b5531a97264b1a956e7b607e3cb81fa4ed42446333`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01646177e05c873338d049d0058c8cd923326812215a3897564adbd669ee56f`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf3460ecbeac950e26287d1cf9fdf47918bf993988d851835f852bbd5707856`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69044b34b50595fbdc42e577dc79e206d3962968154ec6fbf18024dfe607c6cd`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 235.4 KB (235383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e2fe84ec006ef02b90eb19d8de0f72b59b1f5d3cad78ef6d043f1ea320d121`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8feb2512bb10b2b05cf6ac1f623ac53ae1aaaf4d759aa98618bf0a96439d0c`  
		Last Modified: Wed, 08 Jan 2025 18:07:24 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f82eea4e46a614570a5475a2c2999ebdb44416593095c39bfe597dfb70954205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 KB (88337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c43d43c6b18f013ddf9e79c05395cc1213c96194b62e9231a34602566ed737c`

```dockerfile
```

-	Layers:
	-	`sha256:662bb99fc24ff68d14f1e276dc7da9f11ef9f56131659d2a511578d1c4547a4e`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 74.1 KB (74071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab4679badb23f30ba84ac1e7ab274f8693e730ac87dbfac78c97707c071c360`  
		Last Modified: Wed, 08 Jan 2025 18:07:23 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:62a8529f4a88431c2c8453c2198b9f19f5027af08967a818ceb2e9f5485a2d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3806729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b6428f7bf466f0e03b157ec2507c547f21126e87e9b2e288213771e8ccfd2d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d50e862e95a905933f50b6440c968976a25afd06a9808138b7b662be556076`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca1e9dba23dfea2ee87d2657bcd8e5e57a74b668b777c31cdf12a5a688c9e23`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b2864e003337f2f79f0ebbd5d8f47c821a711805de5ac4aac9a3f02a5d06b3`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 223.4 KB (223364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b04a1708fbc0147d4ef6fdeb564449a7a41b7b0e5df2aa27a1441946c81598c`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66b8e9453e2d649488c8d053b0d1d4ae5e3740489586c6bb32f7eae7a3ec003`  
		Last Modified: Wed, 08 Jan 2025 21:29:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:641f93fddb6e6a668353356d78a708a17b7271ab06e13c5d2d1645d499c65794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1511f0eb48159856515b99abf8dee3e56263f52094148ce660d713454d210ec3`

```dockerfile
```

-	Layers:
	-	`sha256:55e5c3dc4287df2df2d9e20c08f5cd46d57a5616350e241f492bf844c18956d1`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9f348d15a848da4a767fe70750751a3015a5b347ab3175554ad77137d71526a`  
		Last Modified: Wed, 08 Jan 2025 21:29:14 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:da6591d15c86f3bf43fab6ccc0035a0650a5756859870abdd3276d24eedff6a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5551193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8476d53de131526ad9562517c1b099c24ce9385a5730746d1e83247619389c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa88ab9b012a876209b14e6deee5c7982f819f8de6d7b9ed357459d28c597e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdf98d05f4226e17074c09dea718e6191052243811401bf5891cdfb4f1005a`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cc53836a810c0768e9eb515600a82be8862a3129239035de56d851625f2890`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 2.2 MB (2170750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd669ab852fa6faffdff5b54301703ace4f36faf005d628470fcef6f3ba9296`  
		Last Modified: Wed, 13 Nov 2024 01:24:29 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ad710654b9957b395b764e0751fb8ceb335cd3970bee0870c731d0c9d1631`  
		Last Modified: Wed, 13 Nov 2024 01:24:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:35c0217a072785ece237b37268cd30f7410f423b96bd889e56db03a674044795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f8f74486982bdb4f701b16321ebb5b430c4a06622f6960273f474bfbb2188e`

```dockerfile
```

-	Layers:
	-	`sha256:88a28221c4fd9d156a4ebf0935fa189d8524bb92c8fdc1d76981cf7435c2056e`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 72.3 KB (72257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a28652304d303135a92cbe69570122aaa332626746b8080a921073de8775bb3`  
		Last Modified: Wed, 13 Nov 2024 01:24:28 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:2b056e84c73867952da7b22052f17a7df808b47516a5bb83b8ee13395dc5923d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3674138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3595de50a5f32e15b6db59451eae6913f4aba96c241c1107b30e84d282d1c841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc1c58e04de4e903d567e58827a257047fc49b0eef9f83f28092313f82cbde8`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797ce336a1e875ccc1cd81f71aff2122e82a35cc94121592994a0335577d072f`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bf37cceecc9d224e361a1ad76cf766d3c66622e6bf682fed3bb15bb73ca6b`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 206.0 KB (206006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef3d29125754db1b1c388a568ccaa80fa40fc0c2b9078aaae244b5a314eaa96`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8bb164b00a2b113f38d85168412b681bebb59d60c7cd5639f5d336feb07d30`  
		Last Modified: Tue, 07 Jan 2025 06:19:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dfa792f46cacda3f23b902f295f4c89e1405c9ecbbf35d3dc361b490cb5d2bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50a77b62b00200a0d22583cee5739c50ef87fac5617e6a874a57b6ab43071bd`

```dockerfile
```

-	Layers:
	-	`sha256:2f8c8e6e444fb4067b5793ed502feadffb90b238f975366fb53d0618681dca0c`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ae978c3bffb1c7f0cad075aee069f572a9513bee2ea6a85ca5f5f145836bc1`  
		Last Modified: Tue, 07 Jan 2025 06:19:19 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json
