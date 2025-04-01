## `golang:1-alpine3.20`

```console
$ docker pull golang@sha256:00f149d5963f415a8a91943531b9092fde06b596b276281039604292d8b2b9c8
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

### `golang:1-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:a9c3b8a7fd754608532aa1c092d03589ae6fcfd3263b2f54060cd54fb05ceb91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82863661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee28666b3f8e38a105268ccc609be21dee5bccf42be3a6ca97dafe2c9a262df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c434a1494886b51a86fb89393427a473ebfb4e65fa4b7afa9cb568bb09ebd2ad`  
		Last Modified: Tue, 01 Apr 2025 17:07:25 GMT  
		Size: 294.4 KB (294390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d296901bdc593d88a0813bb00eef0974b68222cba6add046b831c086a1c68c`  
		Last Modified: Tue, 01 Apr 2025 17:07:26 GMT  
		Size: 78.9 MB (78942217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c25a1dd5f892c11822e5c622be7cbfccdedfc2321058c168b822686cad3924f`  
		Last Modified: Tue, 01 Apr 2025 17:07:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:12f4654bd1dbc422531f229fd2eba11b9001bdbf31befebedcea48c8ce0b253a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 KB (229381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2659211baa6e97e17708a5653ae47c662a16159ffe6d91fea57af352fa72808`

```dockerfile
```

-	Layers:
	-	`sha256:3f9e281b7ab8003623e53541102e9e41fc134ee89c9b4b372c0a782756af5bfd`  
		Last Modified: Tue, 01 Apr 2025 17:07:25 GMT  
		Size: 204.5 KB (204531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca594a5638e95b18a0848d5afa3a89783b007ded69d4420d8115b48bbe0c77da`  
		Last Modified: Tue, 01 Apr 2025 17:07:25 GMT  
		Size: 24.9 KB (24850 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:f63b77647a1c246b0b2ce50cabf82627bae10d457cccea10a4f31cc412df123e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80769318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0deec5a3f1d97cadc309360fb41233faccfc573e96ffaf3cb7273d42a54ce4ec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Fri, 14 Feb 2025 22:17:11 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f7a72b848df6c57152561340e794d310a35691d8f3a552ab9db9fd598f168e`  
		Last Modified: Tue, 01 Apr 2025 17:07:08 GMT  
		Size: 77.1 MB (77100796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b73f4aa8ed24e3804229a7553d1ee88b81cf98c6489992e5151647f4ba17779`  
		Last Modified: Tue, 01 Apr 2025 17:07:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:bf54ea594605b3f19a4421deebbc18c4f7c820aef93d0daffb7cdb61ec27ebd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0302fc9ae4c2e2c82bedc76cf0105a7bd452910e169cec1109dd5b1879eb397`

```dockerfile
```

-	Layers:
	-	`sha256:95f966a636fee8067de62157a14beeb544baac7e474eb02253d07ce63eb6daac`  
		Last Modified: Tue, 01 Apr 2025 17:07:34 GMT  
		Size: 24.7 KB (24737 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:c0814ba277aa92d20ccd10897b070a959c698c23e53c351cb2b26e4a3c794620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80492092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56dee342957e7018e574364a7529ef0a0ab3752f849114db42878921a58fca0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Fri, 14 Feb 2025 22:11:53 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9003e8a4d55742a1a2128c3dabddda68ec2c585f52d2aac5eaee8bd68089640`  
		Last Modified: Tue, 01 Apr 2025 17:07:37 GMT  
		Size: 77.1 MB (77101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716e55d60065fb35d21631771362cad72f183fa415fe2312eceb3682e5216f55`  
		Last Modified: Tue, 01 Apr 2025 17:09:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:24959f1d44fc7896e1b093ae2b4a678fcd284701dfb1736d49545e28eb3bbdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 KB (229483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ceaa160dbfb11ac4fd9d87109270bcf1a5f000d49f36493d9d597bfff21895`

```dockerfile
```

-	Layers:
	-	`sha256:028b44d32f8405f40bb0f05be3edd9570cae6f57fd30d5eff0aa47b537e9958f`  
		Last Modified: Tue, 01 Apr 2025 17:09:37 GMT  
		Size: 204.5 KB (204531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e3b5f23d18f9a1a125314d38f74209bcf15ad5d1cf2f302c27dc2648c380a4`  
		Last Modified: Tue, 01 Apr 2025 17:09:37 GMT  
		Size: 25.0 KB (24952 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:09cc09e52f35e351229195355936fc29e4e392f2ad919b3d5ecfa397a6d23b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79588994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f60e9341d9b3a469f139ea1dfb9ae608fdf70164490f9df9276619d5ce7f20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634366ca850b96a5c7a0780daec3499faf6933b86acc8a8e99b70a5264f8f00e`  
		Last Modified: Mon, 24 Mar 2025 21:31:30 GMT  
		Size: 297.5 KB (297463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a002eda2038f0953467f843586445333b2af3e827e57b15849040931f2903fb4`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 75.2 MB (75200208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ef72f6ae48708a78bc4b5782fce30905ff906bad1d8bcc1e805686be69f155`  
		Last Modified: Tue, 01 Apr 2025 17:09:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ed532e30823e62dd4d55efc7dc96aa15175abf1a4ed7db740768c8ae35ddb71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 KB (229571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aaa418056ee9eb6c55f44b0927242153e3800f6914a01277d25b514e5ee4359`

```dockerfile
```

-	Layers:
	-	`sha256:92a0649b5da6b7c416254039af101f99e19e13afba9c0ff08c85169f756fbeef`  
		Last Modified: Tue, 01 Apr 2025 17:09:05 GMT  
		Size: 204.6 KB (204587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbfffb3919acd6940f050492c3d1939321eaf423219c252c10a5f0797fa96cd3`  
		Last Modified: Tue, 01 Apr 2025 17:09:05 GMT  
		Size: 25.0 KB (24984 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:5983bc7b4c0239974244960096e73a63b759d60ccac2acba0a6deae1a22fe7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80640369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca519790aaf70ccba873a3d82a222775a46588c7378917ecfadf039f8b103f84`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed57473942fbb31f3c6f3ae49630c975ec53d72c82f15509c79dc03727c7f490`  
		Last Modified: Tue, 01 Apr 2025 17:07:29 GMT  
		Size: 295.1 KB (295129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb556227a38cd463b29410ff393a23b771d304e2f2f265b6c233fe487c9ca9ff`  
		Last Modified: Tue, 01 Apr 2025 17:07:28 GMT  
		Size: 76.9 MB (76873414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efda6a9ec0ed27775d0887572a23317fed2c90e7dc2dbe7ce0dfebddc8ae41f6`  
		Last Modified: Tue, 01 Apr 2025 17:07:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:cf8785cc3468bc97c0b7ee37956691583d5e019f8cfc1f924230d8b335175774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 KB (229284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe8e378bbab789fc4e02d54e77d9684052bbe6a6c7a1928213d904007e3c9d6`

```dockerfile
```

-	Layers:
	-	`sha256:c36f9008e745f4cb920a6a9a2cb7f9795cb2291f3fee076d874d21beb01affce`  
		Last Modified: Tue, 01 Apr 2025 17:07:29 GMT  
		Size: 204.5 KB (204470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6d29c253bc089d67cac515477aebae3404b6d85b69c3a625057f7b599fe65cb`  
		Last Modified: Tue, 01 Apr 2025 17:07:29 GMT  
		Size: 24.8 KB (24814 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:ff1463c782c63f03b5ec881fb547fc053a98624ced0946911aba98c24d3b9e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79375022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419109ce574c59cc923c0cb3a606de4b4b1813e0d9825852d704a9db1253c4f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15784993a892df626148136e939e65b594ed2f1456345704a3272ec8fd984c53`  
		Last Modified: Mon, 24 Mar 2025 21:51:53 GMT  
		Size: 297.9 KB (297899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee95abad5ecea3c593f42714d65b6f62167cc9a1a7a50eaad85a7db940a3e7f3`  
		Last Modified: Tue, 01 Apr 2025 17:08:51 GMT  
		Size: 75.5 MB (75501286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04223afbbdf8173f170b7f4964d3a5402fa30ce72585de4e310afb2a606cef8`  
		Last Modified: Tue, 01 Apr 2025 17:10:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e643a7046643edeeefa1fabbf5e8a4b47a7803c15e5590d898ab2618de651d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 KB (227548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5312b1828b759b2b1d02bdc5f95bd52dda5486e62924951b7eeeec1479fc44`

```dockerfile
```

-	Layers:
	-	`sha256:dea0a68c4e9edf37062645e2132676ccf6f8e35e9c4beb14e3d5e262dbfa7f07`  
		Last Modified: Tue, 01 Apr 2025 17:10:43 GMT  
		Size: 202.7 KB (202650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8d682e9dc619a8437a1b26379c8fb53c9c336c155be584e59bb3758dadf479`  
		Last Modified: Tue, 01 Apr 2025 17:10:43 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:c2a0a744790cfaac2c55c4555062ea3f12c0b39a85ea9e5c995e181a8ce17cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79937779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3febd15ac61a20e0e492b92993e7270b873ebe0d5e3b8e729a385876fdbe18b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 06:13:57 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5ce2f0c01e27eae69810e26e082b26502c0109e9fbee7d299ecb1273395b27`  
		Last Modified: Tue, 01 Apr 2025 17:12:00 GMT  
		Size: 76.3 MB (76268943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415c08e1ae9e98a79ae89ce86342a1b493e514e0fad0d9e5f2fccc4eec0f2424`  
		Last Modified: Tue, 01 Apr 2025 17:15:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:c8c1949e6ac1a19a0382ada14b5eda12a25d9329c8fcf640ad0407fa12f6b9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 KB (227544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e509c8e9771de284f0c0033f928c93b1380df9344fdf68b4cf3408b2b3c1165`

```dockerfile
```

-	Layers:
	-	`sha256:35d5159d137c372530721b481db87e727d9695e86e15511bab7df10bd12be7b3`  
		Last Modified: Tue, 01 Apr 2025 17:15:34 GMT  
		Size: 202.6 KB (202646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb3929c5d9d316449c2ee6f61232135bb319732516d521f49832d98dcb56ba8`  
		Last Modified: Tue, 01 Apr 2025 17:15:33 GMT  
		Size: 24.9 KB (24898 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:6fd147aadd8ac7ec4b0567f41eecbc90030316ce1cc157fb9df2efa4bef7ff16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81504413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792cc579bd8b5567de19b1ded1496e17f5c7f15be7ed8af74c8797e02561d144`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 01 Apr 2025 16:30:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f378f0ab9f92249cab05739adecf3318eef414f2bb034b8f1580eac04a7de99`  
		Last Modified: Mon, 24 Mar 2025 21:30:12 GMT  
		Size: 295.7 KB (295703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64586fca58b7ef9b98d81252f6468cd1afe274720313716be72d0e12ecde9791`  
		Last Modified: Tue, 01 Apr 2025 17:08:27 GMT  
		Size: 77.7 MB (77744430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44d0bb66c03f5b751181bfb6efaefbad56e98e3067f489b578fb12000a0cd0`  
		Last Modified: Tue, 01 Apr 2025 17:10:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:00fe15635e67473f38ba9ad0cb1794dffd2171c9d65519e84372bdf6dc30032b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 KB (227429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebc7e851307d2ff22a90cad6e7da7e1da3caf75825ed852d6c9af8d77c03e12`

```dockerfile
```

-	Layers:
	-	`sha256:304fd46d1ef73d5faa162b0dd8ce141ebc1e018b1ede145decd2d7652b8bad7f`  
		Last Modified: Tue, 01 Apr 2025 17:10:08 GMT  
		Size: 202.6 KB (202580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3eae3b62a9e71830fdf488a0a09c8bcdcc06ee6b33be0ed1957d1bd287e4823`  
		Last Modified: Tue, 01 Apr 2025 17:10:08 GMT  
		Size: 24.8 KB (24849 bytes)  
		MIME: application/vnd.in-toto+json
