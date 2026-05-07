## `golang:1-alpine3.22`

```console
$ docker pull golang@sha256:d68a076a182ee06040ff0150214bd654af692cd93fc3d64fb73a28821c4fe00f
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
$ docker pull golang@sha256:5d317ad75e0a9a5b0c6029d555e721cd5bc221685dc5df03a92991cadc224a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69548897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2254b321402a6879eb4fb36fa6965b24611575eea6be9eaaf5ce28d5c5a636bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 17 Apr 2026 00:28:31 GMT
ENV GOLANG_VERSION=1.26.2
# Fri, 17 Apr 2026 00:28:31 GMT
ENV GOTOOLCHAIN=local
# Fri, 17 Apr 2026 00:28:31 GMT
ENV GOPATH=/go
# Fri, 17 Apr 2026 00:28:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:28:31 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:28:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:28:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb73082823697f16e5bf1efbdcb42da033e6d29911be4568035c38c603dfce53`  
		Last Modified: Fri, 17 Apr 2026 00:28:44 GMT  
		Size: 290.3 KB (290334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e327e2b14e32d059b1daa22f82c1fb7fa98060bc20d47dd6686da42229cba8b`  
		Last Modified: Tue, 07 Apr 2026 21:13:32 GMT  
		Size: 65.8 MB (65751024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61855757aa4412305001c6bf7dec44ea31d21c155011ce1b4712a4866d3a4e5`  
		Last Modified: Fri, 17 Apr 2026 00:28:44 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3b1bac524a841c20dfc06fee004cc36c3bf5271923fa8c384b2aa5e35b0f74fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935f02714aaab10ba36970bd096b9d51b4bf9d6de44b25579569a499abfda7d4`

```dockerfile
```

-	Layers:
	-	`sha256:2cc58ada87498c190c8505ca0479ce8cde971db619383b01c1c6afa0b1184b1a`  
		Last Modified: Fri, 17 Apr 2026 00:28:45 GMT  
		Size: 24.7 KB (24698 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:c34d76f7ce9f6c6813f926e89cbca56a66d7474daf9c1a64f7ed062ebb01377b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69266474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235291fd2c7bd13acd994daff283dfdbbc6ef4c3792237d47b3d7561c60ad688`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 17 Apr 2026 00:28:58 GMT
ENV GOLANG_VERSION=1.26.2
# Fri, 17 Apr 2026 00:28:58 GMT
ENV GOTOOLCHAIN=local
# Fri, 17 Apr 2026 00:28:58 GMT
ENV GOPATH=/go
# Fri, 17 Apr 2026 00:28:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:28:58 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:29:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:29:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389aa30d40d2cbe01ad2b410e91e2b2e19f63b148025e6b7f637119ec3a1dc15`  
		Last Modified: Fri, 17 Apr 2026 00:29:14 GMT  
		Size: 289.5 KB (289509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9632d635ea79d4ed0f20337172c2216e2c1af529629b39d67cddabc7b953f74c`  
		Last Modified: Fri, 17 Apr 2026 00:29:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:6bcfc31564d703d04d9ba8d8d804d67dc922098fb6d0b1df84464bea09397e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 KB (220060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77625a1d19ec6207cf39c9e352ead529f9784b1ea046bf8004557f9d04d094d`

```dockerfile
```

-	Layers:
	-	`sha256:a6f0bf965c87f4d1bed6dbdc35767ecac76a8137fe0b88af08a8380fede4d928`  
		Last Modified: Fri, 17 Apr 2026 00:29:15 GMT  
		Size: 195.1 KB (195147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f1fad8443220a748fe2c2769ac5eb596b74c5ecac4db1ecfc6a84f1b70eb31`  
		Last Modified: Fri, 17 Apr 2026 00:29:14 GMT  
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
$ docker pull golang@sha256:471963d2d4c7070d93c3176f19c69692fe22d5a8557d3bc3e7f4acab8238f16a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68787021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b34c4e7ecbcd37956c8eb7aea41296a5475dac1a20feae7bb94b2f3f727b18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:17:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 01:17:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 01:17:27 GMT
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
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c891dd4ae046679c1687589c197d8153faf17642addb2be03543f6897f0019`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:f4c65bd2a336d5e5858c2d1088c9e9c654f67fc6b824d958c5aea300d93b771d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 KB (218080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7282342035a2b7346ae9968b89d6f562bfe725213a4ea476161bc2a1324fe18a`

```dockerfile
```

-	Layers:
	-	`sha256:3b3206d3c733f8b0ace02999b3ad197c685cae19eb77058ccca687a7bf7a9e0b`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 193.2 KB (193226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3966b96090b2fedbb42b40bfdd9cc87a2d8b16c8411e8435de5d467a2d36b49a`  
		Last Modified: Fri, 17 Apr 2026 01:17:54 GMT  
		Size: 24.9 KB (24854 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:4fcc4718c4f21737e33994ed76bd2862350b1cbc8c894a7e025f39860f11e811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68904697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7ac4e8eccc05ca38ff43c590af2e52f78fa570b5a29635154259c93bc5515f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 06:44:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOLANG_VERSION=1.26.2
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOTOOLCHAIN=local
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOPATH=/go
# Sun, 12 Apr 2026 09:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 09:58:49 GMT
COPY /target/ / # buildkit
# Sun, 19 Apr 2026 06:45:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sun, 19 Apr 2026 06:45:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdd8962c4f9ed7edbc2e6b1e001a985f4958aa4c6da1b39520b3e462cd21f82`  
		Last Modified: Sun, 19 Apr 2026 06:46:43 GMT  
		Size: 289.8 KB (289806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255eecdcfda8d0de735d270cb3d6243b48cdb2c14dd1d93b85cc9593eb17bf7`  
		Last Modified: Sun, 19 Apr 2026 06:46:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:92d16dd1af7eda9fb88afc3bce962ce88b4accc645aa12c6666dbaa7ac7de9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 KB (218076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b1a340922ec6dde322df25bae4de911d831e492749a1e3aef24e2ab8ae5c6f`

```dockerfile
```

-	Layers:
	-	`sha256:fa438b1c8e63440cf6c4e8101634011851f0713f683925cbb154721cfb1e66b0`  
		Last Modified: Sun, 19 Apr 2026 06:46:43 GMT  
		Size: 193.2 KB (193222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e2ef7c7f2fc9943a6259c88b47fddb77cc3f5468fd5bf83022300b0477dbbc`  
		Last Modified: Sun, 19 Apr 2026 06:46:43 GMT  
		Size: 24.9 KB (24854 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:b7cc538906ba1e5be4a26cddbd867925294ac3571ea673cd0fe9e07988848450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70376691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf116fd7083c245ba50e042bc5ab31fa1b4b89ce419634b54534ead8583df0f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:11 GMT
COPY /target/ / # buildkit
# Fri, 17 Apr 2026 00:42:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 17 Apr 2026 00:42:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0222edc5317b2dc2298df74fb4a61c9a344e0cd003e6bcd18f12349c6aee5d`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 290.5 KB (290476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c49503a4e2d600d9a611a3613d8d717f74ee138b363f7bcc9d431274f2b87a`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:88cecf735a27193e508b3333e602364e620756ed60e389fbb5b9a78f5b357d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 KB (217983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2102e4ab039df5e49dd30332464eef541512d295dd407f71179209d083e6b5fa`

```dockerfile
```

-	Layers:
	-	`sha256:0cdf32c3702136c3fb67d73f730c053cf3936f9b276b1824933f64bc9904f398`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 193.2 KB (193176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bc5366622bcfa383e05a60cd08803d5423fa475a7900ec00c427fd330f3343`  
		Last Modified: Fri, 17 Apr 2026 00:42:21 GMT  
		Size: 24.8 KB (24807 bytes)  
		MIME: application/vnd.in-toto+json
