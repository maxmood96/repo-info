## `golang:1-alpine`

```console
$ docker pull golang@sha256:47d337594bd9e667d35514b241569f95fb6d95727c24b19468813d596d5ae596
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
$ docker pull golang@sha256:53443fdc64453f971b5c82374d86945b90c053880131b13ee50704001e77f23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77982436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dd8d95a22097eb75e2c20ccf94b3957f40380944a4c8b263cc39ea5ff0d3e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009968c6529e09b95bd1a1de21301f30aa4628cbced5fe0a8fe0c6c6c592b6c5`  
		Last Modified: Thu, 16 Jan 2025 22:06:00 GMT  
		Size: 294.9 KB (294888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d5e94dedf03123c13c33c9f461a159dffbfd2152083ecf3c4c39c215e73fba`  
		Last Modified: Thu, 16 Jan 2025 22:06:01 GMT  
		Size: 74.0 MB (74045677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a648298ca3cb141d19da2ac4305e3b151f5a91715c71246b81fdb6a32c7ad9e1`  
		Last Modified: Thu, 16 Jan 2025 22:06:00 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:233da3c5abd7e947e40bddad74eeb50a6d6f09ac09148e83f5dc07dd018b5132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 KB (243047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3226a1da4af848fad40db0de45352a10a4ed59abe27770664898e4e83d388b6`

```dockerfile
```

-	Layers:
	-	`sha256:40ac0863eda6c4f7a79efc34aa099d3325aa839df512b94640717e7f7f89f8ad`  
		Last Modified: Thu, 16 Jan 2025 22:06:00 GMT  
		Size: 217.0 KB (216977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2de786256a31be30740d0aabca6be7ea4510a47e3245eee931cc4ad31e4ffb`  
		Last Modified: Thu, 16 Jan 2025 22:06:00 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:139e66d81cf53be338206d81e3872be359387d08dafb1dd7e396177e1ebeac10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75854155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8238051a100ffa225c1700f042b65182cab6aaceb3eafdd907e15123e11e6efc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f03f69a8f388ed7361ffb2b4247b3a48f246dac506cf30e7f01c792fb81bc18`  
		Last Modified: Wed, 08 Jan 2025 21:49:41 GMT  
		Size: 296.2 KB (296242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40eea1e2711989cd934fafed2bad6150c1d5f7a6e606fa1c01c32b7223ec7d8`  
		Last Modified: Thu, 16 Jan 2025 22:07:51 GMT  
		Size: 72.2 MB (72193876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12500b0ca01cb5687b419f239e2787ee0941faa12c480cca7141ceee3fb2c936`  
		Last Modified: Thu, 16 Jan 2025 22:07:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:698d3e6d1883f834383a5f143c31fb4aaa99c5f0945fae8db74e5c08327b3874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccd63752de0f1477d829fe4b4c66ea6a779824b5b449425d730f8cc15e5f17c`

```dockerfile
```

-	Layers:
	-	`sha256:a45eb4c0fdfbc1154e7b10d83831c329de001eb5aac1c0a4c87590eb91baf85c`  
		Last Modified: Thu, 16 Jan 2025 22:07:48 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:de6b9de23c83565cc3c0145c1d4bb437a6fc37b0038bde56857afc1b12817e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75586370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffafacc8c9d3baa067ddd12f521f2d6c07aa5380cfe2d0b8dfc4f575bcd2bec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d0001409a747749230c7a654e2687c0848bbc83674d48cdc49a7ace1ecdd14`  
		Last Modified: Wed, 08 Jan 2025 21:54:51 GMT  
		Size: 295.2 KB (295180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71181da0f46bebe3348744084ada18c7bb3fc1a115b2faa229669f2846f8a617`  
		Last Modified: Thu, 16 Jan 2025 22:10:17 GMT  
		Size: 72.2 MB (72193920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b06860d892ad634c5f9bd1c004b2b10e5a6ccb5187376cdbaa5f0d45218529`  
		Last Modified: Thu, 16 Jan 2025 22:11:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:61216ce6853b67248ff886b032614dcefcefa11d8f5ff473d20403832ebf725d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 KB (243212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408194b702c9776bb8202d2a98699ec976a43bc971d37e0ba0c40f0c2c62dc2b`

```dockerfile
```

-	Layers:
	-	`sha256:c905962c5c9c5d251e4df69577ac76467db310ff42cd27188d9474f278a04918`  
		Last Modified: Thu, 16 Jan 2025 22:11:38 GMT  
		Size: 217.0 KB (217009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f0d2c4445306f4e64910a6e35215d2bf87069cd015aa9e34eb13f7dad4d4ee`  
		Last Modified: Thu, 16 Jan 2025 22:11:37 GMT  
		Size: 26.2 KB (26203 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e8630f35a0930fb45171797c621b77d47315081c86ef0b9d5e6ac92fe580a620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74966660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5d4cf8479eaf7d580ff5256466047ebf8ba3a59ff1d9c60225a3fb29a9527d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1056f4fea241387de443606efbb463ff34c3d723317da5aaff9ca1d42468d46e`  
		Last Modified: Thu, 16 Jan 2025 22:07:17 GMT  
		Size: 297.9 KB (297868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d514b7aa85ba6aa1665a90e4a24f9a4312a9ae69f1e26235cf49d08b80c7b`  
		Last Modified: Thu, 16 Jan 2025 22:08:29 GMT  
		Size: 70.7 MB (70676275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f92ea2a58530aa31be3e611f075346f0aa7ba98cc5e5b792cd1dffe3e1650c0`  
		Last Modified: Thu, 16 Jan 2025 22:09:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:403f9fc4040de8d6184fc962ccc10ce2369dad173e5653e68e2e68899e13d382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 KB (243333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e727e09916bcfee4d21b0bd886d4180c1a0469b259c05ea0a34cdb1e18e7384d`

```dockerfile
```

-	Layers:
	-	`sha256:b8813d2c886c1c32b704bb76a6027deaf7471aabbc684af98d8d43003f79d62e`  
		Last Modified: Thu, 16 Jan 2025 22:09:24 GMT  
		Size: 217.1 KB (217081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74aa740858508013834edd1956a952e9b2b3a3362ff9cfaf47729f910a73406`  
		Last Modified: Thu, 16 Jan 2025 22:09:24 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:7152bd044e81d739fb4f663ab89a2ce5c1fa26308271eb291b1f0c82922a044b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75678499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558445893e752ae2b529a14827192d34b22a7164de9828cefe46ed8fca40e560`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7675ca7c73a44a25d7b100e0ba60df69f912dbbba6a02069173d2181e112e225`  
		Last Modified: Thu, 16 Jan 2025 22:06:02 GMT  
		Size: 295.6 KB (295582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec59bcc9dacbdd3d5230d9d8cc5e7e67611376d26868ebc26d35533604cfb127`  
		Last Modified: Thu, 16 Jan 2025 22:06:05 GMT  
		Size: 71.9 MB (71919633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a5dd1ac25de7dd188036e1a4100617af5cd8f3186ee32e7c126df07fd64801`  
		Last Modified: Thu, 16 Jan 2025 22:06:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:315862e1d93dbcf0f93facb7708945eaceed6ffa30c62e0105e0cd0ea17777b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 KB (242908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4690b23310630b60765af7da7e1239df5fa19ab8168af0da58ce1f952578c3`

```dockerfile
```

-	Layers:
	-	`sha256:c3711ad23848c2209e14574c77f763bce557bf32f1715f5096ce5a9e005a4034`  
		Last Modified: Thu, 16 Jan 2025 22:06:02 GMT  
		Size: 216.9 KB (216896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e880765ef18f2c4cc3d6d8717648da8c57431a41f3fb332e48187c0b90fa9a4`  
		Last Modified: Thu, 16 Jan 2025 22:06:02 GMT  
		Size: 26.0 KB (26012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:ec00815c55c3b3cdb8c994a6b9115c31146548e4809f3e7fdb7024a94ae3cd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74710189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b441b4b147ec99d9bfdd3477c15532db388ebf5b0846cbd83148cff1fc9418`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89645da608faf7c82cb1feed37110526e6ac749989dca1758dbe61e2c3fe4b1f`  
		Last Modified: Thu, 16 Jan 2025 22:08:09 GMT  
		Size: 298.3 KB (298271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37aa28c75acc922ecf6560fbabf0d9a7a340adc5cae50338cee3c28a1906cbf5`  
		Last Modified: Thu, 16 Jan 2025 22:10:08 GMT  
		Size: 70.8 MB (70838159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf268d66e8c2237ed2bcc5195a3fe1c4440f55487728aa99d913b5da1c8ccc`  
		Last Modified: Thu, 16 Jan 2025 22:10:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a4ba2561c333519539022a6e7e00fc9c545dee814675744ece203e49eaecd837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 KB (241262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a735af33699f26b87a47be17b6debd3a84d2929a1781b80cfc4e083f409511`

```dockerfile
```

-	Layers:
	-	`sha256:b66bfae913056e991e323f2960e0aba0b8ea5f42cf106cfcedd4b19f399761a2`  
		Last Modified: Thu, 16 Jan 2025 22:10:46 GMT  
		Size: 215.1 KB (215120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c1cf528fda876855e22555fd9f7353a2c0ee707599bc54a67ebf27254b5509`  
		Last Modified: Thu, 16 Jan 2025 22:10:46 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:4a6cb1d23e8a20fe0e4cd06f2152c85092805184d6cf312f34f8fc949d500b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74881244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b617813c7356f703651afff7b041bc20c4130b685ca8a4b6fe3fe9273ac1d7d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d26d7d7362ba90a5c2912b455128da725e739b7dbd70f75dc1091bfed8ea2d6`  
		Last Modified: Fri, 10 Jan 2025 16:32:59 GMT  
		Size: 295.4 KB (295361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9becc12d50f03eb54a28832963ed08e4345ac23e0b0333a0b4fcd21f803f32a`  
		Last Modified: Thu, 16 Jan 2025 22:19:50 GMT  
		Size: 71.2 MB (71235469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81053d243726ac655be2bfd4f72185da0d684ca1ccaeb57233cf4ef55461e2b`  
		Last Modified: Thu, 16 Jan 2025 22:19:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c4125a9f29f113a013b30f3a9c74d075374f871ed85d9863c4d2952d13beb95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 KB (241258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09b3a0c4fb4b9f02d7c778e03909a0e63dca2ed9588b127b32d386b3bb584b2`

```dockerfile
```

-	Layers:
	-	`sha256:ed9ad247ce877ab56e4817c7f1ecbe743e893589bf9fbaed5f23cc5e504bd045`  
		Last Modified: Thu, 16 Jan 2025 22:19:40 GMT  
		Size: 215.1 KB (215116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4f0efe93f794f7249222848646b7fcdc8c123b6197d56a49de57d62d449455`  
		Last Modified: Thu, 16 Jan 2025 22:19:40 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:63fa31b48d84bfdba7c66d44059f9cde93baec9b7034c69bcd150db424dd7893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76717869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8c0d773bd0cd68c6d28eb9b047763b4e8fd6712184c8102185eb4ec88fac7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Thu, 16 Jan 2025 21:14:07 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 16 Jan 2025 21:14:07 GMT
ENV GOPATH=/go
# Thu, 16 Jan 2025 21:14:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jan 2025 21:14:07 GMT
COPY /target/ / # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Jan 2025 21:14:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891798c8b7f45ed9fd4734da8ad75c1f6667b239c599c11f3cdab494a7a8406d`  
		Last Modified: Wed, 08 Jan 2025 22:06:35 GMT  
		Size: 296.2 KB (296160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b567a3d856120b002d262f7c532f30adaa977477b055fda3e7047c19dfbefeb`  
		Last Modified: Thu, 16 Jan 2025 22:11:06 GMT  
		Size: 73.0 MB (72954684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b192a56702bd3b84d700fd90816e66afc9c8d03959902eeddbf252c0b851dfe`  
		Last Modified: Thu, 16 Jan 2025 22:11:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:c6c861b892de6bd4e60dcf2c6604c694ce1be2f1c379c66af2355b4fc1514035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 KB (241096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e707112799db6c31a76af08d2040b57e3efe6d4ddc2c5e9b49d44624a92c62b2`

```dockerfile
```

-	Layers:
	-	`sha256:7d039e12737a84e7c400890d8e1dd09d17b01a27a5013fb2217b2cef22792d06`  
		Last Modified: Thu, 16 Jan 2025 22:11:55 GMT  
		Size: 215.0 KB (215026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8243c7bc1fb8275f3339789aa35e2b9ec8abb4ab3eb66a1a48c75bd8d79101e5`  
		Last Modified: Thu, 16 Jan 2025 22:11:55 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
