## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:b73b8ad73a47151444be659d9f829ef6867322b0015104dad2419db9c3dea753
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
$ docker pull golang@sha256:ad9b63bb1fa120bd8bf01cccd8c97a9af7e753fa674da51f52bb8c92a6949fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99131428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86ba65a3ee25fd64f8e69c0b10fd0c49369bcb653bd30f4acaec8006d719a5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:19:19 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:20:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:20:57 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:20:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:20:57 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:21:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:21:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7e1db952f3240cb9e81fbd01c3300f6b442ac06388fcf9aae5b1c0a0ff70ed`  
		Last Modified: Wed, 24 Dec 2025 05:21:20 GMT  
		Size: 291.2 KB (291157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8ab74e427643c28187f0d3b567e6fea07c0d44d52df85de53b9ccdd7a063e`  
		Last Modified: Wed, 24 Dec 2025 05:21:26 GMT  
		Size: 95.0 MB (95037660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92d2fa6f2d4542e5571b8c5d7809ac7da3d6bb660ca1c051a2b4461cb94feeb`  
		Last Modified: Wed, 24 Dec 2025 05:21:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b02eefe706d699db846e00f0c0e5b6b4a7fa2f47a142c6dda67c8018049a93ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da03bbc605330e1b7a1a237d3d8a40dffb71bacd255a52f8d92dc6d3acbb965e`

```dockerfile
```

-	Layers:
	-	`sha256:58a57284394782f9d4b2ec63a5d462a7f351b599e6a5cfdb862ba8679f5a4547`  
		Last Modified: Wed, 24 Dec 2025 06:24:35 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5968487b104d3d108bb7be36adb3b7eb4889c532b3a8eb6536ff79ee7628ca4c`  
		Last Modified: Wed, 24 Dec 2025 06:24:36 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:baf8a1d5cb1e28a861e809cd43c8bf1e32ed4480a3764af59a010112f7244cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95180062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9075368b009e6121eb2ccee28c7e220862e48f3813f3accf91e09397b50f66`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:14:28 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:17:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:17:04 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:17:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:17:04 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59367ad199c65e0e67435a40a7097a91b8f9b109bee611065a58504f64ecb16c`  
		Last Modified: Wed, 24 Dec 2025 05:17:25 GMT  
		Size: 292.3 KB (292308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cccd0041f8e1b8b3e27b5b75c781b1c5ce120805fd1042666bffd35913573ec1`  
		Last Modified: Wed, 24 Dec 2025 05:17:26 GMT  
		Size: 91.4 MB (91383515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d0f7eef4b88790ff9ed9b4904c12f2fd9620fb189892a5de827a4fa175aa6b`  
		Last Modified: Wed, 24 Dec 2025 05:17:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:141413d6901a227181148ed0332cf9b34f1a62d941ed936d6f45d30ed79b26e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804bbf43e9be4ea737dc1caa87fb6c4e8a28e2c529893b093a3391527c455e7c`

```dockerfile
```

-	Layers:
	-	`sha256:78005b20f13df6767cf38188101948b5d4a6022b186402589b3d9efe5231395d`  
		Last Modified: Wed, 24 Dec 2025 06:24:39 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:fd65541aa0faeff2cbdf8d921b357a5bf7ac399a8956dc175193c7caa18e4af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94618754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b06e4202cd7f8a675dcc3c365a16939cef33b19ee714c7362e7cebd3ece9eaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:15:02 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:17:39 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:17:39 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:17:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:17:39 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d43d467766ad095cdfae152bac0063d74667d32d96bd0f37932888ebbaff46`  
		Last Modified: Wed, 24 Dec 2025 05:18:03 GMT  
		Size: 291.2 KB (291214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916e480570823a95137488489c184e78cf3bafa0a643be0c57f52f82930a006`  
		Last Modified: Wed, 24 Dec 2025 05:18:05 GMT  
		Size: 91.1 MB (91105827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8541dbf9d2a23e9f25b54ff912e032f5977e860a39db84cf868031118ccace9`  
		Last Modified: Wed, 24 Dec 2025 05:18:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:51f7714970071856ef6a992b6c5169e95f0bd07141798b183fbd7b41c33cbd49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74dee078e5841c5f49c6fc33c0d0cdf264ac8c42a0c0cb43cc9c351b819e607`

```dockerfile
```

-	Layers:
	-	`sha256:0df8d63bafefd3432913a11711406d4842273c00fd5501fea7117bb71a0c11d1`  
		Last Modified: Wed, 24 Dec 2025 06:24:42 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f9bff60d7ec134fec75ee1445613ed9f0571d37ddfa9f2abcbbc249736805c`  
		Last Modified: Wed, 24 Dec 2025 06:24:43 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:68a050c2416bd153d8ce438bd8fafa29045e3e8329ce58fc307032aa9a76373e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94545824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17561386ccaa76ca0b172c3e69cb3cb4ca5e5017c10158ef83edb6db1f2997ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:20:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:21:44 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:21:44 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:21:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:44 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:21:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:21:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df825f17be4e1b189d4fdcf9d2a2301d9908b913a1df772e8c6e6cf716c339d8`  
		Last Modified: Wed, 24 Dec 2025 05:22:08 GMT  
		Size: 294.1 KB (294111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1a52724d12595cbdd937d1a6f8220032f161596f409cbf2928a4904bc545b`  
		Last Modified: Wed, 24 Dec 2025 05:22:14 GMT  
		Size: 90.1 MB (90113486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22052290acc2a44109f5fe750c0bd6becb6de8f2619173c1c3c66434fc7e3d60`  
		Last Modified: Wed, 24 Dec 2025 05:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:36cd198163503ecc1469534c247dafd87858eff61c04eada949ec3e6bea964b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af6c5a3e3f279646b7bdfe27e43459394d64295deaff7542343cd79cf27ce4f`

```dockerfile
```

-	Layers:
	-	`sha256:32053c3271c6257abd9605225c1dd989e4b405b64cf75044162668b2420fd491`  
		Last Modified: Wed, 24 Dec 2025 06:24:46 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3f2053ae6dead63850e02a1012bc925089dfc15f8ec6a01b45ec089c754ffc`  
		Last Modified: Wed, 24 Dec 2025 06:24:47 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:5753d90fa7f22cb2780eb0d69aa7f50a1eaf0fb1224dbd492c883c25a0a9c014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96834225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e324f1d1e16ef478c1050949cad566b3263851a0f35d0096993f17285e28db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:14:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:16:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:57 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:57 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Sun, 07 Dec 2025 14:06:47 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a355381f2c82c699747e7d556766fc23be776cae8e820586b505a10932a9a6`  
		Last Modified: Wed, 24 Dec 2025 05:17:19 GMT  
		Size: 291.6 KB (291633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fa6b6fe890c82489ba635114b540868912dc247cb535fd5b44aa5a94fb494`  
		Last Modified: Wed, 24 Dec 2025 05:17:06 GMT  
		Size: 92.9 MB (92923502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7414773445f46f3c56ea4c8eb69e5b627e278e89487c6ce484428d7a727d6262`  
		Last Modified: Wed, 24 Dec 2025 05:17:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a8366ead08085f40d854aa17ea0cd5f5fce06013788263aa8b3c9570aa3e73ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e986e2e0cd619bdc4cfbab60252272b261d9fd7f6fdd28de407c7be397c5d3d`

```dockerfile
```

-	Layers:
	-	`sha256:91eb69a45b5f43b45b6217a54931730b2d7e6e0defff4a6cdf1b96b00d8b6215`  
		Last Modified: Wed, 24 Dec 2025 06:24:50 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8805257fc6a4bea3211d7494be47166ee81f85980a4931caea8fc2f8fe518a41`  
		Last Modified: Wed, 24 Dec 2025 06:24:51 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:a22635af2c578435b14ceee19a0366b4ed27b1c23176a0cccb0526f248d60b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95682244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e206c2545c82ab88f3bb68ac85b36f602069166c95b9a61ef947e5b7297686`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:34:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:34:00 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:43:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:43:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5de3a0302474d051f06a0dba49ec72e6a84fba75a10ec5c8dcfe3ca9da396d`  
		Last Modified: Wed, 24 Dec 2025 05:35:28 GMT  
		Size: 91.7 MB (91655252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322039c2d28b054acb00d61ff9d5773b980190ce6c8fc2d1a3ce73fbaccfb8c8`  
		Last Modified: Wed, 24 Dec 2025 05:43:22 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ad8e0934653f593ca0b7a73a615d8a857ab8e2cc7358217f2f97cd0488477c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b245116e98cbfbae960d24404ba86d96e9d96ab3b11813a019d53eda0caaff1d`

```dockerfile
```

-	Layers:
	-	`sha256:c08960e1a2448584e60ffe157c8ec3c863018fe4165c3edab183a1082c058393`  
		Last Modified: Wed, 24 Dec 2025 06:24:54 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3221833fe680000178ed6eb4198e577add879a98316d50b59c5d4a21a3ba3529`  
		Last Modified: Wed, 24 Dec 2025 06:24:55 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:9a71777d41fc1cc8273b6cb91903b4af617d6d65420c8ca958cd8591f8a29736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96105559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fb2fc2e40ccf9a359514f6ee7d3ca1bed73645c19ab727cfd62c83917efac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 06:56:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:56:42 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 08:20:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 08:20:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efbeb47d67a4f0f513126184055d20de04c0261cfdbd8b06feaf3a27c3f0eb2`  
		Last Modified: Wed, 24 Dec 2025 07:04:00 GMT  
		Size: 92.3 MB (92298638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5876721898d79077d3e8fcb5cf3c03f60c56868ba8497dbdd90953ce028f00f`  
		Last Modified: Wed, 24 Dec 2025 08:21:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:a0b163f86e987c1705a629ffca853c2a693946a3d86f7475af6d9aa825e6cce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fe68706035ea355f4b876da2c1b363f44728e40da77dff1e419a048610ffdf`

```dockerfile
```

-	Layers:
	-	`sha256:d6a47a6e01e90904ac1fde43c2b1e032efc2f402036d4d5d25b2ff1e4fd4a001`  
		Last Modified: Wed, 24 Dec 2025 09:24:00 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2c92707764dec3da8ad4d26168c8f6edd00c5b178f591d141df0d37acfbf8a`  
		Last Modified: Wed, 24 Dec 2025 09:24:01 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:dfd4906f87e452bd6208c3fc44483f09587d7cb13b25f35f529835a16bd43b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98140391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42de40e08fd5a4582f85b4add246a6dc9d6c577c3611adcea696301813743d8f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Dec 2025 00:42:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 24 Dec 2025 05:16:18 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:18 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:18 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2a05f09601b30b4f54a2a9acd5043671541b70f912b9dea60733fd4213fbc8`  
		Last Modified: Wed, 17 Dec 2025 00:42:32 GMT  
		Size: 292.2 KB (292152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eae26383a5ec3ad19d41ec233e74f5aea1ebfab7013779b5b7f518483b785a`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 94.2 MB (94198838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0879c8a851efb577a1cf5a5be5ca322f313d80b84b6287136412cf402a4c74`  
		Last Modified: Wed, 24 Dec 2025 05:17:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:16aa5289444313a3ff9a45ed11ea40909041dacb1ad0da55255d4e35ce3f4d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e19009c8f7bb4a67a833fd2b0be1271a049339eb1c3e035072d71403cea495e`

```dockerfile
```

-	Layers:
	-	`sha256:e32c53011cdf6c89d986e317f52883c4ddf1de152c57f5371888e8c24b986b10`  
		Last Modified: Wed, 24 Dec 2025 06:24:58 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed7fb9b5d6dd3594d0fb7b1881c25c1a33e7e590b178dd85c5eae2cb55abada`  
		Last Modified: Wed, 24 Dec 2025 06:24:59 GMT  
		Size: 24.5 KB (24464 bytes)  
		MIME: application/vnd.in-toto+json
