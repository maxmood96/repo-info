## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:3defbc7042c9287d78d336478981bdf2410928e48fd8a9504755509633620376
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
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
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
$ docker pull spiped@sha256:3565ca7a9021c033aa2f9aa3fa95ec43241003635fa8669990453c55ff55e1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa0a984328f7027e356ee0aa46ff85666d4fdeec5eb2d5343a30a9dbe998445`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3f2d3fc3adfdd301f5e24f24c5392b9879a1b61f182e7752a21cb03e6aeb04`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972687789bff098d9b33d09c024319254bdf8dcd29abb2bf072809733c79f49`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37195bfd737aa3f22ef0dd56d792afbe7e88b9c83db3bf0e69cb557d04d0d152`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 219.5 KB (219522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9420b682506ca5859fc3f4af6d59a5ca6fb329a69a869e8d7d0766374eb87ae7`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f38e672eaca427117d78c3580183cebdd51913b95165f7a4fecbb7219aeb29`  
		Last Modified: Wed, 08 Jan 2025 22:06:49 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:c1545d907101296a82932a434f77b80a720493d1f158f28037a360c849c6b869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 KB (88588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af58e3c42e72d2f836cf482efb095b5869000f90e0fd8c744622051f65cbeb6`

```dockerfile
```

-	Layers:
	-	`sha256:802dad5a525c4dc8453a7af1d74e5f8e0f8e9db9e0b53075b1abb70ebcbcac58`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 74.2 KB (74152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31d587a383d8f42361fc2623919a7a23e16261c7eb1f51cb4aa140497be4935`  
		Last Modified: Wed, 08 Jan 2025 22:06:48 GMT  
		Size: 14.4 KB (14436 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
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
$ docker pull spiped@sha256:79982546d0bed357c3b7f570dab84958af0f189249fe28e89577d41749385d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f4d20594fd72e32a00a9feabc004f2a01714cd681f91d6012c8315cb905ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdd5abd6a9641f814dc31398b1f41f1208ca3c43eafd4a1c8885cb772431cc5`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473a53dcc89c2068574226fb084968b4ffe7be1af4300f024b632369f8a8c233`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 7.6 KB (7561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113dcefb1595560f60660ee7a991d2b59509bc30e01ceddb44741db3ef240384`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 215.8 KB (215788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659fa19d2020016e65ba76874ea424e5842bf892ef9cbb0fb225538f1e187cf7`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff65919c3bd12f584108c1e36a3685a85470a54c58c385eb56d95175f5ab8c`  
		Last Modified: Fri, 10 Jan 2025 16:34:52 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1fe29fb7531300754b92edf6a17cb43bbf6bdccf3669dda2f135e21ecd7bc35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d832c44e71bd3c5c8e4af761656415c7160b797f2992b90ae6ccd9ad1d3bae`

```dockerfile
```

-	Layers:
	-	`sha256:22ce3c1ef9750e4e84284967ee5eccca34b598a38edbca4cd170feb5ca477190`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 72.2 KB (72175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aff322ae82649ec4042d09e767199a7e60414c2658b767de2a09545e6bc998d`  
		Last Modified: Fri, 10 Jan 2025 16:34:51 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e65076fea6d36aa50870267c91ec6d95243f1fb11c28be61a1d14cc261f1cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3684480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f24babcb5d8bb3f6840a272a25b4d6bdcfcea3fcb3a940801065c5753d9538`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe78366bb027e03c42216a6e1d382df7a3ee78f1471f4c62ff2d535ec78d8ce`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644fc493adbda1d67b109c8285fbc4e3c1d916ad0fdd4e52b1d30d0c3b5a8b83`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 7.6 KB (7558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b5aca5c5549a3999391bdaf9bfdf23ae037d07dd0278bcc20a847480979e45`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 212.2 KB (212205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176ea9af669d43767bfdf3ce63602addb4cf802565986d5dc091d471acc30fe8`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d93146a4a9bfc5584cd3df6a564e1f4ed3da6472cd8f41e6e08d7031d0c8114`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:93f271bcfc043724cd8ed10b5a81e091db12c7c9d2e449003a555df7b3164e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 KB (86446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388d85c4a8c82382bf1c9f50c1c9b6f983abffb8517c5e88afc7ecb4b51d7af`

```dockerfile
```

-	Layers:
	-	`sha256:2f690c178f9bae18125b1de0d54e1b4493b26e2f974141f5f5fd3c9d3a20c6cb`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 72.1 KB (72145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8043e5e2fb4d14db768fcedf2f5c98e22493faee4d4820a99c0fb644ece380fc`  
		Last Modified: Wed, 08 Jan 2025 22:07:57 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json
