## `golang:tip-alpine3.20`

```console
$ docker pull golang@sha256:0aa6837f4cd9f308f981f68df1547c9c52b56dc716e2535d9d7cdd78cca0406f
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

### `golang:tip-alpine3.20` - linux; amd64

```console
$ docker pull golang@sha256:2465ecdcd6163fefe84744e7a134b1b3935806e3f55befb964cb8cc402e567f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.4 MB (131440701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f63fae562ce7011f5084d2776c834b6c4f887bbc6288b0bd2785a4b9676cd45a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77488b7789349a8292d6a15bdd15842bad86f3f3bfca8435f34cd89b61634c74`  
		Last Modified: Tue, 13 May 2025 19:17:04 GMT  
		Size: 294.4 KB (294397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a030b6acdb6db93394700b17a9f3cc951920ccdced1afb5118ff9ea25b238acd`  
		Last Modified: Tue, 13 May 2025 19:17:15 GMT  
		Size: 127.5 MB (127519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e802ee8b3b6753d12cf3755807949492c7320f216840c3c01589e09d508e3bd0`  
		Last Modified: Tue, 13 May 2025 19:17:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:71049fa2aecce4ca76b2ab8602d1f86187ff4f4d2fb58485909c8fd1d09d0e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (229987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce9c429e5e43194b6b53adc46a753141506552d92da1ffbe31879a0251ccd84`

```dockerfile
```

-	Layers:
	-	`sha256:0920e1ad8f3becb8c185c86aeef53c379c970d65492e425c8d51b05fd04e5b87`  
		Last Modified: Mon, 12 May 2025 19:15:25 GMT  
		Size: 205.5 KB (205475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463e1efd95b6ed45c5b6b75a4eded090b4ddf6bc4c651f4c8bbbe10e656ea264`  
		Last Modified: Mon, 12 May 2025 19:15:25 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v6

```console
$ docker pull golang@sha256:9d5f0b43947ea385563e5ca45b8d68f132637aec0c1e9d78d16f412ed27dfbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126476523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ad7237cca4c32e05b4732816de43b0b698a048bfddf7e6900aa20b2ebfaa81`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 19:26:24 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737183f74dc0d53c3f643812192622c6f3f2d83b37c68a4ca351085678413983`  
		Last Modified: Sat, 15 Feb 2025 00:23:02 GMT  
		Size: 295.8 KB (295833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4282a86be70f8e1a4d046254c770e7b2183496ad61e66fa1ae91c1abfd1471`  
		Last Modified: Mon, 12 May 2025 19:44:12 GMT  
		Size: 122.8 MB (122808002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6210a6a3e183f9b4b7fa86342d5b9ee6548bf65ed9afd26d18c65953018436`  
		Last Modified: Mon, 12 May 2025 19:46:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ac01a3e58a960fdabc1dc4c8acfd9e9240af5d14fd3e139b5367897939d08bd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 KB (24405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc981ea3a91db1441241e0e7573b82549da4b4437d75decd3d496c800c33f6e`

```dockerfile
```

-	Layers:
	-	`sha256:9dddb837fa181bb4a8f82ba23b87d7464efefcde6763b05c9f44bc7cd581d209`  
		Last Modified: Mon, 12 May 2025 19:46:45 GMT  
		Size: 24.4 KB (24405 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm variant v7

```console
$ docker pull golang@sha256:a14cd2a3f1bcd2c9477ece92fbce3940345c4e2b4439c92091dbf460039e246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125879537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b134bd75a79d86dc0ed976f2a1a140cfd0dfeb6fdc01fddbc21cf5ce2f6636`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 14:35:10 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d221261a6f80d203497a55ccecdc4912512b230fd036ba2df848b8144d67bf`  
		Last Modified: Sat, 15 Feb 2025 00:31:29 GMT  
		Size: 294.8 KB (294754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8433d2a5af6a5a0cd9e0774121856fe6f3adabe483560b233f2a94fde92edb03`  
		Last Modified: Mon, 12 May 2025 19:24:40 GMT  
		Size: 122.5 MB (122488656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22130fee15d0a233bf8c040c5b54d9679b908bfa939498736f4fd3c1a43cb68b`  
		Last Modified: Mon, 12 May 2025 19:40:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:e958ba29f080e73ade463b798e50a5be4a8fe7c2c160332fb0fa0da6c5c423c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 KB (230075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84cc1f5b88dfdb681eaa10497c947a64e14891c763f449972ba3ad29c8ceae3`

```dockerfile
```

-	Layers:
	-	`sha256:b304083d1014ec9238bbd8d1c987311e035933261e944377be95167c38cbdfda`  
		Last Modified: Mon, 12 May 2025 19:40:16 GMT  
		Size: 205.5 KB (205455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d2933a0f1628d0fb0ae8efb0c8adc85cc14405a651e905a83a7687227127d98`  
		Last Modified: Mon, 12 May 2025 19:40:16 GMT  
		Size: 24.6 KB (24620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2c040a8bdf9a557a5581b746eac658e46a6668e8ccdd9ac572debb255dd1ca07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124540518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce3640693af44534568f47d39d78bfa7595047b5362a1afe8e2e08a57a702d2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c56e8762dfc22e5eea28a95b136d7a0b7a8984a3a37a98c0dbc768604f0c31`  
		Last Modified: Thu, 08 May 2025 17:15:51 GMT  
		Size: 297.5 KB (297479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5330a97dbc92942ba37ce2bac7d5253897166c49acf8935c0dc87f91eec5803`  
		Last Modified: Mon, 12 May 2025 19:14:06 GMT  
		Size: 120.2 MB (120151716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4dc1363e2a7f02274bdd3037cd0208ff12268ff388a730b89cc9336132410c`  
		Last Modified: Mon, 12 May 2025 19:20:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:7427ce9ea188f47fc983d6820076f4d3d76bbf2120b96435ffb27904913e5fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 KB (230155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d45a720881949738de778f24d712888ea0c69c891d221646410bdb843a77540`

```dockerfile
```

-	Layers:
	-	`sha256:c094e7ce7327ed6024fdd06543e93eaea40e02c5055ae8a170182a3f2bdf821e`  
		Last Modified: Mon, 12 May 2025 19:20:17 GMT  
		Size: 205.5 KB (205507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ee0d9126e49ad59d8f90e53b2e11f46256ab891bec9ff30f433c1edcca65e57`  
		Last Modified: Mon, 12 May 2025 19:20:17 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; 386

```console
$ docker pull golang@sha256:dcb1ec629a5d932551e547258d0d6238c1a05447fb97073467bf58d02bcc6242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129418708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202c8f2c4073d9983f87b5f7eb2387381ba1f931882b69575097fecb908778a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 14:36:27 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286695f6dacea6b47f9b3f286dbab102bb97ea7277a45f7124062ec935ad8906`  
		Last Modified: Mon, 12 May 2025 19:16:00 GMT  
		Size: 295.1 KB (295149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d7e22db058c2c925ae80e0e254d251aaeb04c6161e3b31757924fb81096b47`  
		Last Modified: Mon, 12 May 2025 19:15:56 GMT  
		Size: 125.7 MB (125651733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b43aa3358e2be9390e7b3c81f0f450f8b65e913cb3f9fc2596d709de58df0c6`  
		Last Modified: Mon, 12 May 2025 19:16:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:ab3f60fc419b12ff8dce4e80a4a76be85fbc63340b7de42a4343f60f5480db3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7398657bab9b1f4783672896fe06bfc556e2fe9d54966fd0c0545bb386ea64a4`

```dockerfile
```

-	Layers:
	-	`sha256:575b3baff786746c1740bac96ab79ef3e2fb237cce9d9ae62829f7d8923a2649`  
		Last Modified: Mon, 12 May 2025 19:16:00 GMT  
		Size: 205.4 KB (205420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d6bb656df05266af10a6ca789cd5d7e83e396aa1ad6c38731618f4b6ec7b4b1`  
		Last Modified: Mon, 12 May 2025 19:16:00 GMT  
		Size: 24.5 KB (24479 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; ppc64le

```console
$ docker pull golang@sha256:2e4a31bfc68e2693fbf56f3799aa2801f17ef1e560275f8fbc2a6aebfee55ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126162810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f945ed361c933440b5943ca86c14736190430e2df0a21426ff85fb072d78dbf7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 14:35:49 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5ae44cb6a22e21c989dc7b540cce14809e91f5f477dfebbdc44d927ba36845`  
		Last Modified: Thu, 08 May 2025 23:17:55 GMT  
		Size: 297.9 KB (297900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ce9d7585ca139e17d7229c72e5e4b665cf0442ad17458746abe1ac1f1118c4`  
		Last Modified: Mon, 12 May 2025 19:15:34 GMT  
		Size: 122.3 MB (122289073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04461f121e9f9258d5f01f5dcba3170f0a08362e3663512757c41b08a1c777fe`  
		Last Modified: Mon, 12 May 2025 19:21:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:43ae1e3637633130393f4b072696c033e8b813e3d0e853972defa01b98eb48a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4621604e68c2648f837eee386976192ebff2bb7bc98667c517f207f7a1237f29`

```dockerfile
```

-	Layers:
	-	`sha256:28f715ba61df7098999d94700c5af1db2fd1fc59db5f9e41d2ec4b2e79de2dc4`  
		Last Modified: Mon, 12 May 2025 19:21:58 GMT  
		Size: 203.6 KB (203586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3dfb4246f33ce117cd405312b27d562c85a32c8eceb3d1bd90a5a7b7b66730`  
		Last Modified: Mon, 12 May 2025 19:21:58 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; riscv64

```console
$ docker pull golang@sha256:f5d28b1c3dc6308574e98a516a034550dac79070edee6edca6a1f944acaef748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126296234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759090d0fbbeedc5c5472d0d901438a363434a48f68dfd3ef38939819ba94167`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 19:30:36 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fa0de6a35b9467baeb7b28786dc580aa911bf02b2cc33ac7a44500327139a1`  
		Last Modified: Sun, 16 Feb 2025 09:31:09 GMT  
		Size: 295.4 KB (295446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6fb6b5563dabdad76b739d3338fefd5b6192bd70358c744c534995868ad289`  
		Last Modified: Mon, 12 May 2025 19:53:04 GMT  
		Size: 122.6 MB (122627399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e195e67ef10d3cf200bcab8974e902a2e65252979c8cc9cea138735a65c1c1fe`  
		Last Modified: Mon, 12 May 2025 20:30:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:32d63cb3a1245dc57aa28a6e76e63f69ab52c2c2398f6e680d6d18dc370fc699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.1 KB (228140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232a2acfefbd6c739dc0193027e30ff0858196b797589f131b6e6658d9080827`

```dockerfile
```

-	Layers:
	-	`sha256:11fbf5fa2149665d3e72d72279296ed6079b607b16a378e4db2c64d9019cd670`  
		Last Modified: Mon, 12 May 2025 20:30:20 GMT  
		Size: 203.6 KB (203582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7857f4067f7ecb22ab888116c7b2c834bb6696a5e6110154134dff920deade70`  
		Last Modified: Mon, 12 May 2025 20:30:20 GMT  
		Size: 24.6 KB (24558 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-alpine3.20` - linux; s390x

```console
$ docker pull golang@sha256:709c0d88774df5cbf219f17218df3014279315bd9635e255939915b9f594444b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128508634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65027cd673a324ce858117779039bff73a62cf6a7cb24173076c32b0edbd2c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Mon, 12 May 2025 05:23:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 14:36:22 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79aca9d4815f0afa30913ff64ea6ac6b14fb546971bdd999f2f73d3dc79f0ba`  
		Last Modified: Mon, 05 May 2025 17:58:58 GMT  
		Size: 295.7 KB (295711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f6707b6ea1615397f3ca5bfff811b917ce5218f2246275a6ac50ada31e70be`  
		Last Modified: Mon, 12 May 2025 19:16:07 GMT  
		Size: 124.7 MB (124748643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537ccff8f619f716301b55f4976f35ec3e312d46a442a52518da37dd2dbe55ce`  
		Last Modified: Mon, 12 May 2025 19:21:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-alpine3.20` - unknown; unknown

```console
$ docker pull golang@sha256:692b7f81891393853a714d5df85d54357ca7eb2560ba4a14f475148526331038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 KB (228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b38388ba43b0fdd227a9674611f2f6a2ad0ac3de2bdb6f23cd33bac281cd2bcf`

```dockerfile
```

-	Layers:
	-	`sha256:b22dc442ed7e03987e8195026ef4454fe0827138de861efb6ee4c32643ff4f1b`  
		Last Modified: Mon, 12 May 2025 19:21:58 GMT  
		Size: 203.5 KB (203524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:972da5a13d8d792c66592bf71dc643ea3548209b438e7793257f1eaf298d985b`  
		Last Modified: Mon, 12 May 2025 19:21:58 GMT  
		Size: 24.5 KB (24512 bytes)  
		MIME: application/vnd.in-toto+json
