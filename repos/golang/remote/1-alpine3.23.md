## `golang:1-alpine3.23`

```console
$ docker pull golang@sha256:f4622e3bed9b03190609db905ac4b02bba2368ba7e62a6ad4ac6868d2818d314
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

### `golang:1-alpine3.23` - linux; amd64

```console
$ docker pull golang@sha256:724e212d86d79b45b7ace725b44ff3b6c2684bfd3131c43d5d60441de151d98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.3 MB (64315034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2677ed46f77ca520058f87d51be06147f6f09ba7eed4ec59858310de09399f88`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:04:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:22 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:22 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:22 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4482833354056f4a91314c5e27db3f838d4c373310fc6a0cede54231bdf1124`  
		Last Modified: Wed, 04 Feb 2026 17:04:37 GMT  
		Size: 296.1 KB (296082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdf71b47847e47b44531d019e8eed7d243fd7189fe6b14cf6754724b04fbdd6`  
		Last Modified: Wed, 04 Feb 2026 17:04:15 GMT  
		Size: 60.2 MB (60156973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2882870326d12f2187dd62331537510b301d4cff1fd48b13312c6542c5d372`  
		Last Modified: Wed, 04 Feb 2026 17:04:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:4443dc8b8181bedc5432ea37a4eb9f0def1066fa4d77a1d8fa05d81740938222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 KB (221578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f5ea0607a0597f63e2092c17c114f3572192b0191854f72c5755dff1b6c92e`

```dockerfile
```

-	Layers:
	-	`sha256:905a178a1486ad164fac9f735d9506daa84ad1b368f023326ef9cecb9273009c`  
		Last Modified: Wed, 04 Feb 2026 17:04:37 GMT  
		Size: 195.6 KB (195551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026e66f82c87c9c8bf2143fd963e02a3e86db45225836de4f9893fee6b3fdc8c`  
		Last Modified: Wed, 04 Feb 2026 17:04:37 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v6

```console
$ docker pull golang@sha256:86e97884b8022437cc0df50f12beed5429a7a242a8085fdc242d5330435d7e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62943370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d6691f6430cf6b728cf8069e7ced11a8dfab4879a9775c3635ecfb81550c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:04:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:37 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:37 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:37 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30e9cf8969b142a022e82d3ccfc0f13b5291a4087528025e7bc75c915ecb7b`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 297.3 KB (297257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4a839dcd7f0a026f4b21f2e42b36e1fcba806c26b99b4544e89678a699bf5c`  
		Last Modified: Wed, 04 Feb 2026 17:04:39 GMT  
		Size: 59.1 MB (59076135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0599c705047f1bf1b345927ae5930229d0f733cef29f11aabaaf28dd28a5a`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:574b4d51088a993e0fe44be61bf52da39da97fe5e6479b9b275b83a854b4e826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562414356bba27903830410cf05a7f9567be004a774b741bc6ac6acb4c65773`

```dockerfile
```

-	Layers:
	-	`sha256:dd2b923198661cc22ad8c5a870d19a4cd21a20086b6e006a916a0e772bec56bc`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 25.9 KB (25950 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm variant v7

```console
$ docker pull golang@sha256:58f54b370acd55c303ef01c952aea0fb06b676481ac8c0f59f6386137941d956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62654241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071fee076d5b1fa03e2ce778b64965d1d0a22b643f0b36ef365a708fdde55f77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:03:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:03:41 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:03:41 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:03:41 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:03:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:03:41 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:03:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:03:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580391213e4360b82eea1904965276b80b3dd05d8d65eb98a65a4fcb3d610789`  
		Last Modified: Wed, 04 Feb 2026 17:03:58 GMT  
		Size: 296.2 KB (296194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7b7e6ac913cf5db56d036aaf335904f49acbba9f9a6464379470983dced635`  
		Last Modified: Wed, 04 Feb 2026 17:03:51 GMT  
		Size: 59.1 MB (59076165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a6af232a36a4a5bbd296a1eb40290eb1f245ffc667ac2336ffcd9cdbbf616d`  
		Last Modified: Wed, 04 Feb 2026 17:03:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:dd3ee69c4fc2554da37a04a87f99538279c43dc7ed33562e0d31ac5cc815589d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f542cc16948f6f01fb98d647ff47749ad0c82cf76eb5e555e821cd3a6f5af23`

```dockerfile
```

-	Layers:
	-	`sha256:dde28ceedbdff38953e5b134b4e9d834979881364c78b218c5e973c34103e621`  
		Last Modified: Wed, 04 Feb 2026 17:03:58 GMT  
		Size: 195.0 KB (194955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5d5431154ec0cb261194badf9885ae0af4cf549e4d00bbae3e30830cef8764`  
		Last Modified: Wed, 04 Feb 2026 17:03:57 GMT  
		Size: 26.2 KB (26165 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:01dd9e0c26609cb11ed1be6ad55884853c5e93cb44e189e5b65fc7ad3e1d7506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62149548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabb4d1915ff64e4bfa249baef7babacd71bceeb3908a8e597c85f5e8f7bb522`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:03:52 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:03:59 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:03:59 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:03:59 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:03:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:03:59 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e3891ab53b21d05e57609cafe86c85b81ed0bade3396b3d725f0c0602e0fc0`  
		Last Modified: Wed, 04 Feb 2026 17:04:15 GMT  
		Size: 298.9 KB (298850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fac6022b2ee873ba16b3704e4dc9dfb3d60a32c4c3577bd7c9d971bdb2f1f7`  
		Last Modified: Wed, 04 Feb 2026 17:04:17 GMT  
		Size: 57.7 MB (57653449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0903dbd38af0cc8cfd6ca0b7316f5e521dd72a7e48dbe761d5e281b3ef6f1741`  
		Last Modified: Wed, 04 Feb 2026 17:04:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:c429c0ace69338504b2078fbf5ad8802a7847fcf4bb11e68da0a375ea88589c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 KB (221214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec11b49b87fe3f500c06e819a71a4607a42076139e16b739764c7184c78de0c`

```dockerfile
```

-	Layers:
	-	`sha256:aacb41a1dc488879219c657f467798c6f6b9908d60ee5bda8b74ae31b4f5f19c`  
		Last Modified: Wed, 04 Feb 2026 17:04:15 GMT  
		Size: 195.0 KB (195005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564d23ee5bfea70aecc483bd1cff9d3f73252792d72d3751c057235b6ba7d941`  
		Last Modified: Wed, 04 Feb 2026 17:04:15 GMT  
		Size: 26.2 KB (26209 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; 386

```console
$ docker pull golang@sha256:4eb54ce75a4ea3c96d9c4c93cf11817afd167015bdb24f7c2d711d15ccdf96d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62856735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320ac7d853280ea032fbbfbd03c0290315b9f80bd16851c6f42e713039979b89`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 17:04:12 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:21 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:21 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:21 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:21 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f41140368eda0b0e0daa0ae9bf86f19625924d1d7ed4d241cc86fb20dbc862`  
		Last Modified: Wed, 04 Feb 2026 17:04:35 GMT  
		Size: 296.7 KB (296672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5c0b9aa7ecd0690c22b5272d78803efbb58eb70a587a69b65a9a3f03d3f902`  
		Last Modified: Wed, 04 Feb 2026 17:04:37 GMT  
		Size: 58.9 MB (58872907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24da17566e83107a3795ef8dd0d2f401c0a6758701583d7d39edcc129ff3636`  
		Last Modified: Wed, 04 Feb 2026 17:04:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:511b1c11312dc144d7ec232fdd8543a646157363347883d459ebdcc46d247530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 KB (221463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b331829eedfe02ccf5b88059c8c1d909eec07c19433b1baad8386b99dda1b5e`

```dockerfile
```

-	Layers:
	-	`sha256:91fa28ced9988a14774937ba1d53d221b2c624a1f3d3fbb33a69b71492973662`  
		Last Modified: Wed, 04 Feb 2026 17:04:35 GMT  
		Size: 195.5 KB (195492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1d880284427cfec66e81a7a9a0f714c339c285db8e6573e95341403031c377`  
		Last Modified: Wed, 04 Feb 2026 17:04:35 GMT  
		Size: 26.0 KB (25971 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; ppc64le

```console
$ docker pull golang@sha256:41679a1d9290cc1fa8f50e7afbaa20388bc845d5c806e0f598a892bf2b8404bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62265985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8784b254c9fa8cc674db6bcef5747edf37817acc5a3ad519e218362920dc94e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:05:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:05:37 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:05:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:05:37 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:07:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:07:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd73d3916f2fedeed1c534628f9a66641a5e1350de62984f598c99fe3383aaf`  
		Last Modified: Wed, 28 Jan 2026 04:06:04 GMT  
		Size: 299.3 KB (299261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d69879181021786809c25fc5c953b51116d19e9c3c6d50663a1bdc3a339c1bd`  
		Last Modified: Wed, 04 Feb 2026 17:06:35 GMT  
		Size: 58.1 MB (58136923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3fb7bfe8ce423a42591835c480dfe13c38785ef3f012607a8521215b50caec`  
		Last Modified: Wed, 04 Feb 2026 17:07:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:2df7ca20c2dd1fe4aa778f8cf5b4b0e401f497af23775331e15d437ee0df7b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6837dcc09d85bcefac32b22b32744c6e926e56ee1b381b6fb3a6edba3964e08b`

```dockerfile
```

-	Layers:
	-	`sha256:61ea3b9eff723183e6c8084dc35fd36aa2880f486259ca631f480a4cec9fa390`  
		Last Modified: Wed, 04 Feb 2026 17:07:33 GMT  
		Size: 195.0 KB (194972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f486d9439742cc6145e08a6ad2e3c798f253e156f0bbe9990dd9beb1e64430`  
		Last Modified: Wed, 04 Feb 2026 17:07:33 GMT  
		Size: 25.9 KB (25926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; riscv64

```console
$ docker pull golang@sha256:afeffef75477be3e77cd161adcdf0d433ea04935ae5956076e146f6b2c562969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62553595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc91603173e32487dd04989edce1ea67ad057f52a523e2747affceecfd79f5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOLANG_VERSION=1.25.6
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOTOOLCHAIN=local
# Sun, 18 Jan 2026 23:11:45 GMT
ENV GOPATH=/go
# Sun, 18 Jan 2026 23:11:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Jan 2026 23:11:45 GMT
COPY /target/ / # buildkit
# Thu, 29 Jan 2026 19:19:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 29 Jan 2026 19:19:31 GMT
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
	-	`sha256:76383bda51f6d2301c4d245b282d3ec6e006fd6e4d52961e3dd0dba3364c9182`  
		Last Modified: Sun, 18 Jan 2026 23:14:35 GMT  
		Size: 58.7 MB (58671645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b066f9be4a06b58001fd53bb904e16cb73d78d2437385b5169320c7647e8ab61`  
		Last Modified: Thu, 29 Jan 2026 19:20:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:d814f1814dcdcbcab4adb14695aecedfc02d4d7d4fae0b28e3dfa4055dfe41b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 KB (221067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e05518d6bc075a1f203e03b10c58d80c17e5c09d05c623a7244c22e6a86dc2c`

```dockerfile
```

-	Layers:
	-	`sha256:175f3b656109046939dd6a75afece5206de288bcafa62b2471a1c41266ff17cf`  
		Last Modified: Thu, 29 Jan 2026 19:20:37 GMT  
		Size: 195.0 KB (194968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08f82f468afc3d1bfb3f4cd9f68f0b5c35f5394e468659c6a80049dc7b75c62f`  
		Last Modified: Thu, 29 Jan 2026 19:20:37 GMT  
		Size: 26.1 KB (26099 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.23` - linux; s390x

```console
$ docker pull golang@sha256:7fda040ab506759c48db39e925ecd36e3a2b6df4c15832fff8fcc76247f46405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63516806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414df5f356713509e718034ac252e7e0a996ad544954c60212c5197d74c2b53e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:07:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOTOOLCHAIN=local
# Wed, 04 Feb 2026 17:04:03 GMT
ENV GOPATH=/go
# Wed, 04 Feb 2026 17:04:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 17:04:03 GMT
COPY /target/ / # buildkit
# Wed, 04 Feb 2026 17:04:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 04 Feb 2026 17:04:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b19da3a82072794d62dde7afbbfd822a592c5dfe5b82c058d3ec326c23cca53`  
		Last Modified: Wed, 28 Jan 2026 03:07:58 GMT  
		Size: 297.2 KB (297176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8f0a3fdc9e8378ae51ec0652c2aa7b3fe566439364495bae28720620458ab`  
		Last Modified: Wed, 04 Feb 2026 17:04:51 GMT  
		Size: 59.5 MB (59494139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2e1653a8456391f7e1d1dedf3d83c022179955432539021f81e7e83724f062`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.23` - unknown; unknown

```console
$ docker pull golang@sha256:b5cd0bfcb0e076089c0d13e45a5751aaf074a796b4d589e35b55dfb746a55712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 KB (220926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd395ff6fdcab17419df5817efcb4561665554f30ffbb505a550c0a803e74146`

```dockerfile
```

-	Layers:
	-	`sha256:4683bf4032b9a3a6aed1e35d373bbec2a841aa1ea30a7c238aa18ab3f4ab1b99`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 194.9 KB (194900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b21c9120922172eff61154548bd18141a3dc22b481ab20c04c74b9c2710deed3`  
		Last Modified: Wed, 04 Feb 2026 17:04:50 GMT  
		Size: 26.0 KB (26026 bytes)  
		MIME: application/vnd.in-toto+json
