## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:c9c3ec26251dceffba714a4c4a26c63bd016973bfa26d94da70b6e6a65babac3
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
$ docker pull golang@sha256:79de4bfa87b76fe2419d9a38eaa35d8191deb447d1dac84c0abb340477cf8c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101430239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7693bf0702da4ec95169b59d7899c6cc4562934eaedb74b30dacbb0c340edddc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:17:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:19:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:31 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:31 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9df0c59cdb4842a258425fe7c0621d53f1616556797f7e6310dfd236cb6152`  
		Last Modified: Tue, 28 Apr 2026 00:19:49 GMT  
		Size: 289.5 KB (289453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779709856b286b334888c2db50fa75d06845c18a6db8049d9f565750e3ae705d`  
		Last Modified: Tue, 28 Apr 2026 00:19:47 GMT  
		Size: 97.3 MB (97332439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e2557eed95dd5a6b218ac2e62f7605b2464274a40085c010cff7a8093df58a`  
		Last Modified: Tue, 28 Apr 2026 00:19:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ce61083c5cc1e527aa95d7257a9b8bc51ec42dd4d07dd1587d7c5b049ae9dd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9739eed1736eb336e30cb5cdcfe3b7b00da83440357510b57c39f2ccb9e240e6`

```dockerfile
```

-	Layers:
	-	`sha256:a91643955734099c9ccf7708ab25c12968fc153082c59d9502c6c8a356f95845`  
		Last Modified: Tue, 28 Apr 2026 00:19:49 GMT  
		Size: 194.3 KB (194297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a6c5502e3ec4b432f3d8cb82be8c14e89464ef9ba366b2174d702a6ce5baef`  
		Last Modified: Tue, 28 Apr 2026 00:19:49 GMT  
		Size: 24.5 KB (24463 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:2cd20fcef8770276642c334594613ac9855ff2bc52885efca2ae7271195c94cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97260768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06a57e0fe356f2609465963fbeea80887d9e3d2ed113518b974a5339c37729d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:23:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:26:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:26:37 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:26:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:26:37 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:26:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:26:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be625d43eab692ab6fa93bec84eb43dd16970d3d29f19452fa838c31656fda3`  
		Last Modified: Tue, 28 Apr 2026 00:26:52 GMT  
		Size: 290.3 KB (290334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a940d4d379576eb230d86cbe12edf83436fcddaa9c7f262eb578020d7d278`  
		Last Modified: Tue, 28 Apr 2026 00:26:46 GMT  
		Size: 93.5 MB (93462894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7257aee979a6a37fec0e2b5b3db0f977476a72ba27d898ebc85d6a2f518847f4`  
		Last Modified: Tue, 28 Apr 2026 00:26:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a7b2e0262644e4a47100c2c62256be0267d1e0a59f501157cc4e89e81f1235a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfbb4f6cb66fe00876daced02c1bbdf185afa400f12b0cda18ddfb270f3205f`

```dockerfile
```

-	Layers:
	-	`sha256:2473d5a8bf9875ba52d195bb9a423e23e5a103bcbe900b6b6d9ed3c5a297cbe9`  
		Last Modified: Tue, 28 Apr 2026 00:26:52 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:84279847a2277eed8ceb9e24bcd01a1ca96ba3b8a4b9184b394f61d3734705e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96687961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf53835682538728dde4fe136a7a3d167f9c1b46f71bf34251ba810c559cdbf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:21:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:20:37 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:20:37 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:20:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:20:37 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:24:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:24:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14eb0867abeb02e07ef509fc6fd6408cd5b6769dc1209d550382990d9402692b`  
		Last Modified: Tue, 28 Apr 2026 00:24:17 GMT  
		Size: 289.5 KB (289510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d73ddf188a2e2e6775fd1105089506e6b38ccd4ec9defa63926d5363c7b9227`  
		Last Modified: Tue, 28 Apr 2026 00:21:01 GMT  
		Size: 93.2 MB (93172464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90cac8e7262e34f1d0bce9c54c75ba4f4a50d1dd9e3a7ce1c89b27da14c03922`  
		Last Modified: Tue, 28 Apr 2026 00:24:17 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:97e53c5b9d4fb07b3247f6f91905fcec0cffe37f60f7ead526cb8962d82862b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ba092f1089ecbd41348cf6cf4e3b74ef93a0b11a1ff14a4c9c330a6ad07d3b`

```dockerfile
```

-	Layers:
	-	`sha256:1a7435c33e26130576a5d139de10ee259af8c082f3900865a6cb94be57d66cd9`  
		Last Modified: Tue, 28 Apr 2026 00:24:17 GMT  
		Size: 194.3 KB (194301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7549a2519fd55531df8a8cea23304740dbd40020b573036c4f7d182fea0334f9`  
		Last Modified: Tue, 28 Apr 2026 00:24:17 GMT  
		Size: 24.6 KB (24576 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:10ee4f2a084e41563396600d426cc1021f09422c11b9a771bb49dac66b7359d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96473641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8dd458d23394d1ae3c9c62afe9c323eab0bafdf86a69b7f9b26c772feb9f1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:17:37 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:19:24 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:19:24 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:19:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:19:24 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:19:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:19:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a004d4be58a5b0bc95e38a2b59a8d9efa8afd65c73f523ac495e3bc8c46d9c68`  
		Last Modified: Tue, 28 Apr 2026 00:19:42 GMT  
		Size: 291.9 KB (291902 bytes)  
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

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e29e54bfd5653e6829cea0e9031d3384677a3f4f2e44cf419e47cd7d09f94a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 KB (218927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda215ab0da802f756ef22fcda72814e4062d3358a94417a5880d119bdf639e8`

```dockerfile
```

-	Layers:
	-	`sha256:72b2940d8b7e78fff0c787da7ff4df1a329d38afcfb0248427d5d8c7966c7fa3`  
		Last Modified: Tue, 28 Apr 2026 00:19:41 GMT  
		Size: 194.3 KB (194329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df09d8b8b33b02b0ed50300d9222cc2c787235cbdd3ee580792cb01387b79577`  
		Last Modified: Tue, 28 Apr 2026 00:19:41 GMT  
		Size: 24.6 KB (24598 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:8e7f51a386962fa0fa3c0eeeb4e1898b366f4a82e6eecf56dfe761990ef45a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (99002640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40db44ed4aae176f5124d1972b9d2a1a61237356dcfc3b9f5d8ec6e3e2f39dfd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:22:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:21:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:21:39 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:21:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:21:39 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:24:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:24:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76543ffbfa39fd25e5aa94718b223eb380d265668b7274829e5a8d8067408869`  
		Last Modified: Tue, 28 Apr 2026 00:24:46 GMT  
		Size: 289.9 KB (289940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d6a9c589b969b9eee8b2fb5a3d53dcb1feacb04a0d56a4902866f913a72511`  
		Last Modified: Tue, 28 Apr 2026 00:22:10 GMT  
		Size: 95.1 MB (95087823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee624035e7efc0b532bb4341a3bc9d7b5a4986d0464b83930ab9610bc2ae90d`  
		Last Modified: Tue, 28 Apr 2026 00:24:46 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:64af96f21efddf970e825ff4457d765eb9b2460b3c22f6e4ca9ec5f1c4eec3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b1cac8515d71c5b5421f0c94712f324bf44de84a51b9795d2a91e84c86fb89`

```dockerfile
```

-	Layers:
	-	`sha256:c62fe64e79830eaed24249ecbf13bc6ef0a87f94975623ce7589da5ca550ed33`  
		Last Modified: Tue, 28 Apr 2026 00:24:46 GMT  
		Size: 194.3 KB (194266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f1c794606f2e84b604f1a87c920ae3d8b07e2a69f45f7dacccaaabdc03ec19`  
		Last Modified: Tue, 28 Apr 2026 00:24:46 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:8deb4a484cbfcf8de32c60a4183470107cb57cba70619e07e267ead4572ff09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97926791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:462c8043bcdcc3d9c6ccc0555ca5c595050a558d2488c0219cf9fad3dd4d3ad6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:17:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:21:51 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:21:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:21:51 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:27:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:27:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573996c1704299f203b95192cb9a61f40867e3dd7bfdbb9d3428c371304bd492`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 292.4 KB (292441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e34165e157d14e975c070ad73c3dbd1767de1fa84e282e6505d64626df00ff3`  
		Last Modified: Tue, 28 Apr 2026 00:23:11 GMT  
		Size: 93.9 MB (93897536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba0c8872704ce01945d95bc50d56bc5291bc92ba1bb13ce86e53cced4ff7f6`  
		Last Modified: Tue, 28 Apr 2026 00:27:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:abe789066c4714bae9d88e604981d0e1a21193046634ca48e056500150749324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b0f5e4e0d0fd1f2728b5fb0b60fd10db780adc6bc9081f56f7004c5335ac0`

```dockerfile
```

-	Layers:
	-	`sha256:8ff18feb5c092c3cd9bf724168447963757c0c4707522a92fa162edec2193d61`  
		Last Modified: Tue, 28 Apr 2026 00:27:16 GMT  
		Size: 192.4 KB (192384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d8c975390c1a9edee58f766855ef6bf4b8764c7768edb512b021640a5c8110a`  
		Last Modified: Tue, 28 Apr 2026 00:27:16 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:0a5cddd7d02fb8be9a91e681afaa710369562c3ba6797f4681c77ab437beb101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98234713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1979108ff76d7e9b0bec4dd0fa975482539c32505fc2f7da68b98d4323c5612`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 01:45:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:56:48 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:56:48 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:56:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:56:48 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 02:25:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 02:25:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e48325e06ab8f03302d19014bd8681498f11993eba6b2fa96b633d7c283c8e`  
		Last Modified: Tue, 28 Apr 2026 02:26:34 GMT  
		Size: 289.8 KB (289807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f21692e8d3232006360c86abeb47c76c05ae0fd9556f2ba4bef366f9fde74f`  
		Last Modified: Tue, 28 Apr 2026 01:03:40 GMT  
		Size: 94.4 MB (94423868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695f371846318d02f1cf09cd5c6642148205d594756756802f6a786f210a219c`  
		Last Modified: Tue, 28 Apr 2026 02:26:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:983a9d1026bcedd6fac1862bcdb43a1b764b6527074150b3c1c892adaffb4e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822fdfd1aee616dccef518bbeed88a8a5864b6acacc46e2eda92f05817d67222`

```dockerfile
```

-	Layers:
	-	`sha256:e9928e41a1cece87a394c529feba92f40a7b0d147023f1b677fde118e857db00`  
		Last Modified: Tue, 28 Apr 2026 02:26:34 GMT  
		Size: 192.4 KB (192380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652fc3f0177e3e71e574f164a411ccc14ecf114520bbc80a017ff7979f534df4`  
		Last Modified: Tue, 28 Apr 2026 02:26:34 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:025139bdf7c25b4e34bd6e2196405b5c191f8050801aaf3d110b5dd499821c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99825972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81934b2f1816f4142d1d2a43e865a51ef0791df3adee2fca5f51bb0783c76b8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 00:35:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 28 Apr 2026 00:35:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 28 Apr 2026 00:35:11 GMT
ENV GOPATH=/go
# Tue, 28 Apr 2026 00:35:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 00:35:11 GMT
COPY /target/ / # buildkit
# Tue, 28 Apr 2026 00:35:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 28 Apr 2026 00:35:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f711787d93515d1c022f8ca72a087b892fecb332af079850218816693d132915`  
		Last Modified: Tue, 28 Apr 2026 00:37:20 GMT  
		Size: 290.5 KB (290483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c795090f7b3ba987c0e4ca6fd1eb3c889fe964ab0c0eb932bae581f24e4f796`  
		Last Modified: Tue, 28 Apr 2026 00:37:36 GMT  
		Size: 95.9 MB (95881458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fe059f7702d0aa88d98d016dfb076302d52f77338e2ea72d3a191f3922e544`  
		Last Modified: Tue, 28 Apr 2026 00:37:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5193ae0278c86926f8667dfe05acfeb8b236b4bf6325b24da753bf184878a694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072e71c430abbd2e47f667bf02abc1a05aa43cbeb427f8ae2a6fa9afb714b35a`

```dockerfile
```

-	Layers:
	-	`sha256:5ce54a5f01b915eecbbd8d84e4ae782ce90fd9d6d7c82b5bd68b78eca062e877`  
		Last Modified: Tue, 28 Apr 2026 00:37:18 GMT  
		Size: 193.1 KB (193094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e01115169c0343a5b3b571e4c18d980bb51ce82fabca70935248b610969a9f6`  
		Last Modified: Tue, 28 Apr 2026 00:37:18 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
