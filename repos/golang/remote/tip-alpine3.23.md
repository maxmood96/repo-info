## `golang:tip-alpine3.23`

```console
$ docker pull golang@sha256:fd137a1a46537e6e63e8c7312de9022127dd4f28c5c519738e740eb52269b8c9
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
$ docker pull golang@sha256:02bddd7b89bc740f027448074d9c25436506d5aac095738b353202be7207b769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101693391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc6e60451e74a58c9b4676b26a98f81a2335ac11aed5da49ef0ee42e390a505`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:02:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:04:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:04:11 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:04:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:11 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:04:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:04:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbc447fc5ce7db5d0b2aaf24263f8e01939a630f3558048a6499de93322a2ec`  
		Last Modified: Tue, 05 May 2026 23:04:28 GMT  
		Size: 290.2 KB (290235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32be2e0f5add9aa550a86f2638e1a5bddb598fef09f796f2626b736ae1c11c9`  
		Last Modified: Tue, 05 May 2026 23:04:31 GMT  
		Size: 97.5 MB (97538809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4032a60b16f98bbf84782f767abcf4f1be0195b1382baef0e72611a51736650e`  
		Last Modified: Tue, 05 May 2026 23:04:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:9fafe96610b2da7689284b0c52de758ba1d599da049d0404f822600116ead6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88407cd562bf56aba08106c63580b02fc4dd1126710c71b29c8d9b581446bab`

```dockerfile
```

-	Layers:
	-	`sha256:b78a7576cd22170f3a79c826b0230f67dbbe95e0ee13a4915ccc3cce15e98662`  
		Last Modified: Tue, 05 May 2026 23:04:29 GMT  
		Size: 193.6 KB (193648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9992190531dd7ad86d3d1fb558d94ccf1e7ddd85f5874d16f0af222d7e254cf`  
		Last Modified: Tue, 05 May 2026 23:04:29 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:d27d8d02b5f5e07fab1cb398c0c914dcb2875252eaf2df15463f0210cfedb52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97525160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e07e84aeb1d7b690e5b4d22cde0b117ad56def8472e63a34d798d17a82a7069`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:01:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:04:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:04:40 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:04:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:40 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:04:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:04:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781908808ede81284789ad864b8cfcdbc124a854cc1c135dcf932eafe84c5e7d`  
		Last Modified: Tue, 05 May 2026 23:04:56 GMT  
		Size: 291.0 KB (291013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63da960de4dc7ce914df12e6e4e0869a4439909a8959fdba48a5cd0d07b76f40`  
		Last Modified: Tue, 05 May 2026 23:04:58 GMT  
		Size: 93.7 MB (93662126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cebde42109e5665ddbdb422827b2a0bbec29c32343816b97d26bea61045674f`  
		Last Modified: Tue, 05 May 2026 23:04:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:256829cae39ffd07cebcd4fb8a4dab6ec560b99ef2aa74d9582db06fd072c422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 KB (25007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53411b9496610db28c435abcc38b373c676db11b1bb310d87c536723eccfd4b2`

```dockerfile
```

-	Layers:
	-	`sha256:6003cb127e23a326a93b5d54f97714cfbf67f68291ee662c5b443a1d00d5c375`  
		Last Modified: Tue, 05 May 2026 23:04:56 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:5342452c0251b325e29ab7ef009d8e964f7335922013361bfe9ea878dfac8aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96952479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a8dd2444c079dfe73859d995a2da6c6e13038ee80a97a7910a7926ed84cfae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:06:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:09:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:09:19 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:09:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:09:19 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:09:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:09:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f13997a90230b73ebc771c3f9b17a17c0a657ddcbd65415c6b8b25533ba39b`  
		Last Modified: Tue, 05 May 2026 23:09:37 GMT  
		Size: 290.2 KB (290168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7124712ceb426f7d5ea56fbdf12ab02ae56c25941c6892b6e8ce38b9f03ee67d`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 93.4 MB (93379030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e56bff5a0527f0e2a3f5cab3df9b34073a30a9c6fe5492eb205748eaa3ed9`  
		Last Modified: Tue, 05 May 2026 23:09:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d07571b9e1b8edc5ff099516648f54033a2a91efecccf583e1ae6a013d61102d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b74ab937c2a54c985e4983b8aa5aa89085f6980eb40f10013a8e2a423fc226`

```dockerfile
```

-	Layers:
	-	`sha256:66ecd99a0598c4fe765cb8899741485e7aa16109da6c1943c7476d0567ef102f`  
		Last Modified: Tue, 05 May 2026 23:09:37 GMT  
		Size: 193.0 KB (193018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86425e7bed89f63af420e632a1ea9f097359031e06ce6d73bcbceb37e0339778`  
		Last Modified: Tue, 05 May 2026 23:09:37 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9d2610902e5ac471ed3ce394c6b7576b3374cb3f48cc349db5fd59203c43a27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96735234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a72e8ea4a35d13b0d91730b26273b7789531278210f342bb7e68c681c2ed85`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:02:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:04:25 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:04:25 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:04:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:04:25 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:04:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:04:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1e9f410288d0a4af9556cff06e208c8c758480e395309fd4ff7e960e7678f6`  
		Last Modified: Tue, 05 May 2026 23:04:43 GMT  
		Size: 292.8 KB (292843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310d7048cbd083a777980fa032397ddcbb87e03b5b4b31ddec2b7fa305c5ce5`  
		Last Modified: Tue, 05 May 2026 23:04:45 GMT  
		Size: 92.2 MB (92242363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4054ab57cf1be20967faf6d4962435cea2bafb2daf3aba6852eff64413555f`  
		Last Modified: Tue, 05 May 2026 23:04:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:e6f0e5b18076071a3c40fb62222ca67ca7be7c17dc392712f678b45d12e2e00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 KB (218307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b83e6cc5abeea00cbeadc733c5d268f7cf4e0aaa218919b67757b4639f4cceb`

```dockerfile
```

-	Layers:
	-	`sha256:e3cb0aaf1d54594c1609e7383e468aeebad19e39e36d3b162c194a95f2758c2e`  
		Last Modified: Tue, 05 May 2026 23:04:43 GMT  
		Size: 193.1 KB (193054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1897d7772a40243e3be527047d867b09ba88234a2c3f098d55f9630f58bd19bd`  
		Last Modified: Tue, 05 May 2026 23:04:43 GMT  
		Size: 25.3 KB (25253 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:4656145527ebe70f874bec861b2dd85976c588d75580a68464fb198c584f4817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99261065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e91104faa5c0ef3957fd23d47b955c9521845fd74c11c42fdc37800d57e2084`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:03:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:05:18 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:05:18 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:05:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:05:18 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:05:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:05:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63de44fe0258348ccfe9e27b9322211bd1696f1777663bbe3103e9a1d4fedf7f`  
		Last Modified: Tue, 05 May 2026 23:05:35 GMT  
		Size: 290.6 KB (290631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044b12f480be5869cc9862686abcdcfb3464484b704815a3a70c6077d05037bb`  
		Last Modified: Tue, 05 May 2026 23:01:30 GMT  
		Size: 95.3 MB (95279830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c2f7dea380e6f5a1b3685fd3548c91a431560cb6e9e7c7f7ead71723932839`  
		Last Modified: Tue, 05 May 2026 23:05:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:944cbf7173cded5f2ab117ebae805453af3d86976b6373acefa3bcace35622ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa4ccf47aa456f5cbedd72424eb945a2ebc7b7d7342bd8edf0996874ef55991`

```dockerfile
```

-	Layers:
	-	`sha256:6e133a120cacecb724ad50e8c1893625e7107117396c52a869062d20862db27e`  
		Last Modified: Tue, 05 May 2026 23:05:35 GMT  
		Size: 193.6 KB (193607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc50fc984270f0d577ba415f5003045d5774ab8d94bf2f3c223d11a490593e7f`  
		Last Modified: Tue, 05 May 2026 23:05:35 GMT  
		Size: 25.1 KB (25052 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:484f1a36371ea59bdb6427972cad9188937fc442413858ffab99fdbc697dde8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.3 MB (98253128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15f2724dbe418fcd3ad5b0ff4e6612bb8000761693b55a1a6558aa04aeef334`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:40:06 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:40:06 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:40:06 GMT
COPY /target/ / # buildkit
# Tue, 05 May 2026 23:45:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 05 May 2026 23:45:32 GMT
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
	-	`sha256:df66d548befa9f03e6fb22cc6385677d9c13ab71d11ae10a9cbc0d2e3d0efc16`  
		Last Modified: Tue, 05 May 2026 23:41:42 GMT  
		Size: 94.1 MB (94128677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894b6c3f959c1e1b9aa7c63f88fde53d04f37f9f02c93c51254f8b556b82efbf`  
		Last Modified: Tue, 05 May 2026 23:45:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:77b4de094993cc305c0c602c56507572fc84e5b9e49f72c650be0b4ab55b6964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 KB (218200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02600e98a72aabbfcdee0b306143ff374c629aa4df1c5affdae6dddb04023647`

```dockerfile
```

-	Layers:
	-	`sha256:bae13537c04d4688dc316bfe671fcc957fdf3f5d2f675333d85caea63ad2e449`  
		Last Modified: Tue, 05 May 2026 23:45:50 GMT  
		Size: 193.0 KB (193047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a06c5c24d2733e2c72748ab5dba1ca55d2ed9b20243c373daa72341c4a3b1fb`  
		Last Modified: Tue, 05 May 2026 23:45:50 GMT  
		Size: 25.2 KB (25153 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.23` - linux; riscv64

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

### `golang:tip-alpine3.23` - unknown; unknown

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

### `golang:tip-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:3943b227636ce29e265ade5de746cc282b11a90100c0be2db2414211d2206d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100123430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606f2d9899d192940f768435bf7fd6a298e80589021b4a9e550fd4b527bab82c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 04 May 2026 19:09:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 05 May 2026 23:58:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 05 May 2026 23:58:52 GMT
ENV GOPATH=/go
# Tue, 05 May 2026 23:58:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:58:52 GMT
COPY /target/ / # buildkit
# Wed, 06 May 2026 00:02:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 06 May 2026 00:02:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb85227a6d474422f642a20f11c0f9c523b2abb74d9032c4b7170dedd36bf4`  
		Last Modified: Mon, 04 May 2026 19:09:22 GMT  
		Size: 291.1 KB (291150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d2604867f1d33ea36e2647b9da201fb796e01f541d58d01f7899b6b2cfc20d4`  
		Last Modified: Wed, 06 May 2026 00:00:26 GMT  
		Size: 96.1 MB (96105590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408687b1ac63739dd51dd03d8ab863924e6486ee0257b1cff6b296fec41833c9`  
		Last Modified: Wed, 06 May 2026 00:02:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:ba13d2c3bbc168de33bd282efba3409533334790a872354e8f9a5d5508a69e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c6e34286248b9d1ef9d95b18d0bf6d3a642934a7a7fc15784563cf52b01d2b`

```dockerfile
```

-	Layers:
	-	`sha256:88db71d503356143315306011db63eac38e3b8db9d85021c5330d35b722573db`  
		Last Modified: Wed, 06 May 2026 00:02:50 GMT  
		Size: 193.7 KB (193745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4901c9d706c71e92859974edd0a2a46ade27775429518b0173ca55238c130d`  
		Last Modified: Wed, 06 May 2026 00:02:50 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json
