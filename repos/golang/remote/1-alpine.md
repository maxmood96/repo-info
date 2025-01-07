## `golang:1-alpine`

```console
$ docker pull golang@sha256:6c5c9590f169f77c8046e45c611d3b28fe477789acd8d3762d23d4744de69812
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

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:052793ea3143a235a5b2d815ccead8910cfe547b36a1f4c8b070015b89da5eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77991250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6d980675843020a9b50696ec178531295719f6b771fc4d7ff3db87d97934d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3739efb98791f9f491c500f021f9ed89d20e62445523efb573896836303867d5`  
		Last Modified: Fri, 06 Dec 2024 22:28:37 GMT  
		Size: 299.2 KB (299200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d97d9959dd1b4bb05c88c529ce0bdcb89ea261e50c87f1ff20366fb0b9d4a6`  
		Last Modified: Fri, 06 Dec 2024 22:28:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6186188d58c2e5ae7ecceeeb12d6c275a6b864abbca34254f04ea0502caa2867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 KB (244416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e4fd70b1711ae2ffeb1e854adc3c75ade007e8b13340448f2b57fe6e92cb1c`

```dockerfile
```

-	Layers:
	-	`sha256:0f3298d0a3feb8da5042b45d9c3bae9c807bd4a237b368ac7955a4eea19fad0a`  
		Last Modified: Fri, 06 Dec 2024 22:28:37 GMT  
		Size: 218.3 KB (218347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69c249a7d053119a36514493c3ae45087f2bf09228290bce8ac4f219a906a301`  
		Size: 26.1 KB (26069 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:27138884925fc4fcc4b951adb43393cb25c0fde2ca06bb331ff3688b69f4b7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75866247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fb8c0792c778848972df572aee05e93fdc084056cd7c441a6a2c99e24e6465`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee1e955efadc353062808714cadbf3fbf443a9d39e47a0309d6f795eebdd2a9`  
		Last Modified: Fri, 06 Dec 2024 22:28:55 GMT  
		Size: 300.4 KB (300367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050f4d41a5916cb5bb0402144198a3db8be943fd5621e8c01e5ba2229f84fc1b`  
		Last Modified: Fri, 06 Dec 2024 22:28:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e5fbbf3d3f03f6d143d4be9d92cf97f87e38c2beaa14eb943701ec4810bead79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0e60d3312ceb3f4430194f40681f7d1178a406e72963404b1dca063ec68601`

```dockerfile
```

-	Layers:
	-	`sha256:26a694dc9329d7e34b845e7279f779e260b2547f3ec90c7de278cfe3b9a173d2`  
		Last Modified: Fri, 06 Dec 2024 22:28:54 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:87d30813f7c7f160e57769a031eac8411f94c1fc4a1faba746c3bb575d8f9c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75598021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea21f647e5442dae05ef0ccdbab7c438c8dd546bd3d910cf2836b26b2084825b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a49a2dc34dc55420bb1a7a53fe706b82cd56c9d5e3b8d9be9b00e726a3443a`  
		Last Modified: Fri, 06 Dec 2024 22:29:24 GMT  
		Size: 299.4 KB (299389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de929eedc35846234bad317684d0189d509dfc992991dd47e138d6aba1cd9c35`  
		Last Modified: Fri, 06 Dec 2024 22:29:24 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d52eecb48455437f5e61ff334a99901f469e7d914ada9b33e08444275e7ace71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 KB (244583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfcbdef020f2aa1c19f94a8d81dba83e34d6681f01e004731b2381a3e601fbe`

```dockerfile
```

-	Layers:
	-	`sha256:4a30b0550a61beb0b880f6730f0dc2feed0707289911c07fe0e6b82029ffb821`  
		Last Modified: Fri, 06 Dec 2024 22:29:24 GMT  
		Size: 218.4 KB (218379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cddd71246748557562b97fae7a8600599233afaa8029ef034ed9f083d489b6d4`  
		Last Modified: Fri, 06 Dec 2024 22:29:24 GMT  
		Size: 26.2 KB (26204 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:42bba3ac5ba2e9fb843c2ccde9fa0502409a76bdffa3945e730703dee67152f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74968556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466670fb570816d537cd1ffbd8a59b6632860be27c4cf6b3ddcd899f76f4bd6d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9615f269cd7b01531f49b529fa34e1410ceaad596584ad001171fb9c574319`  
		Last Modified: Fri, 06 Dec 2024 22:29:16 GMT  
		Size: 301.8 KB (301795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859344cb3f85f012bd48d437addf5714704a80f94bbc46d7026cce2eb6e286fe`  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:56bbdccf126c03aaf84094f9bd12c18568edafe4b13615e2502cad1c70344b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 KB (244702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28859419115d74c09dde73d618ef0430e9bb5d5564199ace2cb5338346127b66`

```dockerfile
```

-	Layers:
	-	`sha256:ed086f0abe0be2fceb71a3850e0ff75b659f6aadaaee0ee14aae0aa098ee8cc8`  
		Last Modified: Fri, 06 Dec 2024 22:29:16 GMT  
		Size: 218.5 KB (218451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f2858dfc638318f3994cf0f1e05bf50a8b5e8677a50775205ccb903947faa07`  
		Last Modified: Fri, 06 Dec 2024 22:29:16 GMT  
		Size: 26.3 KB (26251 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:5949eba7ed5bb0b3da95b97ec5b8800c1dc0ce4338302fef50d71cf3ded6456a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75679152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e62594d6af15701e0d7671297e0e5396bd4ee6eec0b8e172a1283f015fe6cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9729c7fdb1a301c8f7080b00adc5f081b1ec7c88d1eb0ee498a243011a8c92e`  
		Last Modified: Fri, 06 Dec 2024 22:28:39 GMT  
		Size: 299.8 KB (299792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ee978a239d9a54a2ed89c291f3c5c0ee5f67c1dc8c9ff24b239116398d826`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 71.9 MB (71913121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce4227888a34098cc660b2545bd71b85b0e96cbccf76e65ab084be2da5be04a`  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4b30f254e2497b95a56f36131bc1fef31084b5e3b38162b850f0956b4c1e69b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 KB (244279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604b9ea9970097e5738db1a38bf4c127e7d9265a828a83cd820d0db76bd5bb2c`

```dockerfile
```

-	Layers:
	-	`sha256:1e802a27ff4b716ac0c49d082a868f3747fe9e2cf9db7ad81a4a050c873894c2`  
		Last Modified: Fri, 06 Dec 2024 22:28:39 GMT  
		Size: 218.3 KB (218266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2bdc0aad66965d126bada7aff186407153155c19f2f8c06ce60cf42fc5c4ddc`  
		Last Modified: Fri, 06 Dec 2024 22:28:39 GMT  
		Size: 26.0 KB (26013 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:db12ce8aef85f336be800f9b27989539f80f8953cfbb195353fda06f005f7807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74718958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70d171b7a1183fe6fa1507c168ac288e72047841a01a61c6db59bcdb9d47670f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7138f21fcec456d1a09999d8b86ead997fa112463f052c4034e772e6520502f5`  
		Size: 302.1 KB (302147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b834890572191b3d66e6bd561aad556f3c52e760e67fe9e31f02ad3d5139f55e`  
		Last Modified: Tue, 03 Dec 2024 23:35:02 GMT  
		Size: 70.8 MB (70839544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8240d0c6777c77a1b54b386160eae5915a079f2160613d439ec928ba50f0efb3`  
		Last Modified: Fri, 06 Dec 2024 22:29:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ee6a41a267729688404ddda1aedbf45cf3aaa120639f709a4b4b187dedb9e7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 KB (242629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b3d27d0ba8e5e88a1142052653ec1942e05cb1a21d3c264481fbe8c95cb88`

```dockerfile
```

-	Layers:
	-	`sha256:ccf569bae6e4839e116381c38bf78b93a70dedd3d704b6621fec41134e2d1e9f`  
		Last Modified: Fri, 06 Dec 2024 22:29:10 GMT  
		Size: 216.5 KB (216487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3999f1a7edd1550261b2ca0267c699cb438fd9be4901b535688f5c0d2652d792`  
		Last Modified: Fri, 06 Dec 2024 22:29:10 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:d0c6727dbc30a2607ca6d2a2865f84540175514bcc1c67ca7b077d112d419588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74894739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3472ea1ace70f7c20da92ff09529851e73049bc71a9cab6489a49e6980dc73a5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352d2aed11821bec39048fd95800ed8324f4ffbc936cc77681114832e36fdb97`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 299.6 KB (299638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823549eb5d032cbe32b843ae14c0e8e8d506cd24122a9b9045affc7d74afd63c`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:ab8a215ebbe9109b3dd7ac2ba0f93446269f445eaddf6a1393941555246a8e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 KB (242625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb1b5d5e78dd696161d40f1ab9a887c0e424459247d04447ca732e3e2bf546a`

```dockerfile
```

-	Layers:
	-	`sha256:c259a8b951cab2cb0cbacf058261f8e90b6d97cef540e87ed0dd96b3e161e330`  
		Size: 216.5 KB (216483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e964aef05d43cc899631079a5cde222cdda9e9eee56df6e4f185e5c40f420be`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:a333c751d5a1f48cd9b10e6e56f0f4f642c47af94d313013b5d326f3596fb161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76739884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7c336231e06f25f31f5634959ebdcf344096e153869092b129e485159dcc76`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:15:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOLANG_VERSION=1.23.4
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Dec 2024 13:15:10 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2024 13:15:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:15:10 GMT
COPY /target/ / # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Dec 2024 13:15:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860c29245461f1f0f6f0374828569317291bf0da08619725e0467ac079826d5`  
		Last Modified: Fri, 06 Dec 2024 22:30:20 GMT  
		Size: 300.4 KB (300393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fab5e167d0540ec0635fa24bdbf45a8d0736fd35bf05fa6db7ac9b45f6461b7`  
		Last Modified: Fri, 06 Dec 2024 22:30:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6482457ab9e0f1f31cca102f6edf47006c48aff21c5ad0a3d5caf2d799608976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 KB (242463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c841ca55d059b8fcb8286d17ae96342850c3ae494032259edbb649ec6f1de5`

```dockerfile
```

-	Layers:
	-	`sha256:fa25d99c5a9a182f7c539e08b13037f7798f5cc26a39acfc97f37825efbe8fb1`  
		Size: 216.4 KB (216393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1951e3d99ce6da1621f74e8582f438bcd5cf5b8db9266244d4ff3a8b05fee9`  
		Last Modified: Fri, 06 Dec 2024 22:30:20 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
