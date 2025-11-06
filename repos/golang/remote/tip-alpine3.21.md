## `golang:tip-alpine3.21`

```console
$ docker pull golang@sha256:431c7b90c97a048c2f6cc7df8885d4c04d7f21e1b158d5c627844a648f890839
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

### `golang:tip-alpine3.21` - linux; amd64

```console
$ docker pull golang@sha256:d4917afcacad46ffb1aa9bf0552c39aab13c17837588a7a26ae5db00b0e209da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95560512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822275b91d8333ff5cc3ff19e61df50c34edb9c5e9712418b116f740fd72e115`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:11:10 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:12:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:53 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:53 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:12:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:12:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870dfe8324d4814dd179661762c528876b758acd06d0b3663db093a21b282a21`  
		Last Modified: Wed, 05 Nov 2025 21:13:15 GMT  
		Size: 291.1 KB (291117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63342fc87a926c87fc75056ae9b3c0cfc322e728e6ecfbd21d12f9237f02ae65`  
		Last Modified: Wed, 05 Nov 2025 21:13:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:4833e526f5cec2672e8cb7dfb0aa7661c6c6a6cabd04aa6547156e13db12b4fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 KB (218670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f58ed65326699bcce8f4b5d2628ca805a60651244e542cf4e5a1a10c450c7e`

```dockerfile
```

-	Layers:
	-	`sha256:dfff189a4a456a35c493e38b12f9ed05e9f1a01407edf80c0217e66a4162d047`  
		Last Modified: Thu, 06 Nov 2025 00:25:05 GMT  
		Size: 194.2 KB (194205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c01bd46b3acccc1d23e16665524eba7dba2603b9fb8ad9ad2d8d71555abaf12`  
		Last Modified: Thu, 06 Nov 2025 00:25:06 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v6

```console
$ docker pull golang@sha256:42e86718a9d0941ff25418c1329973ff664cd45d4aec2e04aa523c91ac19c107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91722459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c68e08a2a505ffd691172beb0eddda4dbdc50633e25851d5586a20cb120c02`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:12:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:15:23 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:15:23 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:15:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:15:23 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:15:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:15:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c920b66e2a0848078d5e0ebd26aad54c16624585b7a5725b30e7d57ab0c80a01`  
		Last Modified: Wed, 05 Nov 2025 21:15:46 GMT  
		Size: 292.2 KB (292241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f518140b1232c759e1bbff002fa828b3b3a5b3d09a55146300b06356a080e134`  
		Last Modified: Mon, 03 Nov 2025 18:08:08 GMT  
		Size: 88.1 MB (88064592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b23aff128faef36d77e6b2c5a3686ab9517ece11dfddad526e494c0ae3dd719`  
		Last Modified: Wed, 05 Nov 2025 21:15:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:b610c3a712d0a76bf772f2aab82f5b2f8049bf9cde18a664dc72183cc5cc58a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1077231d58039350bba8bb44e574e66ad70822f627895c43c90258feb301b32d`

```dockerfile
```

-	Layers:
	-	`sha256:6bee7880ddab8c1c8ec8a15dc5667037f6f7f19581a3f7f3ddf9ea58fd60a11c`  
		Last Modified: Thu, 06 Nov 2025 00:25:42 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm variant v7

```console
$ docker pull golang@sha256:5a4bf94d2fd5f4d14ae3f2ce7270052b8fc25c1dc762fe5e78c1556aead7b292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91196609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a315c434f8560c7272849b76268576358fe33874aaba5ea36886dba9162bc9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:12:24 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:11:47 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:11:47 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:11:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:11:47 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:14:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:14:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7513fbbebd2d0628fdc01cecbaa7ede76d631e9f8a7df1ed133d3e6890cfa`  
		Last Modified: Wed, 05 Nov 2025 21:15:02 GMT  
		Size: 291.2 KB (291161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c215e74785983f7aa0450fb45b6db1f564380fa34dcf9d9745491d63d41a3d05`  
		Last Modified: Wed, 05 Nov 2025 21:15:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:92fc1a4e33de335e217490a7cece154682daa8e782cefb228922448107306c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc745a26a91af30682baad1902fbdcb60528709b8940c879ad38f242629e54eb`

```dockerfile
```

-	Layers:
	-	`sha256:cabbb14f0c7be9bfb9bfae384aff27d9a970f7ba7d0ee7e40681c5780e3315c7`  
		Last Modified: Thu, 06 Nov 2025 00:25:45 GMT  
		Size: 194.2 KB (194209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9166a532904c30f6020828b0f2779e8011d7d170c7cfb4492e6000d70de422e5`  
		Last Modified: Thu, 06 Nov 2025 00:25:46 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:85055236992bf7f7e9afb11d5bd47f0601a58447c6315f61eddfc4aeffbd354d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91165127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837bf38774eb6352f37ff3fd7c6beec61d3ff96a10545b6c71b6ca28dcd6fc59`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:11:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:12:59 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:59 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:59 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:13:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:13:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0137505af22a73be241a67a159f18c66f2423dd9624aebe548a4f5164000cca`  
		Last Modified: Wed, 05 Nov 2025 21:13:22 GMT  
		Size: 294.0 KB (294045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7650548a4c02bd43552c205b0842e655bb371fc64b8ca906823098dd03634181`  
		Last Modified: Wed, 05 Nov 2025 21:13:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:bdc087f9cb10f52c67b0bdb8f5afde394cd0ce7d1f6c17acdd553eccc8ff2e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 KB (218838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5ea160b960f7cdeb3aad33f723790d46704c49804dcca95fc67ffa776fd8d4`

```dockerfile
```

-	Layers:
	-	`sha256:56fc56cfc2cd0154954560f99d24451bf99faa68b39dbf53289b479be9082efc`  
		Last Modified: Thu, 06 Nov 2025 00:25:49 GMT  
		Size: 194.2 KB (194237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7129786f2364fa8d5e11b9280d32624df3eec7f66e05579de38b6fa26a060113`  
		Last Modified: Thu, 06 Nov 2025 00:25:50 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; 386

```console
$ docker pull golang@sha256:794a6da8bdc0eac949dd27d3c61e392b29798ccca37ffd8de37b2802395448da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93369492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2883cf1818c52ba0d9991b5121ee7320dafdb4df3997edf5b7bdb44140417f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 21:12:52 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 05 Nov 2025 21:12:13 GMT
ENV GOTOOLCHAIN=local
# Wed, 05 Nov 2025 21:12:13 GMT
ENV GOPATH=/go
# Wed, 05 Nov 2025 21:12:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 21:12:13 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 21:14:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 21:14:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4ae92ddc97eb010475e7d182b18b5c01263811c8a796b140d87364cf7e675a`  
		Last Modified: Wed, 05 Nov 2025 21:14:57 GMT  
		Size: 291.6 KB (291603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b6998e520e373cc12f021af852c3747d40780df05b64c64c1e2c964b60ecde`  
		Last Modified: Wed, 05 Nov 2025 21:14:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:8d00c0a4069a1489ff76a624733758248ee258d1147f7e106b8496962a3b6c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.6 KB (218606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4681b0286559a0d558a628cc206bc9e442f3dbcc8003a898611a349bfcf0674f`

```dockerfile
```

-	Layers:
	-	`sha256:361b806b5305eef361100825c54bbc279221493148d296a6b12d98002a39bda5`  
		Last Modified: Thu, 06 Nov 2025 00:25:53 GMT  
		Size: 194.2 KB (194174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781fcfc7b9fab2a8788841f11b77abbf4e958e9996c27f7fcd66e1c1c06329e8`  
		Last Modified: Thu, 06 Nov 2025 00:25:54 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; ppc64le

```console
$ docker pull golang@sha256:2c3136f0334c7ef416456baafbc289a8fcea2c6448e9bc83b405d296a3851d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92160626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f650ea034977ea9f4c7c74e3c6851db7246c8fba3765b89f0ddaf773e426f8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:21:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:21:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:21:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157fb47bb8a37b39db37d445bdc0f41d6332fc70e6aca92f0fee08bb53d187e`  
		Last Modified: Mon, 03 Nov 2025 18:22:12 GMT  
		Size: 294.5 KB (294530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c5a88f48ef60e8ab017a20aa0069340d5651c61a8b33dcb43628642434d0b4`  
		Last Modified: Mon, 03 Nov 2025 18:22:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:2e31f3ccf9327ef2d4e81b2d7bdfc68e881c0c76bf5f775034d972b2d2196a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f296e10e1e52010a530bba645d3c3adc580c7447c33d365f3b364cd84169f1fb`

```dockerfile
```

-	Layers:
	-	`sha256:2bead1c8596104a1f1100bfdfb38b754fe4074e7ee872c4cc71d7c9f2937ae55`  
		Last Modified: Thu, 06 Nov 2025 00:25:58 GMT  
		Size: 192.3 KB (192292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b721adbf6130801cdb75e85a0833752d4dd2ddd30d3aabdd88d3fa226dc53d`  
		Last Modified: Thu, 06 Nov 2025 00:25:59 GMT  
		Size: 24.5 KB (24510 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; riscv64

```console
$ docker pull golang@sha256:8e49ec14ceac580fca256fe14be7ef2bece99abdd6823ce73c1de7aa7cdc9928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92439040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250bd55d03a5cd53c6223de415fb30e4a01f181645065b6d895eb4f208a889d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 10 Oct 2025 20:46:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 19:28:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 19:28:57 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 20:46:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 20:46:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Wed, 08 Oct 2025 21:19:05 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611661040751365eafd7f1dfe7a29755674f06b893fdaa0640152a38b160d0dc`  
		Last Modified: Fri, 10 Oct 2025 21:10:14 GMT  
		Size: 291.5 KB (291463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568766c8d70cce8f34aaf3713ad1c1267acad6ccddf02bbbe3d428a4c87f11f0`  
		Last Modified: Mon, 03 Nov 2025 19:36:15 GMT  
		Size: 88.8 MB (88796418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6213908a2ce7c79893b53fc011ff630a7b872402b8c103fa1452f1695d90c41`  
		Last Modified: Mon, 03 Nov 2025 20:48:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:0b72a5acf16f701073950b4b9a79dc3686a27ababbe60686566c370e0eb74aa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:340587b476d39501562fc90835d4aae8336953e6b261b850d337e248502ee23a`

```dockerfile
```

-	Layers:
	-	`sha256:8ba0ec5753bdeb715229bcb4ebe5861730cc84c8511580463b5869326a27ffd5`  
		Last Modified: Mon, 03 Nov 2025 21:24:43 GMT  
		Size: 192.3 KB (192288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15543194b052049140705869e646b26257d20f5896b3fce1af29a0c8ae46ff0`  
		Last Modified: Mon, 03 Nov 2025 21:24:44 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.21` - linux; s390x

```console
$ docker pull golang@sha256:7e25b48fc61ba7ecb16b69fa59c18a44af571c814276e2281c63b9d55d026708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93595079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f65b96e94e3b6d51f2651e152c82935ddaaf017eb51c045313465660960fcbe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 03 Nov 2025 18:17:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:17:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:17:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa10ab6a939fc7b57442bfd1592957fc4568b2b76c4a2680a686827d9c63676e`  
		Last Modified: Mon, 03 Nov 2025 18:17:47 GMT  
		Size: 292.1 KB (292097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba52f9939f556d69c32e01283b5aeb3dfc2c3230561386c3897f7f6c0ab7629`  
		Last Modified: Mon, 03 Nov 2025 18:17:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.21` - unknown; unknown

```console
$ docker pull golang@sha256:a47d85c66e659c9957a4160b87e611de95f1bcb0fe75814ea1255609a1e5972d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6ed3e6d1057e8a47f3e3d18d8604cb47db8e569509570ecb06420a059c03f4`

```dockerfile
```

-	Layers:
	-	`sha256:768f9b5868074dad78513fad2832a2591762217b3ca11616784dbe09a6ff9e94`  
		Last Modified: Thu, 06 Nov 2025 00:26:05 GMT  
		Size: 192.3 KB (192254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3efc0f5593e7cd366e21c996dbf33487454c3c9d5413bf6146c17dcb58d8db`  
		Last Modified: Thu, 06 Nov 2025 00:26:06 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
