## `golang:tip-alpine`

```console
$ docker pull golang@sha256:7238ef16d548de397286a176693742a85bf70964a92dd0abf179f6870ea8db10
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

### `golang:tip-alpine` - linux; amd64

```console
$ docker pull golang@sha256:2b49d1063cc721dc14cbd296895f02cf58ef6575dbfdf50bd565629e9ec4b0da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87178050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e483c5c48eb7256c5b12d9c05e90b3a10f4abc0805d496e59d234f543cb88`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39b3cfe968cb9c492a7839761a6d1bb285c24d548485830f0908695494c62a7`  
		Last Modified: Tue, 08 Jul 2025 21:07:17 GMT  
		Size: 294.9 KB (294920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9b1bf1df4ddb6cd2f3ba43fc263309f8c370fe86f15d3de62305a26c4885e3`  
		Last Modified: Mon, 07 Jul 2025 21:08:01 GMT  
		Size: 83.1 MB (83086126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8cda94a4fca7b996b468e9e26b6d30815ecb1a71296fa412a52d9db4fdb9bf`  
		Last Modified: Tue, 08 Jul 2025 21:07:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:29aa7d5b81a340469a435d41fc12912dd97e18bf58814331188258a5efe7d477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 KB (221207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74de78f26f75043105373e56375b927ddeed859c3bcd0bd94329aa99c3f68f88`

```dockerfile
```

-	Layers:
	-	`sha256:c5c5b1c0f8b0844e27a23e50a159c9740af946c5d08d3796d0b030c9e7c7aee2`  
		Last Modified: Tue, 08 Jul 2025 20:30:02 GMT  
		Size: 196.1 KB (196069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40407555a46365a03530391166eeedab5e96880caf2133ea284109a4efcc5e59`  
		Last Modified: Tue, 08 Jul 2025 20:30:03 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:39a4b8331cebe0f550759b258c0d55ff810538234e911bfcb51316f24b9c854b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84229884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ad26a8adde1134164ee585820e7d95e8db607962761ecb7fb0d6e069687695`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1a66512d0d840a56a8c3fcd61678c4f71bc9949c18f7ee679feb7494b20e0`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 296.3 KB (296292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100ca644ccef217b691cf701a2d3d00a0f16c7a7cbfa7f84fdba88c2b1a0747c`  
		Last Modified: Tue, 08 Jul 2025 01:56:56 GMT  
		Size: 80.4 MB (80432506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d7cde6f961982d13d0d24f31f59bc92738660669ec209539a21d15338d88a3`  
		Last Modified: Tue, 08 Jul 2025 01:56:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1b6999e773709b65ad184821a1263def9c81a9ad96b9bfe9706ba5b2d0464dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7143f0b87244e154085a893299618510be4fe9bf3832db7f863e9c85f9b04d6b`

```dockerfile
```

-	Layers:
	-	`sha256:2b71cbbd64816ba5207706c72840b5ae3ef6e5f0bdef42d0885d3baa520fc4a4`  
		Last Modified: Tue, 08 Jul 2025 20:30:06 GMT  
		Size: 25.0 KB (25047 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:3fb52eec6be13131fb55893474cf23313441c89021f25d9b2249d1d3b45908a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83695650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb94cb3a9125fba783e65c5dbbe988be4f6231f36f9d1b46dfafa5415f0be0b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6c9cae412d8d42471b3ec2789f87569712940a14bb5b06595436c95f2904f8`  
		Last Modified: Tue, 03 Jun 2025 13:31:36 GMT  
		Size: 295.2 KB (295232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69fdb869efc0a02a2300329eae27592000268e157c8997d8c67d1e2518080e9`  
		Last Modified: Mon, 07 Jul 2025 22:02:14 GMT  
		Size: 80.2 MB (80181079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d1be18a8c565c116d98f3e7127ab1d5665c55f5b7f124c35f6efbcb3eb0072`  
		Last Modified: Mon, 07 Jul 2025 22:13:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:18fea26719bed2201a0d07b14c2223e8153aae3b87c66e6ee576cc484806b795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 KB (221353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66746edacff2762491c0128b6449fba81895a6de37f2c38455e9c72c3e66275e`

```dockerfile
```

-	Layers:
	-	`sha256:6b83243552b90b96533a39036360fdef56f3acbb96ad8135ee87a2b422c89986`  
		Last Modified: Tue, 08 Jul 2025 20:30:09 GMT  
		Size: 196.1 KB (196091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ace6e4dc7ded65446fb9fc9107176637324c4350d17e2f59e4c94486067c229`  
		Last Modified: Tue, 08 Jul 2025 20:30:10 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2a9103ba6766056869a9db3494580ac606ae4c4338bd0360454e0cf3ae9db951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83485193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba5592b58e304c8a639c7468d387fcd5aac4e9b3e1587622a6103f0ccf2c6b7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975e911be57d720d2024fa2b480856a5d20ec0b97f61e13dbbc8463d3824328f`  
		Last Modified: Tue, 08 Jul 2025 04:46:49 GMT  
		Size: 297.9 KB (297898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fe74c58f17b8638ab4c828f8d4b865821c43447e64c8cd4bfbde5a810c7b1`  
		Last Modified: Tue, 08 Jul 2025 05:43:08 GMT  
		Size: 79.1 MB (79051196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44176770c7b1101af9fc4b5b96ca50b4f446e6ac8a484a1babfb07ebca97ca6`  
		Last Modified: Tue, 08 Jul 2025 04:46:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:7a8c6436692dd804254839c07a9257c22fa79d520417effe59a1b3e6260fac74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 KB (221423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305b08c7bf068d06d17d62d10e440cfcc93eac246d579e94e5337c76ec6c058f`

```dockerfile
```

-	Layers:
	-	`sha256:bec0c87d63587785a2d6cf633dbc04d2d2b5c30d65740d1fbc61778a80880d85`  
		Last Modified: Tue, 08 Jul 2025 20:30:13 GMT  
		Size: 196.1 KB (196125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c75048dc7aaec9cf9246a3a8eb616eb44e72a6c106e09a1d53a71e550b4f432`  
		Last Modified: Tue, 08 Jul 2025 20:30:13 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:8bf723f379d5ac3daf62435a3a57eac1866707c92166b0d6cd98770cae9dab7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85732194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5d7771a39bf47239c6ee50cd2f87fc795e91513369d7d6924c2ee1853d7ef0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1be9aa1c0eb013dc4030b2b4e436b66a9d60e819dff5812e380c329d0d7ac1e`  
		Last Modified: Wed, 09 Jul 2025 04:34:21 GMT  
		Size: 295.6 KB (295628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fd65ade23887bad8cc24159556378a6549464832612b1c87e5e65754cc9685`  
		Last Modified: Mon, 07 Jul 2025 21:08:46 GMT  
		Size: 81.8 MB (81820379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f15e93ce1fceedcdd6dace103307bc97f5e6711c846678a1ab9b4838f6927b`  
		Last Modified: Wed, 09 Jul 2025 04:30:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e9f06ade14ce0e6a85c31aba7e6f403d7b005306652e77fe34ea76e73a4c6db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4fb7cd9cdc902c2d41c3f47d61623376c9b326cde35a09b949d3d51da1bf01`

```dockerfile
```

-	Layers:
	-	`sha256:9f6f0f96903a0cb5ce100df3afd3d634a732403479446d210e2338056820ce0e`  
		Last Modified: Tue, 08 Jul 2025 20:30:17 GMT  
		Size: 196.0 KB (196030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a9b3e2b7ae21729aeac060c28bd01fd22f710d927ae7a8ac13f3d510f8d078`  
		Last Modified: Tue, 08 Jul 2025 20:30:18 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:872326fec0048c218360281e648d3e7159ba056f015bacadce84dcaa9e0b39f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84387763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264efc6c1ce3e06704b1a887929fe976c46de87f3fcf0c5b46b5637cf78dd319`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2422959133b1a526eceb8d25136473310e8ed772b3f3d3a7f23ef8aab1a052b`  
		Last Modified: Mon, 07 Jul 2025 22:25:45 GMT  
		Size: 298.3 KB (298332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22b55aa5c49337c93ecd39f723f408177c4f428404ab6858571184b51126cd1`  
		Last Modified: Tue, 08 Jul 2025 00:16:14 GMT  
		Size: 80.4 MB (80359086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae477155aea28b8319cec562393535dec9445c67de7b7d03eb55c6305af70bd5`  
		Last Modified: Mon, 07 Jul 2025 22:25:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:35dc8db3792a282919ccaf47c124fc2fb1fa63fc1e0289a353578e8e754f6550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377b565897cbe6586969aa2815e32371d5fe7bc9efab1fabaaf80be243c44e62`

```dockerfile
```

-	Layers:
	-	`sha256:1c1f0b5e107c07721ef5054ccfdfddec8fa2c718699e9519a059871eb0fcbe14`  
		Last Modified: Tue, 08 Jul 2025 20:30:20 GMT  
		Size: 194.2 KB (194166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05f7f369c78a06bcca01715103084c0fb820095066674811bab3ccf54fc89431`  
		Last Modified: Tue, 08 Jul 2025 20:30:21 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:ed571d7e55f86af561f09f92847f69e1f20f3e291ffa4eb0ede4f80b80145093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84364328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b3a39ea5c90235ce5d4b38eb5efaad937c6f0156884e37fa16727d1aadba9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850bf8006499bec04d28fe13dec3efd4cf9075748d5dcf5b6dc1415aa6aeb8f0`  
		Last Modified: Tue, 03 Jun 2025 13:31:45 GMT  
		Size: 295.4 KB (295390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950d2522679e808bf5b0d11b3e731c061e0d65a03b5eb65235ea8af4cb3df86f`  
		Last Modified: Mon, 07 Jul 2025 22:00:28 GMT  
		Size: 80.6 MB (80554969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88baf821bc336209b3e7ed5e1382b8d1c5d95e2fc624096b6a4bea430e9775d`  
		Last Modified: Mon, 07 Jul 2025 22:00:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:dd844b3c287cdbbc706d1493a41bb3235256830f5b316ddfd4a8db08ddb19837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcd4a6a4451e8b410714b555bdf16b038f5e200e50e77c5ce54930bb0f19c44`

```dockerfile
```

-	Layers:
	-	`sha256:dd7aa2669f9904ce4cf590469f39ebf82cf86c544724ac7901b72ac5f817476c`  
		Last Modified: Tue, 08 Jul 2025 20:30:24 GMT  
		Size: 194.2 KB (194162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f38f03576e534c1c7f10c4aa16454185837a6ce6afb1ccf957cba5385e113090`  
		Last Modified: Tue, 08 Jul 2025 20:30:25 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:6ee9dbc91e61f2bcc3e92580d4276ad60f63979a7baf0eb4ad250d1d2127c8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85541877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44006cec606512bf79815fe0beee90bfdc588a12622da3eac12c77fe3774190a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 05:23:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 07 Jul 2025 05:23:24 GMT
ENV GOPATH=/go
# Mon, 07 Jul 2025 05:23:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Jul 2025 05:23:24 GMT
COPY /target/ / # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 07 Jul 2025 05:23:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac74f8629eb00ddbe16fc3ec1b20b1abfcbc89e9a6ed4dac9e1d4663eccc2e`  
		Last Modified: Mon, 07 Jul 2025 21:31:41 GMT  
		Size: 296.2 KB (296226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff319e613d7718d33c97b2a4d68807464c2ed71607411d5eaa89b10ec085d5d5`  
		Last Modified: Mon, 07 Jul 2025 21:28:58 GMT  
		Size: 81.6 MB (81597964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b0555bc99255be90e678d4d8eddda3ed221cbba64336e87c34c8edf0e14adf`  
		Last Modified: Mon, 07 Jul 2025 21:31:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f4f8cb2d12373e90811ea13458204cf519178844544787140aa3fcf2fd7b996b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679c0197b1e637983966913509a14dd4d2b080c4ba38e09c142d544d42c772f4`

```dockerfile
```

-	Layers:
	-	`sha256:0a6e887b9b72ee1fbf0e25253194380b8d5b8c7e5ce436aaf473b5b3414e44af`  
		Last Modified: Tue, 08 Jul 2025 20:30:28 GMT  
		Size: 194.1 KB (194118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e0ea649121d65650c3be4f60a91f4d49b66cf231d42d625c7d7fa28549990c9`  
		Last Modified: Tue, 08 Jul 2025 20:30:28 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json
