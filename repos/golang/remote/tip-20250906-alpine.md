## `golang:tip-20250906-alpine`

```console
$ docker pull golang@sha256:72213e6b7612128541e2732bea2ed966082b883ebf2dc9c0a75b2bb372aab7df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
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
