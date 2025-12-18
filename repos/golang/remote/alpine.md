## `golang:alpine`

```console
$ docker pull golang@sha256:72567335df90b4ed71c01bf91fb5f8cc09fc4d5f6f21e183a085bafc7ae1bec8
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

### `golang:alpine` - linux; amd64

```console
$ docker pull golang@sha256:301db1784c200c7ec221a84672d0bd3ffdcf6c873bc9806482bbe730910924fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64307662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef5200fdbf03c03780e5f7356c20c226596c5130d1019491b49d2ae7968133e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:38:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 00:38:57 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 00:38:57 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 00:38:57 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 00:38:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:38:57 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 00:38:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 00:38:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f62578bcef03586d252ea1bc3a3f2f936e5bc570a754bd62e098f67225c6e`  
		Last Modified: Thu, 18 Dec 2025 00:39:18 GMT  
		Size: 296.1 KB (296085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c445a0e108b509dd422d6adce512f16cb7edd37814e8e3509850820377bcf06`  
		Last Modified: Tue, 02 Dec 2025 17:47:39 GMT  
		Size: 60.2 MB (60151314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e8847bf924ea4cced11c4db1360c8c8ba93cdeeced7418f48f430e219ebf94`  
		Last Modified: Thu, 18 Dec 2025 00:39:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:661ae635cdcaa7640ae4bf7ddb7cd96ddf501702f69ae4aa2be5bf7b06b49ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 KB (221577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30393b0c3be10409c08ee483d609237ac5eec4f2bc477d20162b2af6929a2def`

```dockerfile
```

-	Layers:
	-	`sha256:c322c874d1bf1fdde0630e0f80e52a4d68538b08fe28a90c091ca4dcd27e664c`  
		Last Modified: Thu, 18 Dec 2025 03:22:39 GMT  
		Size: 195.6 KB (195551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab11de777f96416fed74ec944a25c4074eed435d45c4de25eea1851360aefd5`  
		Last Modified: Thu, 18 Dec 2025 03:22:40 GMT  
		Size: 26.0 KB (26026 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:8d01664fd71a5bc824349b36e09a119cb9f348009be779d6cf9041a2425a13c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62937804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfeaf8a82dede2132e7f82f8efd056e4f1f55033cbcd0451e6533de55e100e3d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 00:49:27 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 00:49:27 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 00:49:27 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 00:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:49:27 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 00:49:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 00:49:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0b4aceab4dd75ad1177c2257f0f4a318ef46f1f0ef211b18cc744783b68394`  
		Last Modified: Thu, 18 Dec 2025 00:49:13 GMT  
		Size: 297.3 KB (297259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43dd4211ee5273ca0c5772840c1a03b86bde39c606d1c608d88cc81d6d76501`  
		Last Modified: Tue, 02 Dec 2025 17:47:55 GMT  
		Size: 59.1 MB (59071955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a708e9bd95398fb9c47ace31045e51bd27a85c6b0bfe5638f4b68203b825c0c1`  
		Last Modified: Thu, 18 Dec 2025 00:49:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a3e884e112bbcbc0c5c107cb5544d6110055ded2db8caa4ac112ed8fe6e57a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4a209a72e0d4bee217d36b8d6aa5b961560c87154a55082c3ba7548888cb64`

```dockerfile
```

-	Layers:
	-	`sha256:b3a46007aae99888170c19a0184abfc6a7d020a39440d76017df0ea8bf4591f5`  
		Last Modified: Thu, 18 Dec 2025 03:22:43 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:e4385555e472ec4f519060b4e106d3775ac8092da87330b7901d23cb79ee0dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62647800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4764c223c6667c827e94fd90f328975e2ae1b29d17513676ffd86ca9d2426b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:49:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 00:50:57 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 00:50:57 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 00:50:57 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 00:50:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:50:57 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 00:51:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 00:51:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7cf52454d442bb5efdbc9b01026f9f52a6a0d103e5faefde30fdb2c006e296`  
		Last Modified: Thu, 18 Dec 2025 00:50:34 GMT  
		Size: 296.2 KB (296192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952f3ceca6918c986252a293f498004b3365bf2efd3e1b6be9d754f9e7c62cfe`  
		Last Modified: Tue, 02 Dec 2025 17:49:21 GMT  
		Size: 59.1 MB (59072062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19244fa39f840cc1df0f3ec37ff3a0b960872f2b8ef7f34246145808a9b7974c`  
		Last Modified: Thu, 18 Dec 2025 00:51:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e57c97bafa48df731d9b2a6e97a5445727a729a0c7a9cda9e72b9685cd5f6184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80215b1097dd9f0b847104dbcea0ea0ce7254f8b939638c2dc6eb6410d80e4f`

```dockerfile
```

-	Layers:
	-	`sha256:6c13dac2c1166edb5374ca9a367fb78e63b188f9d5f9f125ac5e53ca394044e4`  
		Last Modified: Thu, 18 Dec 2025 03:22:47 GMT  
		Size: 195.0 KB (194955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c036e40f76ba584dd89cf6a9ea3eb873f80e399d6d5980d80b9204bef175de`  
		Last Modified: Thu, 18 Dec 2025 03:22:47 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:96bcb423a22896723f8ddddf96186d671ba71644af6c40067a27159d28ec0b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62145655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6e48b664c25560ddd69645297c0b6abc89bc5f8defc09e4fba247b180e2a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:40:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 00:40:08 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 00:40:08 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 00:40:08 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 00:40:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:40:08 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 00:40:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 00:40:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294fa12b0127508a2d6cf922b62615c731ef5506d094999bd13c7a2fc4a87f83`  
		Last Modified: Thu, 18 Dec 2025 00:40:28 GMT  
		Size: 298.8 KB (298842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0562e970c9af953828c5cdc69b3e362c523c3064c669aa8dda79020032e840`  
		Last Modified: Tue, 02 Dec 2025 17:48:05 GMT  
		Size: 57.7 MB (57650917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c3c411d5f38c19e020422a9837452b90cf1a25e6caf16104027e99e5b1a276`  
		Last Modified: Thu, 18 Dec 2025 00:40:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:f6c57b19dbc81c345e1d8c4be35dcb8350d70ad3f633ddeec1e64a793f3653a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 KB (221214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34dcb8efe843509cca67273b99b1550bd164e14bfe0d655d49e3d0e9e85de62d`

```dockerfile
```

-	Layers:
	-	`sha256:7b0a110cb33e75be70a3dbaf9c866f60a4c5e4498b57192b4a55f3b9d5414230`  
		Last Modified: Thu, 18 Dec 2025 03:22:51 GMT  
		Size: 195.0 KB (195005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40555ec66de47ff22c04aadf8e9d5352e47ae5e01b29c5ce3de51dcdc7403f78`  
		Last Modified: Thu, 18 Dec 2025 03:22:52 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; 386

```console
$ docker pull golang@sha256:f8f784f478e37b032640fcd0fa31b1f1bd0d79dd36a746161b62c52e8763d290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62854871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a6886a4186da5e3741c558faadab882ae446916853447f45fbe1df30022240`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:38:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 00:39:00 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 00:39:00 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 00:39:00 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 00:39:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 00:39:00 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 00:39:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 00:39:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc0da2488fa39ae76f5b21517256906e44d753613991fd887c3df200ed7b310`  
		Last Modified: Thu, 18 Dec 2025 00:39:22 GMT  
		Size: 296.7 KB (296675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b714db6db5fd611306e3219023556e73fccd367a39f79eb9eb020ec36684466f`  
		Last Modified: Tue, 02 Dec 2025 17:48:21 GMT  
		Size: 58.9 MB (58871938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0a3e450842fcf39fc65a439089780c5621e7d5dfb7661f56f7689e0fe1284`  
		Last Modified: Thu, 18 Dec 2025 00:39:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a771a250bfc3ddedf697444cd5687066b06e170a6f9884186cdfa01ae5708c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 KB (221463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36646491e515e8d28646507be567b31dbef09b6d16339099496515b78b9820c5`

```dockerfile
```

-	Layers:
	-	`sha256:d51195b1e1fa623155e06bad059c00defa4f83c0cfc13f0d7029ccc317f40483`  
		Last Modified: Thu, 18 Dec 2025 03:22:55 GMT  
		Size: 195.5 KB (195492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:982c45252a00e37ca8505d58e34893fd4f445705f810d0a3a02973771d19acbc`  
		Last Modified: Thu, 18 Dec 2025 03:22:55 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:346c6612554333674b106f41b9452d36a57c6dba0df2462d3e9341013f132129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62262116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e846db069c90d8557289d315da0cf24ae0b89dfaecdd822e5ccab379b87f14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:36:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:38:02 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:38:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:38:02 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 01:38:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 01:38:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251744709998ea3415429d77aa83c1ba367b71bf12c4b11c84d3ff1d0c4b550`  
		Last Modified: Thu, 18 Dec 2025 01:37:40 GMT  
		Size: 299.3 KB (299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0da503e4b3d4a624ac596179648e9a31a4f87f7d37fdb8c7bef57190d6ed7d`  
		Last Modified: Tue, 02 Dec 2025 17:48:12 GMT  
		Size: 58.1 MB (58134946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b025d3f5bb15296b9a1493b9f64902107fe77fd4224fe798265fe3c99d0d4d15`  
		Last Modified: Thu, 18 Dec 2025 01:38:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d18c2808797f1bbde009695d0d4f778b9655d5c39bdd00d8d56520c765dbb33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2c807478f483e543505bc8bcdebd59959ef4316830e0d2e03df0f234fb3fe7`

```dockerfile
```

-	Layers:
	-	`sha256:50a426fa4a41b433e61b57bd1018a6373a496ab7296803634273fddc1a6abba7`  
		Last Modified: Thu, 18 Dec 2025 03:22:59 GMT  
		Size: 195.0 KB (194972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5ea346dd7abe953a214adf688b6cc2253d2351333a3f695a8f6eabb2d3997a`  
		Last Modified: Thu, 18 Dec 2025 03:23:00 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; riscv64

```console
$ docker pull golang@sha256:009cd01eccb1b02c7cbd68719992b3cba77079f7bde5d72595bd7cd1e34555fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62552624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6501029fd2cbbc6751b4e5eaf2e7f1f24d71f28dad61a8bcd35f4bd604c5e67`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:32:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:21 GMT
COPY /target/ / # buildkit
# Thu, 04 Dec 2025 00:33:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 04 Dec 2025 00:33:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee2260aaa09ba7162340fe5926c0fe305f447e406ba4020d7a84ed8048186cd`  
		Last Modified: Thu, 04 Dec 2025 00:35:11 GMT  
		Size: 296.5 KB (296503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d978112d183a69e7d1bc8e0eef2604cc2b23d417a71ea00afe822473ce9c84`  
		Last Modified: Thu, 04 Dec 2025 00:35:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:de6d74cabdb803d8b5f00ddb797c5afa0bb10e79dd3ad1e448271b157a567023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6360eb0c1136d1c40197a0e068088cf9d1ce83475db78e6877fad41225a698`

```dockerfile
```

-	Layers:
	-	`sha256:0eec3f22a27652a8b3204658719b421d90d4069304d93d5a0c72af9ad80e0f13`  
		Last Modified: Thu, 04 Dec 2025 03:23:38 GMT  
		Size: 195.0 KB (194968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d873a2a6807fc61f86582e681d4887592b8754e5cc931654997223789642305`  
		Last Modified: Thu, 04 Dec 2025 03:23:42 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine` - linux; s390x

```console
$ docker pull golang@sha256:9857f0550237878cedb3c9454619177a7a6e498445e4725a03b49437cae0123d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63508881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b84b63f874875c27d1d4cc180edecd20eca70a74431c43d5f931ff064ae75bf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:14:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 18 Dec 2025 01:15:01 GMT
ENV GOLANG_VERSION=1.25.5
# Thu, 18 Dec 2025 01:15:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 18 Dec 2025 01:15:01 GMT
ENV GOPATH=/go
# Thu, 18 Dec 2025 01:15:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Dec 2025 01:15:01 GMT
COPY /target/ / # buildkit
# Thu, 18 Dec 2025 01:15:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 18 Dec 2025 01:15:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7224d7d29671ca737c9ec945a7373478caed2bbfb74b122f8685b8c92149198`  
		Last Modified: Thu, 18 Dec 2025 01:15:01 GMT  
		Size: 297.2 KB (297192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036b6dba2ceabbb92eb6c9ebccd3e6b705dacf7cc4426156bbedfd17ad5dc53b`  
		Last Modified: Tue, 02 Dec 2025 17:49:47 GMT  
		Size: 59.5 MB (59487220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdc2a94dbbe6b03332841a468ce672afab0082c1295b9d6e86d90fb4ae00b32`  
		Last Modified: Thu, 18 Dec 2025 01:15:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine` - unknown; unknown

```console
$ docker pull golang@sha256:87d9d8f820d61adcac8d8076cd4de81d5a4159680105149d081e7fe15ccabd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88c47312c0b931166744d1c7fe226b466f3af9415384de8f9f9632b38e02f31`

```dockerfile
```

-	Layers:
	-	`sha256:d221e5101a16dc4e9f96a1fab62319716a65788780d51ebddec753cd706c3a48`  
		Last Modified: Thu, 18 Dec 2025 03:23:05 GMT  
		Size: 194.9 KB (194900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6411333120e80bccc1c1896b7d9375543f6561baccdabe46badd685398b78324`  
		Last Modified: Thu, 18 Dec 2025 03:23:06 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json
