## `golang:tip-alpine`

```console
$ docker pull golang@sha256:b550bd32096c122b642c6f5534bc9c3b70be797f8d9ac981f92d321a31a7efa9
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
$ docker pull golang@sha256:066b19290551c05750ab78f5240030549ab0955f57f0403f7bc8c6085296b970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.5 MB (101487019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:113760a5f3152dba873e1efa74950a1c15a2d41d76b69ea0726995dd4ec5c646`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:17:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:19:27 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:27 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:27 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad846d1ace415fefc7e89a9deca4ae3759534b15dc56ad5e58cb86dff9a6b34f`  
		Last Modified: Tue, 28 Apr 2026 00:19:44 GMT  
		Size: 290.2 KB (290233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779709856b286b334888c2db50fa75d06845c18a6db8049d9f565750e3ae705d`  
		Last Modified: Tue, 28 Apr 2026 00:19:47 GMT  
		Size: 97.3 MB (97332439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1689446014cb6d600288a132aabcc980c3e7dd8025326b5e9925d386d95adc2a`  
		Last Modified: Tue, 28 Apr 2026 00:19:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:1893da790268046a64d07abc4c4bddb4b312938eb125c00cb321b67dfff4cc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee45ef1f2d4579d79789ace6b46a7198cdb08752697ec18850cd6a17e60afe71`

```dockerfile
```

-	Layers:
	-	`sha256:bf51e4d4f342293ee743f613ec44e54118c2a15e39fc212f8ccc7bc6de13f559`  
		Last Modified: Tue, 28 Apr 2026 00:19:45 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b1628d3ffd7223c0531b79aed343851cd4be40e6e907417e41523cbc1e6fa4`  
		Last Modified: Tue, 28 Apr 2026 00:19:44 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:d92d34bff6c9d5dd02a7ad2dc8363bf0ee97a24fdbca6aa9b383fc3bc04b46d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97325936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf46822de483f2b209603b26430ce231c6dfdcb6da1615139d67889439f2920`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:23:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:26:28 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:26:28 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:26:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:26:28 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:26:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:26:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf270714bd41affccea1251ba1a418fb673537638eb87bf23c35b79364e2512`  
		Last Modified: Tue, 28 Apr 2026 00:26:43 GMT  
		Size: 291.0 KB (291021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a940d4d379576eb230d86cbe12edf83436fcddaa9c7f262eb578020d7d278`  
		Last Modified: Tue, 28 Apr 2026 00:26:46 GMT  
		Size: 93.5 MB (93462894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f4a5b0f179bc654e02864228559ad16f2d21e13904ea1a5b0151cc7a507e8`  
		Last Modified: Tue, 28 Apr 2026 00:26:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:460640e7d122d64250547949e2369b435bae5eda0cdfe2b7d483639956d370f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7e8c1a628565e3272b4985845349c279788385b21aabdc8c77209e28280b3b`

```dockerfile
```

-	Layers:
	-	`sha256:120a759a4b9f4a6d201ef27a430416ad163302d7befaf408a501778e4e437a4f`  
		Last Modified: Tue, 28 Apr 2026 00:26:43 GMT  
		Size: 25.0 KB (25008 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:93c1fc3817d2038aec3f3645e6b70e1c6e7f831f5274c842514e471bd16e5e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96745908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c19d90b74ef4d07f81253ed789b17bab1c147c74ea98f37b8ea67f068a1b62`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:21:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:20:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:20:32 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:20:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:20:32 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:23:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:23:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6bd175988f2490bc2f6ec3102cec5adf093727c21c4f1b036baba19a726ce7`  
		Last Modified: Tue, 28 Apr 2026 00:24:04 GMT  
		Size: 290.2 KB (290164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d73ddf188a2e2e6775fd1105089506e6b38ccd4ec9defa63926d5363c7b9227`  
		Last Modified: Tue, 28 Apr 2026 00:21:01 GMT  
		Size: 93.2 MB (93172464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f83e9340ca9ab9c5695c3a3b462e3ae39102331a7c25856d8fca98120fd96dd`  
		Last Modified: Tue, 28 Apr 2026 00:24:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:457d187d6a7d9d09f6863191dd0633e902b69a2c0dd333283c57c3d059f80ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56532a8ab48c1e5e74f9c3af760e4bfe1bb06fbc422dd5ed4a57a525ae31c5d`

```dockerfile
```

-	Layers:
	-	`sha256:ad1805e8c88bc64781a0f2531cc3e83880f6d377601a2e0e7f6530e638151559`  
		Last Modified: Tue, 28 Apr 2026 00:24:04 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d9bfdca50e48a90208d879381dbae55a7808a88f5b3ce5423ca036c302f849`  
		Last Modified: Tue, 28 Apr 2026 00:24:04 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4325114b5c44da160d26b4757f4fcfe50544e25fe33178625a2fc837d672d56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96532568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722e571fe5e2bf2a4e28328629a3ea38b01e86106ff9751f72db0156414b1c1e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:17:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:19:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:24 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:24 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e5aa8647cbce7b8a962ef35302e3a17ca647e65c9d4a603b2ef4900db14c7d`  
		Last Modified: Tue, 28 Apr 2026 00:19:41 GMT  
		Size: 292.9 KB (292853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324bee5f74040b6510924c3347f3aeb86c3579f67dc47584d6081f70bceb6576`  
		Last Modified: Tue, 28 Apr 2026 00:19:44 GMT  
		Size: 92.0 MB (92039689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1064f9f5a91c9336242ea0cf009f2bc7facc34e3cca8cb3273d500858ee1d1b1`  
		Last Modified: Tue, 28 Apr 2026 00:19:41 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e6bce0b372d653e38da0ae60a38af5991ce6ca90a6cf625bf87db6b48ba73644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc7595dd79b4834ebfc288c9facd4e7b9f7080ffebe6c234c03e9b3bc155705`

```dockerfile
```

-	Layers:
	-	`sha256:ace73a53c4bf9f5f78adcb8b43977e0c3cf812f36bcf7ff3fdc7a756befe088c`  
		Last Modified: Tue, 28 Apr 2026 00:19:41 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6954af18302cbe1463ef89dcdacf30a82543174b859610579e4fb5a98d72ef0e`  
		Last Modified: Tue, 28 Apr 2026 00:19:41 GMT  
		Size: 25.3 KB (25255 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; 386

```console
$ docker pull golang@sha256:24eda8565c4c7c59098bf8a19559223a2228c6206cdbdaa7b630702f2c11c7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99069062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a66f91db5af3076408c7404bdecbe0a1e92e171bc354ee11235ff5f1c4adad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:20:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:22:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:22:32 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:22:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:22:32 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:22:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:22:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b056f7bffd5fefc78e2910661c1d930c1fa156547ddbe72b678dceed742b9fe`  
		Last Modified: Tue, 28 Apr 2026 00:22:48 GMT  
		Size: 290.6 KB (290635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d6a9c589b969b9eee8b2fb5a3d53dcb1feacb04a0d56a4902866f913a72511`  
		Last Modified: Tue, 28 Apr 2026 00:22:10 GMT  
		Size: 95.1 MB (95087823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe99a1bc9e1e2091b840fddfbd9e6f8cb622b0b27936745a481d843e231b210`  
		Last Modified: Tue, 28 Apr 2026 00:22:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:017d2df7c1903206df264a101c0a999bd6e64295a1557ed84ad9cec8b0623049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce9ce9da0a9bd23ae06c2325d4c88fea020fef8499010c22ce11d0534a4cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:69153cdb148dee14f75b9760278b1b6ee42e9afe6f0080e9bc6d9298dc72b66f`  
		Last Modified: Tue, 28 Apr 2026 00:22:48 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0b6baa233bd88a45f772c492464973ee48b7048b48b2a859a2b8c7f60f77f49`  
		Last Modified: Tue, 28 Apr 2026 00:22:48 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:265986eda53ff6c5fba43bc8bd9662214c917d913c0ee5e158e15f5c83665cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98021987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a8931a62b533256763798620c13d44b34a429e669f69cc567d1de46696dd63`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:21:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:21:51 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:26:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:26:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e34165e157d14e975c070ad73c3dbd1767de1fa84e282e6505d64626df00ff3`  
		Last Modified: Tue, 28 Apr 2026 00:23:11 GMT  
		Size: 93.9 MB (93897536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990870f21326610606b376c71a625d2e13a788d23aeb9eeaeb20874ea5a746e2`  
		Last Modified: Tue, 28 Apr 2026 00:27:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a6afdfbcf0368762bb9b0f3e4451a91f888d3b5b593bbeee790da532505de671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a126ff265a9fd9ac302d8384bd14af96c927c2449aea7f99b47ef41449f9ad8b`

```dockerfile
```

-	Layers:
	-	`sha256:914c399c00686a36b575df34efd28395f3f6a81bc9cd43adb997e4a6fcfcfb96`  
		Last Modified: Tue, 28 Apr 2026 00:27:08 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8b5de8f3a3d57fc33eeb6de11418acf6ebecc189e14e410d42ccb1f67d7f5b`  
		Last Modified: Tue, 28 Apr 2026 00:27:08 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:f98dafc7c32667cb0803b63add0f6c98f032ae6d392b4da97d955f2d0625352f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98302241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea05f5b961b22ae6d384782599420066499b03f80755ebd0cad4d9e71c2ce1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:56:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:56:48 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:56:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:56:48 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 01:43:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 01:43:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f21692e8d3232006360c86abeb47c76c05ae0fd9556f2ba4bef366f9fde74f`  
		Last Modified: Tue, 28 Apr 2026 01:03:40 GMT  
		Size: 94.4 MB (94423868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e260956f821eaaa3abc51dd17eeae05c3b2b6ca5127423f0c332a693de3def7`  
		Last Modified: Tue, 28 Apr 2026 01:44:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:8a47f79c51ab47af30456565036185243616840c4bab838fa46bb1d0d6528620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a0f0a2067ee7eb5618304b9dc4e42aea872b221014abcfe96eae5f5d6a10aa`

```dockerfile
```

-	Layers:
	-	`sha256:2c5187ce2297ec2a1873c8daddd695b68eedd428d79b01c317fbd25e9497305c`  
		Last Modified: Tue, 28 Apr 2026 01:44:58 GMT  
		Size: 193.0 KB (193043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7b742b533584f7b1aac3e01f7d0f4fddfda7b03b59ac6f73a03a6814cbc491b`  
		Last Modified: Tue, 28 Apr 2026 01:44:58 GMT  
		Size: 25.2 KB (25152 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine` - linux; s390x

```console
$ docker pull golang@sha256:bb8d7050030a6c50168814e797f3b3a93eff0e4a86149d8dccc0238a54b2477e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99899295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514a98792e82daac134bc9ab76e0b69fa7f08c3023fa026f20ee8b8f0a934767`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:35:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:35:54 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:35:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:35:54 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:36:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:36:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107efaa291b5f83372c13d97ab11aebdd260da2222cd795a4f56930ce905e525`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 291.1 KB (291147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c795090f7b3ba987c0e4ca6fd1eb3c889fe964ab0c0eb932bae581f24e4f796`  
		Last Modified: Tue, 28 Apr 2026 00:37:36 GMT  
		Size: 95.9 MB (95881458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0324bf7b6fb3d284c20dc1636b1d0e2422589ae3d27c696b23ee01a43b6a6823`  
		Last Modified: Tue, 28 Apr 2026 00:38:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0dfff3db7fe368fb8df23e1cc179c5d28474a3df3ef797bff88916ea5202ad3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a568681a81cb563e8f5dbab77b0effa09ed9ec626f3854e671d8585c3d3ebb4`

```dockerfile
```

-	Layers:
	-	`sha256:ba624452dcce90dc354ea068a0dfb6ad5d92c9e8af26c6948237442e7a085535`  
		Last Modified: Tue, 28 Apr 2026 00:38:09 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a87f55ba0f2cf2ba7aa15b97f58329c624931172657c2d1df7a6bd3be192ba66`  
		Last Modified: Tue, 28 Apr 2026 00:38:08 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
