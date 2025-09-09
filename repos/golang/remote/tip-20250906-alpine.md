## `golang:tip-20250906-alpine`

```console
$ docker pull golang@sha256:1a87d951381971cbad8a1346964cec6fefe38a52f1bd9b7e22bc12a2268b3c33
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

### `golang:tip-20250906-alpine` - linux; amd64

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

### `golang:tip-20250906-alpine` - unknown; unknown

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

### `golang:tip-20250906-alpine` - linux; arm variant v6

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

### `golang:tip-20250906-alpine` - unknown; unknown

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

### `golang:tip-20250906-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:9054d2ef08398bc062b3d32c62c35f5449b0e98f58cf1c28a0c9abb6e16f3b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84158543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405410fb0603550f5eda849fe56c8649ee8e9d0b93c0a1860c75790b96990db0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bef6d0fcfa54d75b2d58ea1c7d41ed287cdbb9633682e80badb434c6409bfc7`  
		Last Modified: Tue, 09 Sep 2025 04:08:19 GMT  
		Size: 282.5 KB (282500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b1c648c56772cd07e1e12fd2a4863e7957cf9814eefb36938de6dd4aba1cf`  
		Last Modified: Tue, 09 Sep 2025 04:57:58 GMT  
		Size: 80.7 MB (80656847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77247eb31945081bd72897c70dd187ca1d28bd31e2cdcc9d33c998ddc46bb7be`  
		Last Modified: Tue, 09 Sep 2025 04:08:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250906-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4be91a953b42de9452b1b53165a18e54c4b2fe0ba82ff05ebef79faa9dbfc08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 KB (216815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77d0e257cf98c0b24a958caab4a57e2e1c90376b23198a68acb2e6c0bc340ea`

```dockerfile
```

-	Layers:
	-	`sha256:11df416516f2f37a229b30efa2236e94bc908d24629b724c1f665d4aaa3f46ed`  
		Last Modified: Tue, 09 Sep 2025 05:24:09 GMT  
		Size: 191.5 KB (191549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:913698b3c8452bbc5384ba17ea66136c3034d416a0ba3e051732d2f297a0db35`  
		Last Modified: Tue, 09 Sep 2025 05:24:10 GMT  
		Size: 25.3 KB (25266 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250906-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8669bbf8569215f93721b612fe5979c93e7a320b93d391d5a87c84d3d3588f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84038534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a9a45556967933339d41c7e7ecb0a1eaa33d72eab059e64a377391fdd9a3eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49089f3f1d2ed1087d82b4bf0cce94b8e2fb07fc822c112478ac03fdfc495883`  
		Last Modified: Tue, 09 Sep 2025 02:12:16 GMT  
		Size: 284.7 KB (284708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ec503842f40108336c064bf1248d9e53857dd90a255bfc354d17bccde7d80`  
		Last Modified: Tue, 09 Sep 2025 02:26:39 GMT  
		Size: 79.6 MB (79622918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31800ea1961890d2fffd74574a526e244d30df3e495c4fab72a3fbd42ea0895f`  
		Last Modified: Tue, 09 Sep 2025 02:12:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250906-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:97839d43fefcea317394132ce3fb429914a6320265d083d98d43d1dabecd1ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 KB (216881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224b48fa5317870c6b3bf7ba0c73c794761e86958f7a0b019f36cc136aa9e8c0`

```dockerfile
```

-	Layers:
	-	`sha256:b5d2bfff06a5fe3aed8badf1c306de66fbe826aa864d6154d0269dc02b6280c4`  
		Last Modified: Tue, 09 Sep 2025 05:24:13 GMT  
		Size: 191.6 KB (191583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a304d58ec2f1fb50c02efc79e25e825fed46b48eb8f88ce1db2efdf985d02462`  
		Last Modified: Tue, 09 Sep 2025 05:24:14 GMT  
		Size: 25.3 KB (25298 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250906-alpine` - linux; 386

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

### `golang:tip-20250906-alpine` - unknown; unknown

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

### `golang:tip-20250906-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:f8681afa5cff4991b4d5761419812dc5ddd543a7eb264c799df651148aa1828d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84992358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ad469380f313e4cd72d83e7a2b705c8ad8e2e0cd25a4ea836f1c8d110e163b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
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
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093a8784e85737b54c7bd288e58eb1c4d919cf932185be9835fe0acd194ad05`  
		Last Modified: Tue, 02 Sep 2025 17:37:11 GMT  
		Size: 285.1 KB (285121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1051bc6933b658b142c723792e59e09c480598eeb964b45782057c6c9144799`  
		Last Modified: Tue, 09 Sep 2025 17:08:24 GMT  
		Size: 81.0 MB (80979968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0271e1d6c2293c93c53bf4d0721de1a15176ad33bfe057ddf4fe59b7f1ffb19d`  
		Last Modified: Tue, 09 Sep 2025 16:59:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250906-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:41270f762e4ad7f61119be440f0d712269e9b4960d6348cdd56c19c528c7ea15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c81f855e6f440e677b5e595307034f7c57a22e39a859ab6ee31b54317eda43`

```dockerfile
```

-	Layers:
	-	`sha256:fe39efad7a231e39fa174441b752336c17f77c85bf6a1bf7dfbf006905a6fbfa`  
		Last Modified: Tue, 09 Sep 2025 17:23:23 GMT  
		Size: 189.6 KB (189624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4674064663f10034504d2fe5e4b67dcc7584bac9f607a5111ed381900e7f61f`  
		Last Modified: Tue, 09 Sep 2025 17:23:24 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250906-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:4baab422c32cf3e012916002c2cb758cc6bed9edeed47702689a9782197a5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.8 MB (84841402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6cff23ac529bd11b99253ef71b78efd44d61394b128d20b68e4111f624b123`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c829abce40c6e676411d0af62b8c004ecfb77ea108ba2632a87a5640426b84be`  
		Last Modified: Tue, 09 Sep 2025 09:50:53 GMT  
		Size: 81.0 MB (81045663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb9e0ecae3db930f5291777e8f00cfe1461b70a1593eb202a8571a863d5a048`  
		Last Modified: Tue, 09 Sep 2025 09:50:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250906-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:327f9d35cfe8933609c304de4d2f8f2cbf6d20fefefb743f034d3897b9de4604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 KB (214816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d63540e470faa5a456bbdc1278a43fee659e79450883cc15e1e34893b736a4`

```dockerfile
```

-	Layers:
	-	`sha256:451a258397d5854bcbc36215bc4d4fc576009b7b3f17ae672997531c1f097903`  
		Last Modified: Tue, 09 Sep 2025 11:23:31 GMT  
		Size: 189.6 KB (189620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4cf68f9e0afd02986240a335b8f8c117a63c0a6a8d5f58c73d86d0c9cd52b73`  
		Last Modified: Tue, 09 Sep 2025 11:23:32 GMT  
		Size: 25.2 KB (25196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250906-alpine` - linux; s390x

```console
$ docker pull golang@sha256:c7f763439a3e8ae783aa5d39c27de4417994a1cf629d2d25a4e7619493ec64c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86114204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54da7c7a2064f8e2193e8fd7f66cbfc5827571745c59ac6c5df69e0abe1fd175`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82129bb6bf719d3efe5e37bbda9c61ccb03eefc8feac9fceac09035731c0c7d`  
		Last Modified: Wed, 03 Sep 2025 20:46:26 GMT  
		Size: 283.5 KB (283475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4433fcbd8b218065f69331fedd31f57a7cec1ad8aeb95ea22dc5e132a3d8aac2`  
		Last Modified: Tue, 09 Sep 2025 13:14:51 GMT  
		Size: 82.2 MB (82185600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8879bca8c294377ca811b1715983d87980ca2f295b46fc4051d6e71e98c30c89`  
		Last Modified: Tue, 09 Sep 2025 13:14:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250906-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a73a5e24d31811ce7277a437790074d10905712630b84dea355cb154ff373a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 KB (214714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07818afeb20c9e414c81bbebe5de92be3a89d5f0a505dba35c8e07703f5ac015`

```dockerfile
```

-	Layers:
	-	`sha256:3b27c7ecbc33a0994de708557b01b072258bfe129124de9e4e463896e1e912a4`  
		Last Modified: Tue, 09 Sep 2025 14:23:28 GMT  
		Size: 189.6 KB (189576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4418dc18e2a8695664f55c0a870a3bd83d961c050dc99e2ece053612a1a169`  
		Last Modified: Tue, 09 Sep 2025 14:23:29 GMT  
		Size: 25.1 KB (25138 bytes)  
		MIME: application/vnd.in-toto+json
