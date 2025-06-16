## `golang:tip-20250613-alpine`

```console
$ docker pull golang@sha256:1d1ce4463969ce4be20e3a6385f5cae7b2109e4a4da83cd3ed434ebf332b701b
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

### `golang:tip-20250613-alpine` - linux; amd64

```console
$ docker pull golang@sha256:0b3710382a028b2c1349814c357778058c6dff6da668c3afc4d4bb8f8af8a0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87290894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0455f0d8620f6ca7051899afcf02308ae34ffdad2f3db5d702c2e685906b17c4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a71b5969dca0f7a6cd1fef1f8cdefe3d38618927931be829c8dcf2ae1f4cbb4`  
		Last Modified: Mon, 16 Jun 2025 17:54:17 GMT  
		Size: 294.9 KB (294930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995fd9226ac30cafc0afd46b4cd0a61efa6a788bc8ead02212a127058aeb6d31`  
		Last Modified: Mon, 16 Jun 2025 17:54:27 GMT  
		Size: 83.2 MB (83198960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecfb6fc54b124b75153eeffee3404ef48684aa9a88036fdcf5ab2195dbb5080`  
		Last Modified: Mon, 16 Jun 2025 17:54:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:37e55be31e77a00036fb7bbf7d2b3cae5f001c680a469b580626ed21da3632b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 KB (221207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa76097761c2d2dd0d8e46ada3e4e38dbd39fa24a080fde078f854c6602b07d2`

```dockerfile
```

-	Layers:
	-	`sha256:e9de0860669ec06be0cf59e4ccf4341621aed3117a17d2337c05f732f42b675a`  
		Last Modified: Mon, 16 Jun 2025 20:24:11 GMT  
		Size: 196.1 KB (196069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bb3eb3c3087d2d0fc25bf042be27f354bd6373b3a7fff6bf88b56677ddf6b0`  
		Last Modified: Mon, 16 Jun 2025 20:24:12 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250613-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:fde2479f892d29c4e11745a81798bef808d8e39ac40014b82760c12282054d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84317315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c93825fd5ac6f34351979af8444d05e54deabd0ab81d853b1b5179d39da56ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
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
	-	`sha256:f9d7b905f0aee2b36a5d9e3374bb05dfb61512e02db750c601c2c1ad98c6c2af`  
		Last Modified: Mon, 16 Jun 2025 17:54:26 GMT  
		Size: 80.5 MB (80519936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e78fe96e46e3de98ee8f4d34626137497dbce1445c8a542e83626249161b40`  
		Last Modified: Mon, 16 Jun 2025 17:54:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c7082503739f3695796867c37707883ad51532058ce5bac1d33c6910d71089bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243825650d23b563be18b1d0da2119e50f5bf208f81a069337f5eb9651570866`

```dockerfile
```

-	Layers:
	-	`sha256:e24c3c9fa49bdba4fd4181dcd1315d80b96e4914f2e0f29abbdc9b7272cedcbd`  
		Last Modified: Mon, 16 Jun 2025 20:24:15 GMT  
		Size: 25.0 KB (25047 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250613-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:9c859bba670f7c77f2f3651d5868c04ad2043825e7e65dc083c4794a04377256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83791362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907d95766aa7794005123af3a85c93148386d7afcb093b9c42659dcfa6e4b726`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
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
	-	`sha256:d61657cadfce4d144c231832da5fb28f3562535b7ef7b3db141bedf56ff930a8`  
		Last Modified: Mon, 16 Jun 2025 17:55:24 GMT  
		Size: 80.3 MB (80276791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32541bf860e4e527b9544ff1dcc85a62197dd9c609ab2740a1964c49f03de444`  
		Last Modified: Mon, 16 Jun 2025 18:03:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:cd1616012a65ae939c4f5992bdf6b72876df06b6eefeb7df6a95e17e3bf94378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 KB (221353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e936bd91e608ba6c0c19787073b8bd7f14b18de325d5c55caf7657cd0f198f`

```dockerfile
```

-	Layers:
	-	`sha256:253d93cbf8cc363939a16d4776bf8a6b2d6d57afa675b73be993bbc4fccaf6de`  
		Last Modified: Mon, 16 Jun 2025 20:24:19 GMT  
		Size: 196.1 KB (196091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6c0ff01924041e8bb8ed8f6dcbe3ebc9409c41987b6128b80dc50522bc59aad`  
		Last Modified: Mon, 16 Jun 2025 20:24:20 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250613-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5c221bd6e24aa9badb2abf7576b9f7c9cdbf8a472c0fc0a8aa507036da3074db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83605863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9b67f341e9deea82518927edbdda30503e4acdac9e1786ccce4cf374478392`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dd3ea6e04c1423d6090963e2686477f06c34a0dfdfd784acc48ae829d42ba6`  
		Last Modified: Fri, 13 Jun 2025 00:40:51 GMT  
		Size: 297.9 KB (297894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474322652bdf8738a818f3dc1b43a8c6cbcdf6326e806a2a5c83973b4d105379`  
		Last Modified: Mon, 16 Jun 2025 20:49:17 GMT  
		Size: 79.2 MB (79171869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d9311707add41b70049ba4a52c343678ac5140e5e7d78d5a64440a8b6ed77e`  
		Last Modified: Mon, 16 Jun 2025 18:08:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8432ae205c7957465f0e682a89b096f490bf6419074656972899819a5d8a1707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 KB (221423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93bdd1f0e338e6d62fde2897e14becb4e7baecd584ed169abe3585fdb238f1fb`

```dockerfile
```

-	Layers:
	-	`sha256:d40d5d04b977f5da15752520a4497711f04e8957ea27a424c6627e62bc6d7ce4`  
		Last Modified: Mon, 16 Jun 2025 20:24:23 GMT  
		Size: 196.1 KB (196125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2132af84fc5675b4b516dccbe8e947f62d8f26effd305283e6e36f570e3cc45`  
		Last Modified: Mon, 16 Jun 2025 20:24:24 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250613-alpine` - linux; 386

```console
$ docker pull golang@sha256:4d12a4bfac0e23577b97dc304ee64a345fa5af0a6dbd564bf815251fffe0d506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85837954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d55034a619cd4cc17d44360769a9295ccc265154df0ac64fd90f20b5de93be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399cdbbca51e9d3a6f07c4b077f7ccbd0489cf2ba1965b3b44f9860189fbcc75`  
		Last Modified: Mon, 16 Jun 2025 17:55:11 GMT  
		Size: 295.6 KB (295613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e76dfda8e65144da912c18e6b785a2d25e1b2cffef4d19df66cebc068e773e6`  
		Last Modified: Mon, 16 Jun 2025 17:55:19 GMT  
		Size: 81.9 MB (81926154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad3f94a5d9a0e87fc135383c2c98f5dcff3ce79ab36641d1e818c8ee6dfc468`  
		Last Modified: Mon, 16 Jun 2025 17:55:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ed70a629d1929dbcd965aab374b394e75baa842b81e66fa0350646b8083ecabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b0b75492bf7eddd76e154becc4e6fc7eea774a792ab590638ea2fa09f4ea3f`

```dockerfile
```

-	Layers:
	-	`sha256:0ff603c4a006fa3ee1f4683fa9974443dd2a48e490f06fd6f6a2a3a18168fccf`  
		Last Modified: Mon, 16 Jun 2025 20:24:28 GMT  
		Size: 196.0 KB (196030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02f454b0e398e2bfd2665b0c8f3940cd46e82269aaf28f975d1e8eed33ea9ec`  
		Last Modified: Mon, 16 Jun 2025 20:24:29 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250613-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:ee8d5197e789a0cf8f667043e8272afdae4e70d8a60acf50c1aec238252c8e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84492207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384e41eee0b75f37d7af49655a73a82f6429fa12afc3e5aaad4b4b71cb1c1791`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187c79905be9977c8b81d03082bbff0333d20fe9ac9a7740864c66f7e0e5c7a`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 298.3 KB (298320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad7c0e71626161bd82d741bbfbcc3bb6f7d776d61d81013c12c5f78c854c376`  
		Last Modified: Mon, 16 Jun 2025 17:54:42 GMT  
		Size: 80.5 MB (80463542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c672fc6d675751e965b039a438e8e71491fde5df8b643b4c8bac447f1372866b`  
		Last Modified: Mon, 16 Jun 2025 17:57:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:31734b66f5da1882240d8f2648c5ed25831ed50be57bb21350a522b08f700f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44ede937b6f75db61aee307b39771f0de77a7750c5702db8e38cbe73233744b`

```dockerfile
```

-	Layers:
	-	`sha256:0bcaea47a40626545800e0d65ff15d428cd943fcf02c9cb489cb14083bbf9d01`  
		Last Modified: Mon, 16 Jun 2025 20:24:32 GMT  
		Size: 194.2 KB (194166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff3e8b8a8cc00e92b56ebf9461c11a70e7110d1400c5587cd25ff90201fdc68`  
		Last Modified: Mon, 16 Jun 2025 20:24:33 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250613-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:b2f1d97435014038267ec01b3029c0efa6201b73c31971ca196b1e01ab70c59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84471420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e703fd517250753a513200eac9d076161bce22e6e48b4e8a09d675342f7bf416`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
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
	-	`sha256:f11e6f198f2e22d74a216fc8dda40894832303989a270a6a2a28b62c9c2d8223`  
		Last Modified: Mon, 16 Jun 2025 18:27:37 GMT  
		Size: 80.7 MB (80662061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6175372e0f2b04a6fa12fb6a453d7583861febfb882585583842d0a18ef546`  
		Last Modified: Mon, 16 Jun 2025 18:27:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1486e10dac09d29b5c02406d31091c302f4b307c66fce9c3073ae29646959373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4f0108ebfd41c36c4324566fbb604a6ff7faa5b73012db47c893e4921c0f94`

```dockerfile
```

-	Layers:
	-	`sha256:a72e4a035d4995f68a5d58534cc70cefc0b7ba30661362aa24adc900bacd3963`  
		Last Modified: Mon, 16 Jun 2025 20:24:37 GMT  
		Size: 194.2 KB (194162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f1803a79866bef0141d87c20e2a7a34e9bf9638e37ba7dee6bd6d0a4da65d7`  
		Last Modified: Mon, 16 Jun 2025 20:24:38 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250613-alpine` - linux; s390x

```console
$ docker pull golang@sha256:804266209da353b259d20aa4f165260beb5232e32bb3f3790241b98909254516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85649618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69462ae4ada6d0ada1708ba9f59bf0e471051eafa36655832a9aed27b1cf3cec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 16 Jun 2025 05:23:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Jun 2025 05:23:25 GMT
ENV GOPATH=/go
# Mon, 16 Jun 2025 05:23:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Jun 2025 05:23:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Jun 2025 05:23:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02725f6addf0718099c43b5965203aa513fc71aa710978afc18cf384dfb4798`  
		Last Modified: Tue, 03 Jun 2025 13:31:49 GMT  
		Size: 296.2 KB (296215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaececbf60f8977aeecc80652f00dbd122956c4ff0ff7fc6dcfdd1756401a5d`  
		Last Modified: Mon, 16 Jun 2025 17:54:19 GMT  
		Size: 81.7 MB (81705716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12572d811925b73c7c7c4cf2649d897eb20cbc0e3158a8788d6103072da4afa`  
		Last Modified: Mon, 16 Jun 2025 17:56:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250613-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:868ac45cb282498899defc60a57a36d1b50c1d8acf855259718536ccedf4a279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 KB (219256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44a485301fc9ea7f5ff2a2309fff0bdfb9be910e4455d30bab8058e68696da6`

```dockerfile
```

-	Layers:
	-	`sha256:f9d4e73cebb2d3ef85620abed371311bfb692a26f3e2e139c9f39b3e6ccf5ceb`  
		Last Modified: Mon, 16 Jun 2025 20:24:41 GMT  
		Size: 194.1 KB (194118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd95311a04dc50f4ffcb8446ac3d5ddcdd726558cd275d63600cd0d211ca8e9d`  
		Last Modified: Mon, 16 Jun 2025 20:24:42 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
