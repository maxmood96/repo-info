## `golang:tip-alpine3.22`

```console
$ docker pull golang@sha256:8c371084c039e192fd9f8a8ddf75ba0735fbd20d98d7bf4da52ef36510088154
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
$ docker pull golang@sha256:9be797a77759a2adb428fe789503430ef1904300e4c6f850f8f6813d17314643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97760182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bb3dd6b02380fb2381ea2b4f7dd5e9614c550cfe8efcc74093f575356132d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:34:47 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 18:36:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:36:37 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:36:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:36:37 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:36:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:36:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a758dc760d5ee44543d1a985535d8f51f23b1024f6b96462ab2fb105cccec`  
		Last Modified: Mon, 09 Mar 2026 18:36:53 GMT  
		Size: 291.2 KB (291157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a04c034b447c8996669d72bbe0e1d2cec1d82755b44408c364d44c021efa7f7`  
		Last Modified: Mon, 09 Mar 2026 18:36:47 GMT  
		Size: 93.7 MB (93663992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d3e568c9e4b60a4798641cac8e085cee620459789beeb10e80e2cd6af2435`  
		Last Modified: Mon, 09 Mar 2026 18:36:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:52515b752fed7629c028710987d89d9a176c40607ddb64252e67fc559aaee698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4155d5989e00187e4f9f3f7cc7e22b5d91ad662346b062dfcb05c16f252cbd`

```dockerfile
```

-	Layers:
	-	`sha256:4056d387eca688767238571629c9c07ee7722d60dbaa8a066f193277249dfc63`  
		Last Modified: Mon, 09 Mar 2026 18:36:53 GMT  
		Size: 195.0 KB (194982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc97cf930a68252e051290daceae3c5228359bd089445cf7ec65bc1f6c971dbf`  
		Last Modified: Mon, 09 Mar 2026 18:36:53 GMT  
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
$ docker pull golang@sha256:0bef86ac40a0596f59d68c7ae3c2e58419ada124f79db7b5017a5548623c0159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93267448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ef27fc8d6df47e6c9312881294c63aab4207394a72a01ea1046ba9c16e1bb1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:36:11 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 18:38:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:38:00 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:38:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:38:00 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:38:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:38:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95fb583a8b8d9062c75f9581fe3f9e8a19ff9d56a5a2e13a2e84669cbaabbb9`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 294.1 KB (294089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1276795b08c8a192fe74bc0ca89800479d8cab1b3bb0e3b28f26af398b665fc3`  
		Last Modified: Mon, 09 Mar 2026 18:38:20 GMT  
		Size: 88.8 MB (88833682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b75353c1602d54dc692ce7e7496143df3825360f0a7c69451b63cd0681f14ce`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:5dbabf387b8c29b59d231cb76bfe0d4322f545aed9413e47785c489efecedccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 KB (219615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7b12ddd75a93b70a93ceef26636e7491195fc256330a4cc2ac4f6f79922a33`

```dockerfile
```

-	Layers:
	-	`sha256:178166a27828e6dd19d5e2fdff50f8d8d6981d700ac856aa84efc5e5bea77479`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 195.0 KB (195014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:679f3ee9b1d48b42209c8c1045b8a7e1981cf29d36cbfebe44dae0ea238ac585`  
		Last Modified: Mon, 09 Mar 2026 18:38:17 GMT  
		Size: 24.6 KB (24601 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; 386

```console
$ docker pull golang@sha256:4cef400ebc2a1bfbe9380c9d8fc33f092545a910a65f50588a829d3881b00275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95428401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221d50ed01008e8a3faa5f178c8433685b65c14be3bfca3a15b4aa6b1e722032`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Mon, 09 Mar 2026 18:21:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 18:23:29 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 18:23:29 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 18:23:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 18:23:29 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 18:23:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 18:23:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267e739d5b2121dd2b4f14cce44c5e7344d1b1ce8bdedb94da0d149586fb44cb`  
		Last Modified: Mon, 09 Mar 2026 18:23:44 GMT  
		Size: 291.6 KB (291632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8181476688ce59990f6e1b32458c610684950481d47bcb0583cc777042e4e2`  
		Last Modified: Mon, 09 Mar 2026 18:23:47 GMT  
		Size: 91.5 MB (91515879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b67a29d340e8cfa895548cf415726ebdbc59e6dcf10292f17a06e0510b626b`  
		Last Modified: Mon, 09 Mar 2026 18:23:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:00dcfbe4b91138b8e08dac4245b58924caf8d41a68c6b9c2e54e5d6fa547b39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 KB (219383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193c19ce741ff060448731dc32feb57fde79b1088d536ae8cbf9250561a26f69`

```dockerfile
```

-	Layers:
	-	`sha256:3ded59aabf84cc2dd68636b83d6cae97ecb26182de480e868231e1aae0b2b203`  
		Last Modified: Mon, 09 Mar 2026 18:23:44 GMT  
		Size: 195.0 KB (194951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37b1dcebb6f03db0926b977c36830bd1ff94fa2595dba6920176c1ee02c5b588`  
		Last Modified: Mon, 09 Mar 2026 18:23:44 GMT  
		Size: 24.4 KB (24432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.22` - linux; ppc64le

```console
$ docker pull golang@sha256:697c7b5a5214bd093338d6f8222c3f7986344afb1e63dc686a92a18a01eb5e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94410567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0b012eace847012a297bd383458aeb1c45e4b55e54c157ae4051441b03f9cc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 20:29:53 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 20:29:53 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 20:29:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:29:53 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 20:34:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 20:34:23 GMT
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
	-	`sha256:7fd4a2e00fb2b423a29812f722692ff6df643271561859f95cff5536124a1105`  
		Last Modified: Mon, 09 Mar 2026 20:30:57 GMT  
		Size: 90.4 MB (90381527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c99701f6c7e9e903cd219a6601ee5c0f4c3114880ecb9b758085a8e0611721`  
		Last Modified: Mon, 09 Mar 2026 20:34:39 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:e3f2d02230f5aeb1981abfd96f88bc5297c7b6afcb43eac3f57e2eb6e5100966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 KB (217407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c394fd7bd53a0927b25ca4598bf41f5dcdb715622bf467287e6a991542a329`

```dockerfile
```

-	Layers:
	-	`sha256:8a769dfc4f030f1b1d90dc5335b824fdd3b967d455ae669e052a5f716f95dfcb`  
		Last Modified: Mon, 09 Mar 2026 20:34:38 GMT  
		Size: 193.1 KB (193069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4652304248d74503f55db8c0281ba3a253647d20a21b8a10f3ff116165423083`  
		Last Modified: Mon, 09 Mar 2026 20:34:38 GMT  
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
$ docker pull golang@sha256:53ccb7739c700ad6bdb7edb24de574d50a19fa72a40fa7863073a33c76c1ea80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96809306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f11df442cb741550b08bbaed6282b178329683c70a63133132f5ab3fe4f4ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:10:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 09 Mar 2026 19:05:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 09 Mar 2026 19:05:14 GMT
ENV GOPATH=/go
# Mon, 09 Mar 2026 19:05:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 19:05:14 GMT
COPY /target/ / # buildkit
# Mon, 09 Mar 2026 19:05:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 09 Mar 2026 19:05:16 GMT
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
	-	`sha256:cdeaa76acf61a14d8cb194df2a407d1383d717722d6e254333be0cf42263af58`  
		Last Modified: Mon, 09 Mar 2026 19:05:28 GMT  
		Size: 92.9 MB (92866565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1874128cde57f68714aca0ed53caae04e59deeb0f95b29fd55dc5d512e25f7dd`  
		Last Modified: Mon, 09 Mar 2026 19:05:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.22` - unknown; unknown

```console
$ docker pull golang@sha256:19224bfadd7adf3b0f76c181cc5b08eaf8f40dd2918c3e14fcca46bebde9aa5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 KB (217496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528837c7b3d01f35676f75dd7963faf112c87812fc6351e96ea1c8a12b78b3f9`

```dockerfile
```

-	Layers:
	-	`sha256:248f0a2e0655f026ab7fadb25df09515c77aa3fb5071ba4c3dd68e5ea9c019fe`  
		Last Modified: Mon, 09 Mar 2026 19:05:38 GMT  
		Size: 193.0 KB (193031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0046ecd7de92fcd7b013b3d169573a68c432f57c7fd4c79b9614ceedb0615666`  
		Last Modified: Mon, 09 Mar 2026 19:05:38 GMT  
		Size: 24.5 KB (24465 bytes)  
		MIME: application/vnd.in-toto+json
