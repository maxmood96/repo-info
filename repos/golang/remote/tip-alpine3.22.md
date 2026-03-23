## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:b0be12127a47c26e46d469f5cc158648cef00d959d9d058c62c02143f37320dd
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

### `golang:tip-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:43426c370b143cfc7c30ccddb2bc73dda0466d0c4da8b7b7ea946ff1be146abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98023072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e55aaaa7822be3ab3d5b0d3d3b65f5194ffd69b483a95d8b7c4576f359261a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:14:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:15:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:15:53 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:15:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:15:53 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:15:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06e267ed5e3ca8d934a842f824ced4094910a9dbc30ead19e548d16fca4857d`  
		Last Modified: Mon, 23 Mar 2026 18:16:10 GMT  
		Size: 291.2 KB (291159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14da6971e9abc1b6c7a1372792a609e9cf545f9f36ce489f1bdacf534e2c8abe`  
		Last Modified: Mon, 23 Mar 2026 18:10:59 GMT  
		Size: 93.9 MB (93926880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1827279c298acf9b1edfec35f1679a6efd0b3c457b9eb44efaf6fa2a7e4db9d`  
		Last Modified: Mon, 23 Mar 2026 18:16:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:88d950e835ccd3bac60940735a4e7d9e13ae603f6a9ce42e52671809ce10fda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7f426793d9c79669024491e12403200f0a74d4b351c0c43f88064bbfedb466a`

```dockerfile
```

-	Layers:
	-	`sha256:a64f72a4de22cb887fdcdab299b962696439657c5cba74ceb4ea74dd816126fa`  
		Last Modified: Mon, 23 Mar 2026 18:16:10 GMT  
		Size: 195.0 KB (194984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2becdaabe17a16bb2f28afbb25e09682ce619e81b55aded58e41967fca66d6c`  
		Last Modified: Mon, 23 Mar 2026 18:16:10 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:d7af232ec5a29231e7cd26263b8c74d88884ce881ca00166cd96ce3aa44f7cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94120313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0c17e84ff04e616befb43e0e92436d2114e058d12519f1e418dfd081a75f42`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:07:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:09:55 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:09:55 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:09:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:09:55 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:09:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:09:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189f536970b68846d26064514b679140c3fe9d859d79db2d4dc7d05e3b4d94ec`  
		Last Modified: Mon, 23 Mar 2026 18:10:10 GMT  
		Size: 292.3 KB (292325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7dd031b7d46ac68f8093f5d3ca1cfde9444287482bdf5554db65238123ea`  
		Last Modified: Mon, 23 Mar 2026 18:10:04 GMT  
		Size: 90.3 MB (90322785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cf3b6d7712d39d0c8c6d9e9f468ec2ab758be89f61acca09f50cf4e34febfa`  
		Last Modified: Mon, 23 Mar 2026 18:10:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b88cb725d84990c11982bf2c1342c276c764663d36f6f677c85b395c4455095d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35516d34a8ef0d620688b6dd9a7b28eb600d3e7bcbab629ab85ccf82a7df0324`

```dockerfile
```

-	Layers:
	-	`sha256:ae31db0228751008eea9860b9ba09f75747c9289a4d71d9736f1fdfa9cc14827`  
		Last Modified: Mon, 23 Mar 2026 18:10:09 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:74396c7522b403525fe630d88d42268d052abd6658d803c5785c5be487ed85df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93557856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1886e010ec0f94cf26abc5055966c902ab583684bf0bf684b7c59a42c41a49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:06:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:09:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:09:38 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:09:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:09:38 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:09:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:09:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0176f4dbda2e12dcb05ade8f2e3cc40b6665face6a38f7858cc89c6345a4a66`  
		Last Modified: Mon, 23 Mar 2026 18:09:55 GMT  
		Size: 291.2 KB (291205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3fe8212a49eb41f6a4366c38fc20cb7c161e830a9074b4c7ea09f324d1f7e0`  
		Last Modified: Mon, 23 Mar 2026 18:09:57 GMT  
		Size: 90.0 MB (90042864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d33211469dc7585834d4109ff27aae20e06cd92c06ff435f71115ffe72f14e5`  
		Last Modified: Mon, 23 Mar 2026 18:09:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:405b519db8b6b1a6122ffe904a87ce22bc9ff568f75ea13dd80e8c0344c07897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289825fa3198c5ad1973a38a53d5311ac586259022d8b8f1c4293a9ae379e4bc`

```dockerfile
```

-	Layers:
	-	`sha256:7ba786750cb3f35bb0ce82bb590fd39be415d1763b7cd7fce62f6194f5667b75`  
		Last Modified: Mon, 23 Mar 2026 18:09:55 GMT  
		Size: 195.0 KB (194988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd5763df9a2b9484f1e62d1cfec100e6323d08583e0797936ab949808c30366`  
		Last Modified: Mon, 23 Mar 2026 18:09:55 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:068318f5043141fc9947050f5b8800f57043abde2692e3f2afee40987e0fe844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93466669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95378333e79e2169750b8a3508d5545bc831e054d84a88c76fcc7325aab8a82`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:13:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:15:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:15:27 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:15:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:15:27 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:15:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:15:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0f61fb42404f4b567b0fe571bd00164ed7b8a7ba5fc6aec72205fe49687814`  
		Last Modified: Mon, 23 Mar 2026 18:15:44 GMT  
		Size: 294.1 KB (294094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d89156bf69d73fd72aeaeb2ffe43a084d18a5918673e90973fa80f2bd1106c8`  
		Last Modified: Mon, 23 Mar 2026 18:13:03 GMT  
		Size: 89.0 MB (89032899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521c08da9bdffab259d50540511866cb6bfcba810eba948f6734c5d10b4041fb`  
		Last Modified: Mon, 23 Mar 2026 18:15:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:53a409bffcbfb015c68b08fc5116f13a5fff427ccd6fc17b74514869509b4e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafdb4b5314cc65ec745a030099e93a3d5e9fddd11f85b675291432d79460308`

```dockerfile
```

-	Layers:
	-	`sha256:b00d1270a9664c67bc0f66cf6af4f90a0f0ccf26e0436c21b082071fef34cb91`  
		Last Modified: Mon, 23 Mar 2026 18:15:44 GMT  
		Size: 195.0 KB (195016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:085cdca4ba3b3ca8d6d3c899cac382f5b44d50ef5c7a3d3330268c709fd162ad`  
		Last Modified: Mon, 23 Mar 2026 18:15:44 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:c3044362c77c0dd850986474cce24efe54f83645601a0e4378f187d9f84a41cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95645135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fec5e4ba9aa14af8faa3a5b4ea1d5b0b1a0da0303665f536765d37da56b061`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:11:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:10:49 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:10:49 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:10:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:10:49 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:13:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:13:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da92df906d043472a8a0404937db330ea53b5cd36439415bccf8656d6477ec14`  
		Last Modified: Mon, 23 Mar 2026 18:13:44 GMT  
		Size: 291.6 KB (291628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264f7e91fc0f0620e6fa158257cdbe7e1dfe1394592c1026625d9442a0cf94`  
		Last Modified: Mon, 23 Mar 2026 18:11:19 GMT  
		Size: 91.7 MB (91732617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3262ea64ab805f87005b07b0ad48fdf8a70e4bf5f13340dd08990e7124e965a2`  
		Last Modified: Mon, 23 Mar 2026 18:13:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:986fb614ca31026ac977a99be514e48adf7997f2d6574b114ce01615b3a844e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1814b393c5b1f946d0e2c7ab763ddd2c592dd089513d4bd045cf10de36aae57`

```dockerfile
```

-	Layers:
	-	`sha256:e26be3a517aa4c32dd65a6fa747e47b051dfd6cda5cdfe53c1b3d61bbb21af80`  
		Last Modified: Mon, 23 Mar 2026 18:13:44 GMT  
		Size: 195.0 KB (194953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2157497f1e398a54ca0cd43432dbf9ce51bee8536a386e15b4187d38eda5d538`  
		Last Modified: Mon, 23 Mar 2026 18:13:44 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:df336130835c62b0a3a6cc5aa6f0d3a3c5bd5fea6912bb6413b6b863a59e7d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94754367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5c09478b8643d7b0b94e7b820049d702c91c642262b653ddebaf944a005e62`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:39:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:33:46 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:33:46 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:33:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:33:46 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:39:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:39:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6a25f78c4fe7d260b311b328ded3f0d94a19620fa6b6fcbb74feb4746a81d8`  
		Last Modified: Mon, 23 Mar 2026 18:39:39 GMT  
		Size: 294.6 KB (294572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70a7a68b066f9965e7b26b52317270613e7319f2d2ec75b34f1e502d6ba09c`  
		Last Modified: Mon, 23 Mar 2026 18:35:15 GMT  
		Size: 90.7 MB (90725340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e828ab5c1ad9fd0e74852921f9a7616644e951e2713450d27b4bd89257f86624`  
		Last Modified: Mon, 23 Mar 2026 18:39:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:8a025644a4f617425bfc2463a8dff9735321cf1c067877216ed3758c4a9e96bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb02d56c4190aa6c7db1ca59f208f0dba905c933b56ae67b3fa31bf9b25cf411`

```dockerfile
```

-	Layers:
	-	`sha256:dca861130c301a5b600f4eff4ef6a2836e568df2201c08149d62577f48dd9275`  
		Last Modified: Mon, 23 Mar 2026 18:39:39 GMT  
		Size: 193.1 KB (193071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e38f0b1958e403d483002d16dc68d1c39f90df90a6f53e9b8b65f3c465dba0`  
		Last Modified: Mon, 23 Mar 2026 18:39:39 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:f0aeecec1b238134d9b2f59f1e5d7cc8e91b5271ac826d3fa8de6aaff8a407ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94713254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9913d849911b1a22a86ae89e9ca7969241201c27b55b1b0e9e0e82b47bff677`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:41:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:41:25 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:41:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:41:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 20:07:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 20:07:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2540b408e98980f08989b2a443ee35cdf7da6f3b7310d46cd1e63b1f1b775094`  
		Last Modified: Mon, 16 Mar 2026 18:48:21 GMT  
		Size: 90.9 MB (90904175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6d51cc0faa2aec06425a5a910476d6921842adbef5038362d888c3fb60bbb3`  
		Last Modified: Mon, 16 Mar 2026 20:08:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f5278b888af166bc61691740f56984aeec5145547449bcb30894f6c98302c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785f8ef59cc04558c6b26b14e022f355486bc5267e4e93973701c5deb43089c8`

```dockerfile
```

-	Layers:
	-	`sha256:1e1b25310def20f13a3bbdcadb0d9c83571de83e655c88e0aff7454ab1223c1c`  
		Last Modified: Mon, 16 Mar 2026 20:08:30 GMT  
		Size: 193.1 KB (193067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e1eaaad123788bf931599e93e511ec075f57d60bd487837c78efbfec11f8c1a`  
		Last Modified: Mon, 16 Mar 2026 20:08:30 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:bb51a9ce252cab9940e664d65721b05d313f6d8eaf1fe0d108916b0e25517769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97061853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85c2cba26d834e3d209cbbe69250c5ba0e971ec933591869d38424cf90bccd6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:10:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:10:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:10:34 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:10:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:10:34 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:10:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:10:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6f56b99ce63283934e1bc3e3a0d460e27abbddf6d690ef3bd655a557cb2a3d`  
		Last Modified: Mon, 23 Mar 2026 18:11:09 GMT  
		Size: 292.1 KB (292146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ef3b2e5174bcf54b94b5b8caec33835ac1e023d73b8c9e7be52d6d2ef4659d`  
		Last Modified: Mon, 23 Mar 2026 18:11:11 GMT  
		Size: 93.1 MB (93119115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc7386278a4a19e53a810e52a082208a1b3b67fe3d671918f4f826e622a150c`  
		Last Modified: Mon, 23 Mar 2026 18:11:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:cf1ab855a8cd6144e157711aed10c33b6dd6a7d46ecc9f643c0b6fa2c7b8edb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00138ddd2c904533807231aabf095696e76061d39bd43b945b0f4701c24a5aa`

```dockerfile
```

-	Layers:
	-	`sha256:763831e0ac8857aafd06a50da42ed493533e4a3af3459bcc79f41a2c7caee84e`  
		Last Modified: Mon, 23 Mar 2026 18:11:09 GMT  
		Size: 193.0 KB (193033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32aada7fc5ada85d017258f1860e88ab52e2eb9b6bdd737e5d3f20979ae918e`  
		Last Modified: Mon, 23 Mar 2026 18:11:09 GMT  
		Size: 24.3 KB (24291 bytes)  
		MIME: application/vnd.in-toto+json
