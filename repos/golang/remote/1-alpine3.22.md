## `golang:1-alpine3.22`

```console
$ docker pull golang@sha256:be93003ee861b3b91b6ebcb22678524947e0cd786c2df3f32af520006b1e54f5
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

### `golang:1-alpine3.22` - linux; amd64

```console
$ docker pull golang@sha256:323541ca84541015a3dbb9cfa73836865493ce77bfc48dd8d2708661236aefad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.4 MB (71382883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7daffb934979006c0e62187c34791a71c7a264fed866ee5a023205458629030d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:37:07 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:37:07 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:37:07 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:37:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:37:07 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:37:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:37:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713d2d8a8d8daea90208f0db2272f7c5b7b1ed86d1830e274eb0b77523ab311d`  
		Last Modified: Thu, 07 May 2026 17:37:59 GMT  
		Size: 289.5 KB (289454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70bdedd442d430ea119cf8db8c0031b4eedeb5bde886892773876ded7629e8`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 67.3 MB (67285082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b484117e1e151ea52ceb93fb9da6760698c9d7e3c6e7552124c09eaf5d9112c`  
		Last Modified: Thu, 07 May 2026 17:37:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:dc2439baa0a3d5eb227aa424be4a5b67ff807f83176410471b496c125e1d8f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555493430379262c91ae3215d76a3a1c325ccfda1ce243a955cd68ab9fd44d75`

```dockerfile
```

-	Layers:
	-	`sha256:7aa2bacf2a9a375d2a0e1a36d727d065d494345a811054ba2ff9178f09f9e1b2`  
		Last Modified: Thu, 07 May 2026 17:37:59 GMT  
		Size: 195.1 KB (195127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239976f6ce79f977e639b4af5d3f57744d9ef5bf1e4d32f959b3633b25f364eb`  
		Last Modified: Thu, 07 May 2026 17:37:59 GMT  
		Size: 24.8 KB (24807 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:e2b310d5104549904fb5a00c2f881741c34dd426157735254d09992d51611c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69584396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60dced476a9923e71f451022ae3839007e90a05d3ef83c3256de1f7c529d6e9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:56:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:57:01 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:57:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:57:01 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:57:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:57:01 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:57:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:57:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5453098388140b084d878a9ed65fec5ae606b6d0ccbbb7052b79bfbd3c900437`  
		Last Modified: Thu, 07 May 2026 17:57:16 GMT  
		Size: 290.3 KB (290335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323b6bdac241fc54c2e0e06ca7f4045ec740c882bb235caa36f634f6857573cd`  
		Last Modified: Thu, 07 May 2026 17:57:09 GMT  
		Size: 65.8 MB (65786523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976237db066761005df1749e4f61dcd44bbab82c2b1aac01c02a895d4fc07a9e`  
		Last Modified: Thu, 07 May 2026 17:57:15 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9383990ff0dba6c4ba65ad39990fc8f31f20fb67155df6461bf909db6dd52bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d990276e1ffcf50877a64a1d7fe187fe8dacbabdadbdccd98c56da59516018ce`

```dockerfile
```

-	Layers:
	-	`sha256:b99c43269fbf11f9e90a0f53bc030f308f6d0f95c3f6c199096408b5a375c1ec`  
		Last Modified: Thu, 07 May 2026 17:57:15 GMT  
		Size: 24.7 KB (24697 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:4916fdd22054b075f3c3adb5d890d075ab7d2222448fbe0591c97def918d131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69301972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273f6d416bb6c437bda9e7a69d9c92284f789ec2ab71387356bbc0d967b61b11`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 18:01:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:01:40 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:01:40 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:01:40 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:01:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:01:40 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:01:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:01:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03abaffae2fb2cc44dcbe33e3453df0006ec0ec16eb26aa08dbd8efa0c1c87f`  
		Last Modified: Thu, 07 May 2026 18:01:58 GMT  
		Size: 289.5 KB (289508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e7137c96fc07d2fc9e87f7cec43a327dd6c1385057f6c469907ef731cca2c`  
		Last Modified: Thu, 07 May 2026 18:01:49 GMT  
		Size: 65.8 MB (65786476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be70cef542c035bb53047bd5b5aad676346765a2fb2430039c03a8126df6760`  
		Last Modified: Thu, 07 May 2026 18:01:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:9c0346c0108f8c68fd3486b5ec782e4dc18550315d1c95e7249300beab2ee26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f4798b61812e0c8953a129fb0434f24337d61efa465d8d0af3522ad08c9751`

```dockerfile
```

-	Layers:
	-	`sha256:053dd38160ec6311331d2e27541bef3dadbd7872dcf546e765a35d30b600388d`  
		Last Modified: Thu, 07 May 2026 18:01:58 GMT  
		Size: 195.1 KB (195147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9f45aef30aab3b28a6565a2cf14ccdf24f17ac315a344d09991e75b354ba59`  
		Last Modified: Thu, 07 May 2026 18:01:58 GMT  
		Size: 24.9 KB (24913 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9ee078b9dcc56c65b8ad6a34058d2e6d2e676fcca6544b6cdc5a8f6edb844569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68601732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66690f303ee3c914208c3a299e0fdb764834cf1d228deeb31ba5a727c20755c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:43:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:42:14 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:42:14 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:42:14 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:42:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:42:14 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:43:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:43:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d96c866386f0879f551e8f74fae1deab282b71fbd8b1ac40b54877695830b5e`  
		Last Modified: Thu, 07 May 2026 17:43:16 GMT  
		Size: 291.9 KB (291896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fa76ba696f7dc4b9e2330d4ae7c03a0f4b2c055caa94b353f7f600a6dab0c6`  
		Last Modified: Thu, 07 May 2026 17:42:45 GMT  
		Size: 64.2 MB (64167785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39517a2b2e7da232f6faece8207d26a6e5152663c4bbf6c1b449b48e360917e`  
		Last Modified: Thu, 07 May 2026 17:43:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6f002d5dfc60e384b94d628c0de1f0b4ca63b7bd7f2696a345cc61100b30ddbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6b15e458783c43951ce7e76d401e4c1ae4ff7eef25bca868c58e9493367b69`

```dockerfile
```

-	Layers:
	-	`sha256:f70600d9c673448993a88a989a622bce44c53d68e228cf6cd2ce83ccc2a93688`  
		Last Modified: Thu, 07 May 2026 17:43:16 GMT  
		Size: 195.2 KB (195183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ceb6f434455e3651588ad62be766443b8bcc84e6ef7f7020d1eb4048441771f`  
		Last Modified: Thu, 07 May 2026 17:43:16 GMT  
		Size: 24.9 KB (24940 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:5f902bb12753bcebfd4d9e1d7596a118d19389ba18656441e42e3ebc60bdaa9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69513965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5b039e3bd7906d158b23bf4fae62ce1d90e06a16d3ab396fbf3ee339de6ed4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:52 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:38:01 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:38:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:38:01 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:38:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:38:01 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:38:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:38:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a28410f3412c5e4a869d4bd364f51fd2389cd1c9704906a4f7073d78e3f8631`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 289.9 KB (289938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40fc8fcc10ee56c441c06327bcf95af166f71835205a4f4eff05758add1ec7`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 65.6 MB (65599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd6f9caa6fb71d5d178c5c75e5b9a3e8ff161369ced132c8c2fcb935a327c06`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ffb9ffd97d3c0369850b170005398d51b640ca04afa2050f6ab1cd2ae1b229b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 KB (219857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df23d123ca4bc52d3ac32bf40dcc1444bfdb3703d726a59fdeb4cf801d857c63`

```dockerfile
```

-	Layers:
	-	`sha256:c0a8b1e61e60d8b5cabadfe8095a5dd1b507ddb32f3d968b7235f811db9c947b`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 195.1 KB (195086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f61c19b8f4bae93a665776cba65f40f02f88953f173c3bf07bb5fd4550d12df`  
		Last Modified: Thu, 07 May 2026 17:38:17 GMT  
		Size: 24.8 KB (24771 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:16f88d0e4a66fc8b83969e8e233729bdd4f0ffde915e334fc39254be08874864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68871944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0210e7d082e687f38993a50692d10cb7f111f5ec61415edcbb32fbe475dfdcd1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:17:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:19:35 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:19:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:19:35 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:19:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:19:35 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:20:57 GMT
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
	-	`sha256:677743e4af652dd79f8723ff89a284363d59474b87d72b559faf60d691a51c58`  
		Last Modified: Thu, 07 May 2026 18:20:28 GMT  
		Size: 64.8 MB (64842692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3b2c3d38d2a7afa179c184cf444fb7778460f4dd05c0617028b83f39d0e093`  
		Last Modified: Thu, 07 May 2026 18:21:10 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ccd0498828e7511bd37727eeacf2d5f0ad6dba584f4f49418f3b474a210560ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 KB (217908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ced4a444ceb091bcc46e4fa05d36cee8e390448e023698b38cd08b3dce9d1f`

```dockerfile
```

-	Layers:
	-	`sha256:64b142d472bdfe4679aff9762cb76cf7ae63eb4c5bc0f7023b74c843ff0e5724`  
		Last Modified: Thu, 07 May 2026 18:21:10 GMT  
		Size: 193.2 KB (193226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd9d918c1e24d975878651b0bea183a6d7522f731c81a54e67d3f88a3aa124ce`  
		Last Modified: Thu, 07 May 2026 18:21:10 GMT  
		Size: 24.7 KB (24682 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:64dde243b6aa428d5162389a3fb2914917be89530d05aa48fac412885410053e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68960319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33845653a50ab21a985743be161dcc00f77d900612a5fa10a993115fecf8d1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Tue, 28 Apr 2026 01:45:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:25:59 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:25:59 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:25:59 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:25:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:25:59 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:37:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:37:21 GMT
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
	-	`sha256:4576730cc1188381475a15201ad7de7153b28247376e0d104bbac61494efc78b`  
		Last Modified: Thu, 07 May 2026 18:32:41 GMT  
		Size: 65.1 MB (65149474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64d7f02e16e0320bdb8e0b4498746cbc503a74b767a5dfb95d93b8b5b8902b9`  
		Last Modified: Thu, 07 May 2026 18:38:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:c59f874cb9fccbce6d077c44c35234397fab2e934a64a1b9181055f00f861b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 KB (218076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d9004a44ccd5ab0510fb308ee35f4bebb96cbab58f6909e34f30eb9fa7df1a`

```dockerfile
```

-	Layers:
	-	`sha256:4fba77ee9855f097f706455c36cfa7b12fb382d27dc0f28e2293b1c2e7b041a3`  
		Last Modified: Thu, 07 May 2026 18:38:27 GMT  
		Size: 193.2 KB (193222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0211df2ad1d521bf7b8025c99b93fe31d28ed713a7ff98fff472c48374a967`  
		Last Modified: Thu, 07 May 2026 18:38:27 GMT  
		Size: 24.9 KB (24854 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:739410bf0bbda3d8920c44e7346e70e54d1c15ba1a419b663aefc20c7230a93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70460625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0807c8da157f06a48750d2f63dbe17f64f68c572621ff1abb1c9765b07b4ef`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 00:01:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:34:27 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:34:27 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:34:27 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:34:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:34:27 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:34:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:34:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0b12310626fa8235af46cbc071f95db3829e79b0bc5117a7395ef8ff53bb2`  
		Last Modified: Wed, 06 May 2026 00:05:31 GMT  
		Size: 290.5 KB (290468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585ea404f5b1266beca471637498b2c7b5b5d49eff5d438b1d1e375a59498340`  
		Last Modified: Thu, 07 May 2026 18:35:38 GMT  
		Size: 66.5 MB (66516126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ef467323f8a96494e73213acae2b112ffb5f664ec15798c0eef5052e605948`  
		Last Modified: Thu, 07 May 2026 18:35:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:950a6769f198f2fdd310c19e737aeae6522ee058296b4a9c12e16f02aafd50f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 KB (217809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de1d814dac8b5d3a169bcb40d721560e6b868ed93c31d748a67dc652a199d7`

```dockerfile
```

-	Layers:
	-	`sha256:42647d282476310dc26c5a7a2154bc8e60a81d66a5efb9468aaeef82f4e952b6`  
		Last Modified: Thu, 07 May 2026 18:35:43 GMT  
		Size: 193.2 KB (193176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdaa026056f452ed42a7e76d459cd850de32e80557d22ad74e90b50eb2aec6a9`  
		Last Modified: Thu, 07 May 2026 18:35:43 GMT  
		Size: 24.6 KB (24633 bytes)  
		MIME: application/vnd.in-toto+json
