## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:7f953bb2d859a844a5f76f5ebd8b1dc8f5196b00c9469806839c3dff82430f30
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
$ docker pull golang@sha256:8fe082550628c8a39dfd974201e4c63c95765b85c95975a2d8c44415977d9e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87708925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcc906c91ca7e6694e9df6eb5421354ed3e20095de426b6b18690c0921ac54a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db091e23d5610d039e3402870b74302d87da18e4b2fde8c2449c7e2ea805305f`  
		Last Modified: Mon, 08 Sep 2025 22:38:07 GMT  
		Size: 282.4 KB (282437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ded06cd7fc4272134c8fd8dd6fe01e98f582c7adaa60ab9166ea8bfd71723`  
		Last Modified: Mon, 08 Sep 2025 22:39:32 GMT  
		Size: 83.6 MB (83626642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd17d0300ba75345f3215c45ec877c88667b79387c84ff31c27334465c705358`  
		Last Modified: Mon, 08 Sep 2025 22:38:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:912d5448f840b2ae23976cb05ea04ba78d1bba0cba09d56272ebd5a127c9556e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 KB (216665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e581241e81df85e11f700ac72e68bc9c7d690bda2d646235b333058c7ddc61ca`

```dockerfile
```

-	Layers:
	-	`sha256:1928f864cbfada4b2715132c990db03dbc4c434482e3a0e155a399dfa1c20139`  
		Last Modified: Mon, 08 Sep 2025 23:24:26 GMT  
		Size: 191.5 KB (191527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456677578b83c82a9b2c9d4c958789d373ed499b9716284564b4cee4eb54266e`  
		Last Modified: Mon, 08 Sep 2025 23:24:27 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:b0c7fac015fbf6540f6ed3c605045a8d8c6d86e1b1eab2bdde42667db80b3875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84679902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688c2ca44fd2287be00260bf4bfbac35f518416301f8764e99fa70bcb62addd2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6457aff3e3b183002f97aace2dc68398e1c5112d5d6eba56025ce508cc175d80`  
		Last Modified: Tue, 09 Sep 2025 01:19:40 GMT  
		Size: 283.3 KB (283328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcbe18c0f889b22c938684b528ef1c3ed22f9b8e65f539809799c450b1bf80a`  
		Last Modified: Tue, 09 Sep 2025 01:19:49 GMT  
		Size: 80.9 MB (80895506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4079afdc2493e68dade7e7d49a2f3dfa8651384b3c6e35c84a4b13412b22c31`  
		Last Modified: Tue, 09 Sep 2025 01:19:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:061fdf1a4fa79cb995e1dc63789e2a979749b8ca327cb889eca27748b55c1c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e704d4ebdf19c93c0c8a4b48a08159f00758a9360a052c6c0beff4157e23e095`

```dockerfile
```

-	Layers:
	-	`sha256:990aa6a6f00100540a1e84f1829f653fb9318ae09f6a6aac43c5bb31a6aed6d0`  
		Last Modified: Tue, 09 Sep 2025 02:23:11 GMT  
		Size: 25.1 KB (25051 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:8b5f40be24ce53c9ead1b6ebb65a8ed63b613446402db51527bee4c090a53aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84013970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:708d939e450b0418f2ea9eda0c9e26b5f6e7610e04ea609d4da1e13231bd0c04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d1c7cd6f49363bcd6156bb689087c0a4e1624bb6497290e03e589310895c3e`  
		Last Modified: Tue, 15 Jul 2025 23:00:53 GMT  
		Size: 282.5 KB (282485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8183d7d02c47a9b085b3d0bc6d67309b7fa4b7ef97cac1694dc0b5ea8b6ce9c`  
		Last Modified: Tue, 02 Sep 2025 17:26:14 GMT  
		Size: 80.5 MB (80512289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba87bac453220f2e79296ba55b884f58ca354e66a820e73f35a7ee1a9c4e118`  
		Last Modified: Tue, 02 Sep 2025 17:32:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:12abfe4e7f93ef3ed612c6f67c8f58d217bc6e606e9a254b490c623120bfd311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b190d7322405cd0c85a9d0fe50801344c11616e30f9cf2ab0e8a75b2c8a049`

```dockerfile
```

-	Layers:
	-	`sha256:133413a42d959d8ae468a161b3a0fab97eed36c0cea380db3547f8a66316e237`  
		Last Modified: Wed, 03 Sep 2025 20:24:06 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:419077c4158cd7fd41fe308d0592f5da628d4e7864763306bab0abbfcfe07655`  
		Last Modified: Wed, 03 Sep 2025 20:24:07 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5ad0a3d3ee9c67c68af590f1a79559def9292fe52739185ce1c7b9226bb40a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83879077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4a158102989352f46a8b4ed881cddee3990e5567721d4e3d143d51f0f45ef9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21357df949f743a56d3417cb15486b8a5579e1b74b558f43b89f72158c8010f`  
		Last Modified: Tue, 02 Sep 2025 17:28:59 GMT  
		Size: 284.7 KB (284705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948ccd09d5c498d3bdd3015babafec64e8e01106fe6a739f268b131403fa7cbb`  
		Last Modified: Tue, 02 Sep 2025 17:24:20 GMT  
		Size: 79.5 MB (79463464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c27de6762ec6e9751df491f3adc0b399fb062458f6a695574cff548c5e31b95`  
		Last Modified: Tue, 02 Sep 2025 17:28:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:fb1913b5c3b2001da1ef33f38d1a3b6ec2255fe1509f3dd846bf6bed9c562b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fdde1c5b58ef37cafc0dce67411d0676a44c1a1bab03d6f4541c227f011a2a`

```dockerfile
```

-	Layers:
	-	`sha256:bd955ef1e9429189ffa1c06bd08bf27472c047b91990e24f17f237ca693b4814`  
		Last Modified: Wed, 03 Sep 2025 20:24:10 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:300030301c99c9ce564d047e0ab261bf6794fb7974bb825bc428461f5a19d687`  
		Last Modified: Wed, 03 Sep 2025 20:24:11 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:23145cd6bac6aef178f3219cdd67a359f49d6e780249310f662867e0f4589e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86188642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40051227413253e49a1900ba8c83da6af68ce63809e34c5401d8d10b477987f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 08 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58347b0235dfdf8d337c8a97a9f6fdb9090c38dac80d081787b0879a31ede147`  
		Last Modified: Mon, 08 Sep 2025 21:55:19 GMT  
		Size: 282.9 KB (282935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518dceeeab292a9ac96f797a930543374e02f8a442c539c30c018a2f30d27fff`  
		Last Modified: Mon, 08 Sep 2025 22:30:33 GMT  
		Size: 82.3 MB (82290543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b235d9acec4712857df83d2105314c7b82ca3f351b30bc5a5c917b40c89d93`  
		Last Modified: Mon, 08 Sep 2025 21:55:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3411d2f30002e4f0e58089330816da62a5afa0279596faf4446b6a4f5cfb1bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.6 KB (216583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2eaafd11ef501486f02b58492e7f7b982a3c14e922aecebaae3beaea347619`

```dockerfile
```

-	Layers:
	-	`sha256:8c4545d6353084cfd004664f14fce83a33361cc28cb5f3eb6860f7d598894bcd`  
		Last Modified: Mon, 08 Sep 2025 23:24:30 GMT  
		Size: 191.5 KB (191488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba14403b6120b918d3a984335db09ed21b3f0eed37afba123f00397b5b786b0`  
		Last Modified: Mon, 08 Sep 2025 23:24:31 GMT  
		Size: 25.1 KB (25095 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:43da9e4eda68b38306e899ed92f4f626e2187feaa929c6d0939a9e49f53adefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84828307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61afb74d9eed1731a50abd3cc6da0862f8bac3ddfe982149510c77fecacfbcca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093a8784e85737b54c7bd288e58eb1c4d919cf932185be9835fe0acd194ad05`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 285.1 KB (285121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65adef97a585f4d6f34375efc6b453ef50bc737c051ef6eb9403cedd2e831eb9`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 80.8 MB (80815917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6c32a48d93963a4d27813669fdbea9c34f26e45cd91fbaa9d96c210dbed8a1`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:7e151042de03954acd66d71dce8afa6481b40413e297dc28b494925bb236acc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e14dcf6c30366f933c342e1d899cc1dfb8839924cc77cde3fa8054eefbedab`

```dockerfile
```

-	Layers:
	-	`sha256:b4a463f518e211f862ba60f08a5395bbb13e72a2235414789abf0f3f130fb36b`  
		Last Modified: Wed, 03 Sep 2025 20:24:20 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbc0bbb4276e97da55c00b023a3aaa23ee2fb0539e1de4409c5330021dbfaeec`  
		Last Modified: Wed, 03 Sep 2025 20:24:20 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:e22af9fc5cbd5f37886f4502f6da91d16771df25bc0aedf9d17572b41cd1d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84686874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ee6c366a39cb66afc19a0cad905311eca4c532943bb8771efa36634298ff00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293eb689539c18522b5644ece27c44567aa0a4ab5ae7b74edd76c1cea9f0f71c`  
		Last Modified: Wed, 03 Sep 2025 05:13:46 GMT  
		Size: 80.9 MB (80891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7afa004129fb15f859e90a6e4fa3f104a09530c1c655b24f9022987086dc9c`  
		Last Modified: Wed, 03 Sep 2025 05:55:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:aeabe4ab0cbe2d5cead3f727b8360054ca328ce065763862aec582f749ffd31a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ffacd1d55b87f25b0c3859cd5739b9ff78cb851abaf428b7b98e35706d35ae`

```dockerfile
```

-	Layers:
	-	`sha256:45fd23b94f66345b96b2a10980864610824385a1324070d7b9d9a696f1a3c8fd`  
		Last Modified: Mon, 08 Sep 2025 08:23:31 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d78b03a6b420db292a67f3c6570402e3e48e32e702af2dde100d7a4dbc166bb`  
		Last Modified: Mon, 08 Sep 2025 08:23:32 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:1130d871939bf911805c63ed8800dfd27f841ea7fa55a816d5540e32aed79165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85959657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95dd45f2b65542ce9fd28c9981f6217d319066f93b2300a1c79704d1a0ab52b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 01 Sep 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82129bb6bf719d3efe5e37bbda9c61ccb03eefc8feac9fceac09035731c0c7d`  
		Last Modified: Wed, 03 Sep 2025 20:46:26 GMT  
		Size: 283.5 KB (283475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d5b2317c0e6d0b707d21864c7e46b8277ee225d4365f7839ca2960a88e985a`  
		Last Modified: Thu, 04 Sep 2025 01:06:05 GMT  
		Size: 82.0 MB (82031053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7f6f7ae5735094c802725a61149975e0052413b565d930fce020d19fecea9f`  
		Last Modified: Wed, 03 Sep 2025 20:38:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:b1d6d3dc52b6fb91a63424db869b69a8fb9c2673ba8988eca48eabd0fcd4def6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cf8c74eb8a979819a8e63522684354a9526086256f1a06133432418d3b5b7c`

```dockerfile
```

-	Layers:
	-	`sha256:7f32d19f2a6f46dbc9717da7e0833bc904217f380e872eee70d6e47e31ac415c`  
		Last Modified: Wed, 03 Sep 2025 23:24:32 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb24abcdd395b8d0f5f741e9b4fe4eeecbb240940c09e1c33163d05d590cf0d`  
		Last Modified: Wed, 03 Sep 2025 23:24:33 GMT  
		Size: 25.1 KB (25137 bytes)  
		MIME: application/vnd.in-toto+json
