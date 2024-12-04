## `golang:alpine3.20`

```console
$ docker pull golang@sha256:dbf06d8ccea279a1f28ecb700742551b3f17e007de23c1985b3a9adf868cb1f6
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

### `golang:alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:20c0c5ccf7c851ecde9f0664404213adabe2b47f34e5292bfbeaca203241836c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77962398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed2b335ca59cd7eb2c5b0f34cf36e87e4122a5e1984b4669a125579b017f5fd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef4a4ee8ca5db55a7139577107921417e5e27350f34f39667f17d271f9dbd1b`  
		Last Modified: Tue, 03 Dec 2024 22:28:59 GMT  
		Size: 290.9 KB (290888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe327b54edc2534d4a94dc17716d2b1655e6cf233f86390c0a9b854885ae545`  
		Last Modified: Tue, 03 Dec 2024 22:28:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f2b124395e0fea6d545088fdd5e155b81a1214ecd6dc1ae2540ec99fd309d9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 KB (236112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3097cb4614c13388146282366813795776b110ff645493b01379bbe01a9c35c`

```dockerfile
```

-	Layers:
	-	`sha256:278aa60445784a3ef913b0c7722c077e0aad45432c534825f1ab7156f1299c54`  
		Last Modified: Tue, 03 Dec 2024 22:28:59 GMT  
		Size: 210.0 KB (210042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40568f94b26ce51062e8c363b911b2cf25a7b760be7dbf0fa6a4fc76941f67be`  
		Last Modified: Tue, 03 Dec 2024 22:28:59 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:a498fda841d32360ddddaa6da7a7a11d8b1f2b658b6a11dc859bf36d61b9c6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75857072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbe627e05a67e9b0508262a80ae1e035af58691e5c45459bde29a0bb3441f10`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09660efa60074dd6fc7ed0eaa983537498c86f66f4ce6ec6fd9caf5018feac3`  
		Last Modified: Tue, 12 Nov 2024 06:28:18 GMT  
		Size: 291.8 KB (291778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569843b3031b27806b4332ef906025ac81fe5ab3623a61a6d2306598bfd512bf`  
		Last Modified: Tue, 03 Dec 2024 22:28:55 GMT  
		Size: 72.2 MB (72198540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7fe4b05e3f7753d356e4efa5b383d0a712d2663f8dc7c0713449b5f23c865c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:7b1009e56d0de81fe3b1ad8f769b408c46d56a61d7eb3c3778f70be7da4cd93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88716f9a9ce7bca02a69cd73c91fea498953c4b53038aa03544452410ef59cd`

```dockerfile
```

-	Layers:
	-	`sha256:4056994e586307221d4e998e7106f14e0b8610d59649d07c6c14dab40d621f9c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 26.0 KB (25989 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:111fa154ef01b6c19cf9356d59baf18a9c2ea9672df7a412acd1a6fae86bcfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75570689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca044b4ceed000542715c5ae895d2102f31e20c2f1316edcd1d89238b7cef6a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10b69bd94b71748b3b994e140d39db4c4684df12500052eb3fcfed9e34082f6`  
		Last Modified: Tue, 12 Nov 2024 15:29:21 GMT  
		Size: 291.0 KB (290958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e990400f8c0342109351b2ea2dff891387190e755f29d02b0f474578fc3d222`  
		Last Modified: Thu, 07 Nov 2024 02:59:45 GMT  
		Size: 72.2 MB (72184086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380a81bcc5ad698a1f0d6c59d1dff6e7302730857f778a0a44021f5190c2e6ce`  
		Last Modified: Tue, 12 Nov 2024 17:06:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e5be131b9f2434c31919a278f1e03c25007057062ec9708ac3d748d8bc352c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 KB (236278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9e63fb78f689f8eec615c871b007acafa3b6353b1f6bd8109b4392e6dbfaa8`

```dockerfile
```

-	Layers:
	-	`sha256:74d16b59916c5a4c81454041b8ddba08819519b17cc8ef99287d45157ad2002a`  
		Last Modified: Tue, 12 Nov 2024 17:06:55 GMT  
		Size: 210.1 KB (210074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da73b62f81c9c2851e1b6157ea7fca58a66c6c2fb706732aaf740842d7b182f`  
		Last Modified: Tue, 12 Nov 2024 17:06:55 GMT  
		Size: 26.2 KB (26204 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4152418b1c7ced56e47197c3aaf822a218d3f5be12de867e912c3f2fc8e5a0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75050354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9226d159e1ab2a8e974475023cc0453c9961651eca396f46bb864b53b9d07fef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d571ba9261b2ec97b6a5261bc2b5f8dd6b1cad7aa5ab454e38fdd9ab1cf45335`  
		Last Modified: Tue, 12 Nov 2024 10:27:52 GMT  
		Size: 293.5 KB (293522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323003b0d8ad8001283c9881b96c87e9fa38fb378aa4de93c4defd3899f30d2a`  
		Last Modified: Thu, 07 Nov 2024 02:59:17 GMT  
		Size: 70.7 MB (70668948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be085c496fa3648c76be85bb025157a095ddcbfd306f9a423cce78e0698dd3e4`  
		Last Modified: Tue, 12 Nov 2024 12:00:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:66256dde58934d1040d6b880bbae448735904e9ec659e1c74062c2184fa2d853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.4 KB (236398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7839f62d51202236793ad8863d56506d4c1fdd8783a9bd5c596e8332f1196b`

```dockerfile
```

-	Layers:
	-	`sha256:e614e0ec079bd2f8114d51f9b375805a34bfc8f8f86813041e65ed24701f94a8`  
		Last Modified: Tue, 12 Nov 2024 12:00:06 GMT  
		Size: 210.1 KB (210146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc31b6b2b413b80c5ace6bd2c03ff1b889cc56c2dde57b4e09e8c977eae7026`  
		Last Modified: Tue, 12 Nov 2024 12:00:06 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:723f332afe88412434d45646c2b87a5ee3cdc27a2385a5875423f2bff7ffe3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75673870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e69d5179d39e92af96d845bf137b6f12c036016f928c2e53b039e828bba112c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257726af4a6173859e4021d329d77e8e60e5bd1b76d826b2aff969b68b7633a3`  
		Last Modified: Tue, 03 Dec 2024 22:28:51 GMT  
		Size: 291.4 KB (291372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ee978a239d9a54a2ed89c291f3c5c0ee5f67c1dc8c9ff24b239116398d826`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 71.9 MB (71913121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3fd4950283ea8297754af1d9667c4f6f6f7da11ebe9771b0fac797a7034f08`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:a78f62d8bf313922733dfe723033fdb8228053e404609bc33cdcbf325d99f272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 KB (235975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c8d64eec0074b6367d25b29232d8f6fd17f5c5268cb8ab9daa0006f441cb92`

```dockerfile
```

-	Layers:
	-	`sha256:91466505c35c924c1447638d3f83156d954121ad4ef96d09913c9da2975aeefe`  
		Last Modified: Tue, 03 Dec 2024 22:28:51 GMT  
		Size: 210.0 KB (209961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486013dead1a65c5e1753e93cf16097403fe35d9476a3c83ac749ec7fa011a27`  
		Last Modified: Tue, 03 Dec 2024 22:28:51 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:ab238ac50b1cafe8ed007a3f7bc05b93f232052044d2f681996efcf91443f17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74695127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436229f5810ebb8a4dbd94c062c3cf4ccc92ade0fea2f0eb481975a5485e9ac6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 07 Nov 2024 00:26:15 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 Nov 2024 00:26:15 GMT
ENV GOPATH=/go
# Thu, 07 Nov 2024 00:26:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Nov 2024 00:26:15 GMT
COPY /target/ / # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 Nov 2024 00:26:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3873bb4db6d014ff18a3c4d7f5d4ef80493c562c62c0640979ceafbca23930d`  
		Last Modified: Tue, 12 Nov 2024 08:05:08 GMT  
		Size: 294.0 KB (294032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d45dcd888e3183671630e662953341e3111584ee0e6ca4f0d40e50580ea2de`  
		Last Modified: Thu, 07 Nov 2024 03:00:09 GMT  
		Size: 70.8 MB (70828478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7c8e4b36ae1306e411f533d94206075953e9d651e034156cba75c35a30a3ed`  
		Last Modified: Tue, 12 Nov 2024 08:59:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:f2f68f077a46c94c9760a9f40a77e01f11ba911a46cf37e4179b030232d4bae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 KB (234324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717ba9e77bfdacb98a5afb2e2cd91dc0e17c884d8e7d2621d6bdaf23755ef971`

```dockerfile
```

-	Layers:
	-	`sha256:0256af33933831aa8d78786da80fcaba43f49f7df5731f963f88a760f574b185`  
		Last Modified: Tue, 12 Nov 2024 08:59:05 GMT  
		Size: 208.2 KB (208182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98f2401dee4c26a616b6e6a019a7b3668706fe383e02253477c698b5dbf28e69`  
		Last Modified: Tue, 12 Nov 2024 08:59:05 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:00d024e45ae31dd77d5f4148070c53cc37b1bb877ce2fdf29dc52c7d9e7e6b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74904231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059ce06ae8915b70ba6467f7d07462ff6f81aa12b22402eb9d4addd7e2dc4f12`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9da01c4ee7a2864330da14801bdf35f981730b5e2ffea0588c9ac48734e26b`  
		Last Modified: Wed, 13 Nov 2024 01:22:36 GMT  
		Size: 291.7 KB (291671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ea5001679e325e9959f4e49e737d7b5d8a17fc575fd3810ab4495a88e73ee`  
		Last Modified: Tue, 03 Dec 2024 22:32:57 GMT  
		Size: 71.2 MB (71240920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933ab90a88816114ae116bd757c876eb44413901c2699659dffc92325a8501bb`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:42fba6156278a29257c89b9a42880ef578cd682518520a7fa1ef50f9df478d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 KB (234320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7559831148853817ab7357c87f47dddc684a5546b75c04ae350e3560140b4ec0`

```dockerfile
```

-	Layers:
	-	`sha256:b26696367c1171e42169b80d74c304c679fcf7e8a5edbe86bcdc6977792da3ef`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 208.2 KB (208178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a85cfb2a28455bb00457fbb33e951356c34d3311703e9b8ea06ea3d02b5d0c51`  
		Last Modified: Tue, 03 Dec 2024 22:32:46 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:8c8e4256e2fe09dcdce32bcfcc1fd32aefed0fdb1a0cbc23308fe628ef4632f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76723476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba1931d9138d040d554c07ab595952705f97e6f8a4369a77b612ecd52c4812`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 19:01:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd7484226737ceedacb2f6eba2ffed52277681762f797e80ac3aab9dcd04a0d`  
		Last Modified: Tue, 03 Dec 2024 22:41:06 GMT  
		Size: 291.9 KB (291897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eab153b4468df7f657167533fa78804e60b235edee0f04ec5dcc52a35b056da`  
		Last Modified: Tue, 03 Dec 2024 22:40:01 GMT  
		Size: 73.0 MB (72969813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd6797f065d69e1c2b1ae8e8c7df91d6c7b2b3d9173a471b1969a6d413cb13d`  
		Last Modified: Tue, 03 Dec 2024 22:41:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:8bee4a894effaf97d463d50467d34adeef2ab69eda2dcc5512df6ebcb9c968a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 KB (234158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927e87c0c45592d5d90368c6b239824123c3b9cb9fa05fd888b6646ceaf6e737`

```dockerfile
```

-	Layers:
	-	`sha256:5169d7feea0ae53b8d213f8c2b99f2ab059d26eea113d92720cb51569c86cf6f`  
		Last Modified: Tue, 03 Dec 2024 22:41:06 GMT  
		Size: 208.1 KB (208088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1958b171a3541765f721fded8adf8203b8b2afda691a1263e785ab46ac1509c8`  
		Last Modified: Tue, 03 Dec 2024 22:41:06 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
