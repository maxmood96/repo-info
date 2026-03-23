## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:e458f280a1c51889220936f5a673be92547a1a360c90262f2b045a7f89641ef6
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

### `golang:tip-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:9bbce516aba7686adc6aac0adbb57f12b557e77db611b0a39f5dac9ae8c0218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98084952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405a1ee28c181fb62ba5757c94135e3164c4c9a6aa48b235712f395b85db71a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:14:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:15:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:15:56 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:15:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:15:56 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:15:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:15:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea34634650847bad95f51be45f482366277d11b81e55465c321969ef0d324204`  
		Last Modified: Mon, 23 Mar 2026 18:16:13 GMT  
		Size: 296.1 KB (296093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14da6971e9abc1b6c7a1372792a609e9cf545f9f36ce489f1bdacf534e2c8abe`  
		Last Modified: Mon, 23 Mar 2026 18:10:59 GMT  
		Size: 93.9 MB (93926880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe09be4d642fc88a7e2d8bdb2b4493110727594997ee51eef4687bbd902b864`  
		Last Modified: Mon, 23 Mar 2026 18:16:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:a6ccbd04f00b1b28bf737160f3605975dadd985e3bbc11d634deb1f767af0964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 KB (220698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1d7b2dcf6b81fd8096a034fba0c3e8b76ebcc0a191d35af7205be8691119bf`

```dockerfile
```

-	Layers:
	-	`sha256:84f934e0182513f2efa640bc32cb44ec6510a6368211225249f4c85d5e543188`  
		Last Modified: Mon, 23 Mar 2026 18:16:13 GMT  
		Size: 195.6 KB (195603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cffde023852bf91ba1d6be167f4896dcdf987c29a1eeb5847cb581ed40ffc63`  
		Last Modified: Mon, 23 Mar 2026 18:16:13 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:9e8b8361c67f2665302ed43ce6aa87186bc03f64c687a64fc541f8e53595eef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94190021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15eee29905e3fa2a41e597d0273c5bdee128c29123195cfd92e810c8b9332cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:07:01 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:09:46 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:09:46 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:09:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:09:46 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:09:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:09:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b7c034b87405a6375211d41cb307703f468d1a7614fbc44f947e99b1c458f`  
		Last Modified: Mon, 23 Mar 2026 18:10:01 GMT  
		Size: 297.3 KB (297257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7dd031b7d46ac68f8093f5d3ca1cfde9444287482bdf5554db65238123ea`  
		Last Modified: Mon, 23 Mar 2026 18:10:04 GMT  
		Size: 90.3 MB (90322785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2fdbece42402cc5e3ce6d49a3c24526416d53e872977d260b8f5b728232762`  
		Last Modified: Mon, 23 Mar 2026 18:10:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:b62dca4d3fde2f625577f73e7e905c2390a3e8a9828f17b7ca61747561cad952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dbc3e5b9a46abafaa88fb46aafb81699200b70ccff83f8bb97a4a31c819028`

```dockerfile
```

-	Layers:
	-	`sha256:bdb35a84b259fd5f76948946e2ae638bb0aba3d3420b6d18f4a0431a4078f797`  
		Last Modified: Mon, 23 Mar 2026 18:10:01 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:ded01ddf793c4d25d36757558127ceef4bfc2d348759038804af17293c3b44aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93620947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269211f8ca72da9138f9fb007d404345c031aeceac399f0163f29b91ed113f14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:12:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:09:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:09:40 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:09:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:09:40 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:15:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:15:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69532c426d6a34033884bf4394eccb6b96c17724ec73106f85c53a1ef08b3b9`  
		Last Modified: Mon, 23 Mar 2026 18:15:19 GMT  
		Size: 296.2 KB (296201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3fe8212a49eb41f6a4366c38fc20cb7c161e830a9074b4c7ea09f324d1f7e0`  
		Last Modified: Mon, 23 Mar 2026 18:09:57 GMT  
		Size: 90.0 MB (90042864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de669476065d0ce3f460f94ee4be3f0b4d7157fb446835b69c2aa7855acdb178`  
		Last Modified: Mon, 23 Mar 2026 18:15:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:8f0135bdc2e532b5ae3bd59ba29a5c9f0b20c542d97cabaf8faf0e96853ad7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6e7df44ce4397dc3922f5e4b3a104bd72b4a16ec0c6a2e79613a2068172821`

```dockerfile
```

-	Layers:
	-	`sha256:a0bb2a71532b3b8f8990fe1518b306ecc9db14ac57cb6fa00672ad5aa5cc1505`  
		Last Modified: Mon, 23 Mar 2026 18:15:19 GMT  
		Size: 195.0 KB (194973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e5355527fc0926774d8d5ef16f8c3faf8fa9823f92dd38f3357e933243f4e9`  
		Last Modified: Mon, 23 Mar 2026 18:15:19 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2ee47a083dc2a32d78d2208fd3629b80029cf99ed6a54dab51368caf53c00d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93528991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c1ca4bbc2bfbefa8a13cef91acc0dfc09c46ab61216278a025a795e4cb6811`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:13:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:15:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:15:26 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:15:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:15:26 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:15:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:15:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d59f09325eef11ca8cbe07595dafc1d1d2f5fe92de3752a70fd651980fbc9`  
		Last Modified: Mon, 23 Mar 2026 18:15:44 GMT  
		Size: 298.8 KB (298844 bytes)  
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

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:050244bb5b49ec1823c7493213ce3f12618832228cd34431bfab615313c8b019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.3 KB (220264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6317cfb39167576cd044699c3591c8afaeb00513661f8589c3bc5c2583d099b`

```dockerfile
```

-	Layers:
	-	`sha256:3727b9973ea9e978173fef679caa4081e49bfb4fb3acd51a290db120078cb21d`  
		Last Modified: Mon, 23 Mar 2026 18:15:44 GMT  
		Size: 195.0 KB (195009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f357fbaa47c7a0fede267d9bd6f096b402f2d2e0e4691b935748fdf482361c89`  
		Last Modified: Mon, 23 Mar 2026 18:15:44 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:ec81d8c73758fe797383163ad8577ee2aa0aa52c0bfe79969d73d95231903099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95716446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffb94933d045e8c97b49cedbf9455489eb37fd8c7209f5f733b3d3f41cf203d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:11:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:13:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:13:24 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:13:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:13:24 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:13:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:13:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43585c980ac5439608d0e1c7b29c964f4b153c88ae3f3648f000b7906fc7043a`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 296.7 KB (296673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52264f7e91fc0f0620e6fa158257cdbe7e1dfe1394592c1026625d9442a0cf94`  
		Last Modified: Mon, 23 Mar 2026 18:11:19 GMT  
		Size: 91.7 MB (91732617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a173a96f0e9aa246ef1951644ebb3e440516875fa8bc69a670af7b30926fb26`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:387b56a39567205396b02309a813b4a4202581ff449f42f1a9d396f1f4392021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977265d6a008332c60d22cd5bbfdedd1d8fd9b8202ef459d00882ac32c3042e5`

```dockerfile
```

-	Layers:
	-	`sha256:f49a0bb89101eff479025c9ad03a10f1c5a14af04eeb58f15dac60ad4b763ae6`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 195.6 KB (195562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b43e45914fdf9d2915bb4385b5f3ff07215bbe6b2773aad066cc5d516e86f84`  
		Last Modified: Mon, 23 Mar 2026 18:13:41 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:8e93e34a4810b24b51b56bbeec131f5cddf2523623442d3e26f4c25f0b6aa481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94854396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0175be658db1e865a810c0131c040b191d58d91fe39232b25d3f467479e0100e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
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
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44ae5f08a3b31854f65b8b732d22555b5d281a52e17ea708b110e141f25610b`  
		Last Modified: Mon, 23 Mar 2026 18:39:37 GMT  
		Size: 299.3 KB (299255 bytes)  
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

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:2f684917f9f77c01f4ceba8534cdbbeaa57dc9f35926589903a07f66664b7260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af26dacbf16dcd553f52d81963d6081d284c16fb3b63a3f7c93e7795f464c97`

```dockerfile
```

-	Layers:
	-	`sha256:8694b49fa1679978cc640e43d505ff69c82b452baeaa7bb5145c3d263a22b998`  
		Last Modified: Mon, 23 Mar 2026 18:39:37 GMT  
		Size: 195.0 KB (195002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee63530d3961bf0c0d8bdb996668a9d8dd990050776fd8eb80827b7709282d0`  
		Last Modified: Mon, 23 Mar 2026 18:39:37 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:71625a2ff62463d75e6f7d4b89cecbdc9dc7c003f1b8413b792b867b57e43b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94786123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de74bfae71aa5c71ad89d72fc017c2f433bf71258c9f5224bf2a4d196ffa4685`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 16 Mar 2026 18:41:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 16 Mar 2026 18:41:25 GMT
ENV GOPATH=/go
# Mon, 16 Mar 2026 18:41:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 18:41:25 GMT
COPY /target/ / # buildkit
# Mon, 16 Mar 2026 19:26:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 16 Mar 2026 19:26:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2540b408e98980f08989b2a443ee35cdf7da6f3b7310d46cd1e63b1f1b775094`  
		Last Modified: Mon, 16 Mar 2026 18:48:21 GMT  
		Size: 90.9 MB (90904175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db5032ade1fe129b6714d217bd3b7a823d8e26052379c448b411ed97e90875`  
		Last Modified: Mon, 16 Mar 2026 19:28:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:b7cd539814a47517dc10d4c5e3095f08069a40624d05aad2d9064cab1cc2242a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 KB (220151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c534329e1670b95a946cbbbb6e80ca3b855e56433b0ad2d96d6209a345e33f1`

```dockerfile
```

-	Layers:
	-	`sha256:b2084ff6927c9b5e412a0a6cfcda14945649af5276ce63cd7059d243a5efbf95`  
		Last Modified: Mon, 16 Mar 2026 19:28:03 GMT  
		Size: 195.0 KB (194998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62c04d8fa0d7b06aad37b76ed4501f11db57b203dd01d4829c11b2bcf907bf1`  
		Last Modified: Mon, 16 Mar 2026 19:28:03 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:e8645bda6ee673c9ac0548c2a675e08294ba2c3d8de789cb6c724c67e9a4bdc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97141793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f077758bc70c01c70481ae82c19a3cb5c5864cd8eccf4432efdb92993264cdaa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2026 18:10:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 23 Mar 2026 18:10:43 GMT
ENV GOTOOLCHAIN=local
# Mon, 23 Mar 2026 18:10:43 GMT
ENV GOPATH=/go
# Mon, 23 Mar 2026 18:10:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2026 18:10:43 GMT
COPY /target/ / # buildkit
# Mon, 23 Mar 2026 18:10:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 23 Mar 2026 18:10:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11279f22cd782ded769b57fbba7b08a2080e81c5861c4c9728308b5c5509ee3`  
		Last Modified: Mon, 23 Mar 2026 18:11:10 GMT  
		Size: 297.2 KB (297187 bytes)  
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

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:386b1cc4c4d3d9b3e18657b76f8c9338d36ba073347de9750fd8da3366d5871f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b71e32282fb993a71dd325062b571f6c11a8eda1da7a2e8af648828a74be31`

```dockerfile
```

-	Layers:
	-	`sha256:9d46c8b9e8a4c5bf57d8162c360a4735b72dbc0c6635f12e471c9c730e61365a`  
		Last Modified: Mon, 23 Mar 2026 18:11:10 GMT  
		Size: 195.0 KB (194952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cd3a7a1e1ed7f3c6b88acc68d7b07503709fb2348e889f6e46efba9876c389`  
		Last Modified: Mon, 23 Mar 2026 18:11:10 GMT  
		Size: 24.9 KB (24922 bytes)  
		MIME: application/vnd.in-toto+json
