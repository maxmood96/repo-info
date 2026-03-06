## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:abd368ab2c5937e709e90f501786552af002bbfad1631bad94e660096c0223a7
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
$ docker pull golang@sha256:c471cc2e84269bfa2b3fa76bafcc34d32561157513fb162283e3b3eee983a9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97699539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a1ba5ade1514ce22791e738558eb23cac32147e93c6386990c412392cd4788`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:01:21 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:03:17 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:17 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:17 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48525f5eaf09f5c482c54e2c3149ac2d1c3b91eb6e027ba4cf9cb68ed03346f`  
		Last Modified: Fri, 06 Mar 2026 02:03:34 GMT  
		Size: 291.2 KB (291160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c664b692c42c224e696026ec9ec2afa2556b09a298fb5881d3823f0c6dd`  
		Last Modified: Mon, 02 Mar 2026 22:02:43 GMT  
		Size: 93.6 MB (93603346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e86196a33bf366f76516c0209d1748bf34cafe3b69921d64115005f5704910c`  
		Last Modified: Fri, 06 Mar 2026 02:03:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:47963683f3690c29d5b9ed4839139695371017de03e17213847e8c9165e74942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffa6c3ee52fe9ff1d06d1d4cfef7a81822c36663b6591ac6c522063646fd507`

```dockerfile
```

-	Layers:
	-	`sha256:a2b8a5f858d827663cb5820417fb49408c264b19545d1e8a4421da62f04b0f51`  
		Last Modified: Fri, 06 Mar 2026 02:03:34 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a70fa7be58b3e5a65d70bd9569eb8962f1479f2ccc2a8ba7f18337f11427979`  
		Last Modified: Fri, 06 Mar 2026 02:03:34 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v6

```console
$ docker pull golang@sha256:fab5b69b3c133a27089ab7efece7a829ea6abbdc88462f44686dc92a19d09dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93768124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97376e5b01efa0b653aa8c090d8200dca636291c4d83082317671bf05a7d768`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:59:31 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:02:19 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:19 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:19 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c79be00da80db0c0ea9098c53a998eeca3b7750e8f341d2859db4b78975037e`  
		Last Modified: Fri, 06 Mar 2026 02:02:34 GMT  
		Size: 292.3 KB (292316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f75482abeb648b9189b3f4696db6444fed715bf37c369ca85b2202c497f7c6`  
		Last Modified: Mon, 02 Mar 2026 22:04:54 GMT  
		Size: 90.0 MB (89970604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2955ae40d76347369dc9c77bc2038131ec2a637c882ea53080c329a33327c86`  
		Last Modified: Fri, 06 Mar 2026 02:02:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:884926d3b5c7595166841467fae202e7109838be1930aaedfa70226d1184ff8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c604599cc9e38d6355bb145049ef946b0ac549a201105786c438a7a75c61aee`

```dockerfile
```

-	Layers:
	-	`sha256:51f9b3e0362fe5c2170c0dec81ec7f80f207b63c969e7ba2ea15ebc0a8052c98`  
		Last Modified: Fri, 06 Mar 2026 02:02:34 GMT  
		Size: 24.4 KB (24362 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm variant v7

```console
$ docker pull golang@sha256:e67d78fc72de286a39d18737c394c70677bf8fffc994068395de356161f55c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93211665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b645f3c2afed8942e9c1951e20e2c20950532f15b2df801205f83abb1f79ee20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:01:09 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:03:56 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:56 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:56 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd13121ba81d44a865f4f1026b8a0220932c5274a872f702027bfa4b8b9e0f9`  
		Last Modified: Fri, 06 Mar 2026 02:04:14 GMT  
		Size: 291.2 KB (291214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619c3f71f77f69e225ea5672e51800bfe43c91f26a92fa075ed4ae7f1770dbac`  
		Last Modified: Fri, 06 Mar 2026 02:04:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ea7d0e29fd3d532428ff62caf837cf49fb7bdf535fc670fd7f047ccc3dc1fc91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6005f3837a7d6ac5621b24c72f5c74e20563a1542ad1bbb98445e248d87b1967`

```dockerfile
```

-	Layers:
	-	`sha256:54f46111105ebbe59afb4d9dd8279f8c82c21da25a7ebef093538644ccd8c732`  
		Last Modified: Fri, 06 Mar 2026 02:04:14 GMT  
		Size: 195.0 KB (194986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd21c8db3c3d2585923125c8f6c0913b75bdde379529c48cb12b3deb3f3442c7`  
		Last Modified: Fri, 06 Mar 2026 02:04:14 GMT  
		Size: 24.6 KB (24577 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:951354ee7093eff87406295a433a4f180934f9357c286a549c30853a10ec7bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93218604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4816ac5bba6757faa1ee1e52bfe26ac71744638aa8b26d0c2b63ade8e4d7ca9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:05:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:06:44 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:06:44 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:06:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:06:44 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:06:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:06:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53cf0a862aadb041e3dd2244ba4cc4cd01c2b2f846d937d8ff9e6af1517bc9a`  
		Last Modified: Fri, 06 Mar 2026 02:07:02 GMT  
		Size: 294.1 KB (294097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e982fdcb72c3ad1cca7a139b473ea3951042395bd4cf7fbdb4f775c24a9b551`  
		Last Modified: Mon, 02 Mar 2026 22:03:07 GMT  
		Size: 88.8 MB (88784830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088a580e9e416f7c9b0c5b6eac29a559786fd64c7d873bd7627d253026652144`  
		Last Modified: Fri, 06 Mar 2026 02:07:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:0a7269aeb8f45298d4d857cb5d7f9839d77a7f34f689bd0139429511ca4c808b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6541c0bfa1ed218c2326e6277cb198285d9b8fa4dd28daf73923b8debadd4333`

```dockerfile
```

-	Layers:
	-	`sha256:0ad680b81727fb480052872a200d4445508b045f7ac5f7d373327c96580a8a99`  
		Last Modified: Fri, 06 Mar 2026 02:07:02 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79cd0f61a6dd6a286764117917503ae8a6b49b59456a0b93254a23d5a342e9c`  
		Last Modified: Fri, 06 Mar 2026 02:07:01 GMT  
		Size: 24.6 KB (24600 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:bb92ba95d68d70d6003f924f5a79f8bfc8673d463a3fcc1c0ae3ebe58ccace09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95361438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98412ec433f7cf2f764e864d9bc7d0a3e19b9cdfe44bd1c66b8512f5340f3dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 02:03:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:02:38 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:38 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:38 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:05:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:05:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052dd817c54a608953e7513c045459d371374fdf42f9cd39ff4433ac722d0d9f`  
		Last Modified: Fri, 06 Mar 2026 02:05:26 GMT  
		Size: 291.6 KB (291626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b2140e9f06d205b6b5af3fcc14f26b13013365f22129c2ff99cb48ee34776`  
		Last Modified: Mon, 02 Mar 2026 22:04:44 GMT  
		Size: 91.4 MB (91448922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e581ddf0dfcc7ac64aa0b4b727606f85c86675618a28105a9426b5680e9924`  
		Last Modified: Fri, 06 Mar 2026 02:05:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:40d7eeb911a18b7a3ff5962413b365dfbbf1333155a03e2c874c3ff19205ea83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bdadae6eebb76161797f008a7d325d9dc7c26e6e22045394d4f0b385d41a792`

```dockerfile
```

-	Layers:
	-	`sha256:cfdc39d0aab1ceaedde9a2d34b5ac44be6293656431af46016688e6e15480afe`  
		Last Modified: Fri, 06 Mar 2026 02:05:26 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5a94cddc83f69b1a0c9b143205138eeb6d981f89d3f2693f85231471733d75`  
		Last Modified: Fri, 06 Mar 2026 02:05:25 GMT  
		Size: 24.4 KB (24431 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:7fa2014721a5045a99385067a84cd2c684e13009a7b5ef4be04da955acdb03ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94344929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a93490513ffc98f8a311c69baaa80d5622154579f454261a95aa9265c3d64c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:04 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:06:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:06:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f02f69aab787878d0fe63ce3447907150c58efe2b290a63ccdc4a10152b83f`  
		Last Modified: Fri, 06 Mar 2026 01:13:19 GMT  
		Size: 294.6 KB (294587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc3a57b0d1a4c549275152be846eeab1e4bfda9d363982944775991fe15219`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.3 MB (90315888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982c155d3f447cc650e69555a85aa75d5c6a1952f54f1ba2fa5567809576c689`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:83cb672ec47ffd183529b0235572012dd7589c5dd43e8cc066a723b5e8fe6483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3892c115bd0cad2a98a310fca4fcb0dba61eada880d8b779da58a6cb8f7e14d0`

```dockerfile
```

-	Layers:
	-	`sha256:c35b17e5a91d74818746539e790b57bdc6370da46ef68ff13327ac81e7712871`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09c22cc24afe1135cc2c06b613d43eeacd5a0667c062d47b23f484c97e5254b`  
		Last Modified: Fri, 06 Mar 2026 02:07:20 GMT  
		Size: 24.3 KB (24338 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; riscv64

```console
$ docker pull golang@sha256:f38a447af32c82a25de0cf61b3435ce225ed9f478f0fd1b36174aaad7aa4a6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94598361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5953d450324b93bfe4c3303d3ff94a7a8ab826cb1fc25b15b0160136f87bb72`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:15:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOPATH=/go
# Tue, 03 Mar 2026 09:03:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 09:03:40 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 04:04:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 04:04:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dcab0b270d631ffdfee1c090f676984c71b03f87fc76005b512418b2ec110c`  
		Last Modified: Thu, 29 Jan 2026 19:17:49 GMT  
		Size: 291.5 KB (291499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550964df09cbec6e16da50f25098e25826ade610bf4557ad9371e12e9ced3d4`  
		Last Modified: Tue, 03 Mar 2026 09:10:27 GMT  
		Size: 90.8 MB (90789282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef5d23f44614801b7569fdaadf56e1dacdd39053e486bd787c170c8ccd2f39`  
		Last Modified: Fri, 06 Mar 2026 04:05:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:3a332892f6458b1e665b16dc3da6db2a789bcb6280281d37160c5cc50d93ca25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 KB (217576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b98dfca10eb6aef8886f6d89b9cc9e6eb69dc7b83898d11258ca4bba9933bb`

```dockerfile
```

-	Layers:
	-	`sha256:cf169df80b1afdd0e672f2070c82894c2144cc8f6b7d3f5d23c4d41396d0a67c`  
		Last Modified: Fri, 06 Mar 2026 04:05:27 GMT  
		Size: 193.1 KB (193065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6105f88b9c1c8e1c0c300697a9f4accddfa132a22eb16c03ca9410e36ff7957c`  
		Last Modified: Fri, 06 Mar 2026 04:05:26 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; s390x

```console
$ docker pull golang@sha256:b8896c901ee553f69d76220511f14e5481ae33503324eb9072d23025a5f9113a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96745301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0e6b6b806513629e0a174fa623115a6a055af8d0bb18752d6cf9b07899dceb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:10:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 02:01:51 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:01:51 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:01:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:01:51 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:01:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:01:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1d36c7004440a7bc74888d2f6443567456c48f3d6c6f7ac34b012ece010cd8`  
		Last Modified: Fri, 06 Mar 2026 01:11:10 GMT  
		Size: 292.1 KB (292149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d3098d11b942b930d9b88ef8d2b13e42c10d7ccd12c5e317467f410cfa58`  
		Last Modified: Mon, 02 Mar 2026 22:04:29 GMT  
		Size: 92.8 MB (92802560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7cc7c085d9dc1a6682b8671453f8721b644b7535b62f677fda4c3ec5e3d8d3`  
		Last Modified: Fri, 06 Mar 2026 02:02:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:ad2fd1003422214b97ac48ab69709784ba2c84749ce26b00460d7de4ccf2d987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 KB (217323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf53893519f9351f9e6a79d9d863f1b4832747d40b83da225d48df5a0ffbc07c`

```dockerfile
```

-	Layers:
	-	`sha256:6b811a39ff90868cdf03365def026dc8b4eb2d5c9891f75d15a1c671afba2551`  
		Last Modified: Fri, 06 Mar 2026 02:02:19 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b1bd99c19d75af35f6bc3ea22b7d34a73b953541ca903a288600fe3de48a66`  
		Last Modified: Fri, 06 Mar 2026 02:02:19 GMT  
		Size: 24.3 KB (24292 bytes)  
		MIME: application/vnd.in-toto+json
