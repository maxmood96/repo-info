## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:8e8c654d5c05f664aa393a4cef6e840fcaea9d19c50f40d6a356c3d2616e7c50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `caddy:builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:71489de3bf6fbe5714a1ec1bacfa46121a16b9b7d72ebdfdbce4c73627a01c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79708742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd012b780204a531a72bb0bdff6b3b810cb50e05df244bf571d03399bac74c88`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:58:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 19:59:02 GMT
ENV GOLANG_VERSION=1.26.4
# Mon, 22 Jun 2026 19:59:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 19:59:02 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 19:59:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:59:02 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 19:59:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 19:59:05 GMT
WORKDIR /go
# Mon, 22 Jun 2026 20:24:29 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 22 Jun 2026 20:24:29 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 22 Jun 2026 20:24:29 GMT
ENV CADDY_VERSION=v2.11.4
# Mon, 22 Jun 2026 20:24:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 22 Jun 2026 20:24:29 GMT
ENV XCADDY_SETCAP=1
# Mon, 22 Jun 2026 20:24:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 22 Jun 2026 20:24:29 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 22 Jun 2026 20:24:29 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d063e9d63c5a9a316f84e2d0798be3f07a77b0903f4cb5441b41b0cb450e3f`  
		Last Modified: Mon, 22 Jun 2026 19:58:49 GMT  
		Size: 245.1 KB (245055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b813cdff7bee934633b69a58dbbc0547bff724a8e7b9691ba01920fd2d29a598`  
		Last Modified: Mon, 22 Jun 2026 19:59:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8d11f6203fff083bbc13a81361941dac2c7263baf664996a58ff3fce2507c9`  
		Last Modified: Mon, 22 Jun 2026 20:24:37 GMT  
		Size: 6.5 MB (6489141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5705af9dfe517a4993d3827c7bfeaf406e79f2bcccc31322799ae13d55f644de`  
		Last Modified: Mon, 22 Jun 2026 20:24:37 GMT  
		Size: 1.8 MB (1846503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e91fb3ff6cf54c3a6adc9dbd4d7f397de42fa0ccae083bd33a430f085f8e34e`  
		Last Modified: Mon, 22 Jun 2026 20:24:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b6213601ab9aa8a325963b66fdbed63eb5a407dec59c4658c51531e6ed091cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.0 KB (284013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6411e76c323076042175451629930c65236dc91ec2feafa180b33a6f741ab2`

```dockerfile
```

-	Layers:
	-	`sha256:94960e823d831fc3402d39b1e5193757b6106884044e8ffef091623e0cb2ac08`  
		Last Modified: Mon, 22 Jun 2026 20:24:37 GMT  
		Size: 263.9 KB (263884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf930cb191be5f2cbac1ffaa71b8cc2bb2c8bdb9096618f1a0cae02133559fb`  
		Last Modified: Mon, 22 Jun 2026 20:24:37 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:38923accfdd0ba30e5f8a887d1a4bbf50d1247a3442c846f1d639dc8422bf41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77736682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ec65efc886ed8c1e2a5009f29789227c09f72f4e5d6cd9c69859e2e164a455`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 19:55:09 GMT
ENV GOLANG_VERSION=1.26.4
# Mon, 22 Jun 2026 19:55:09 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 19:55:09 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 19:55:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 19:55:09 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 19:55:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 19:55:12 GMT
WORKDIR /go
# Mon, 22 Jun 2026 20:36:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 22 Jun 2026 20:36:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 22 Jun 2026 20:36:27 GMT
ENV CADDY_VERSION=v2.11.4
# Mon, 22 Jun 2026 20:36:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 22 Jun 2026 20:36:27 GMT
ENV XCADDY_SETCAP=1
# Mon, 22 Jun 2026 20:36:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 22 Jun 2026 20:36:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 22 Jun 2026 20:36:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0eb0fd8125cf2b8af4b0ab223d6707fc99c28bcb83ad941214fda6cc501c1d`  
		Last Modified: Mon, 22 Jun 2026 19:55:23 GMT  
		Size: 246.1 KB (246139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ec3a75ac452d0582a4ae366cc169f4a366463bbb26a27606587c25124fac70`  
		Last Modified: Mon, 22 Jun 2026 19:55:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a14c8c4e9005c99ffe1cd176904241c63a6bce348d4dbbddb7c70d50c80e41d`  
		Last Modified: Mon, 22 Jun 2026 20:36:31 GMT  
		Size: 6.4 MB (6406407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71744ac3a240d51cb7113f0e938126021bbd85d7612cdce3db0f2f2de93d07ee`  
		Last Modified: Mon, 22 Jun 2026 20:36:31 GMT  
		Size: 1.7 MB (1744998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f5cfffb7b0aa2b2d97d9bc6788267ff36c6416511742a4d658dc743ef01fd7`  
		Last Modified: Mon, 22 Jun 2026 20:36:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:00691b340467d435bc2b31e05873a8a7fce6f66e8977a463a00d788fc00dbcba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21482e8686fd355010c294ffaaeff22f5edf415913e5c237b6dd7afe367fc40`

```dockerfile
```

-	Layers:
	-	`sha256:d51ce3396bf78b151836d509d97bcce1d0ce9e9ba7a51dba3487443e9c1600b7`  
		Last Modified: Mon, 22 Jun 2026 20:36:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:741efdc7e420ce64f045ff245cbb60608ce55f98b9f48e17d3439a049414ba2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76891947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32558a9c4831ad0d4628eb9b1a912c720b51c8494953906b85a201b8f82d0202`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:18 GMT
ADD alpine-minirootfs-3.23.5-armv7.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:18 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:09:14 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 20:09:23 GMT
ENV GOLANG_VERSION=1.26.4
# Mon, 22 Jun 2026 20:09:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 20:09:23 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 20:09:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:09:23 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 20:09:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 20:09:25 GMT
WORKDIR /go
# Mon, 22 Jun 2026 20:51:22 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 22 Jun 2026 20:51:22 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 22 Jun 2026 20:51:22 GMT
ENV CADDY_VERSION=v2.11.4
# Mon, 22 Jun 2026 20:51:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 22 Jun 2026 20:51:22 GMT
ENV XCADDY_SETCAP=1
# Mon, 22 Jun 2026 20:51:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 22 Jun 2026 20:51:22 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 22 Jun 2026 20:51:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:177f8e1e6f831989320cf2b59b7eabd21cbf36804c79506912f3a81caff426f2`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09e1a554df7e294fd0dba441c970cb7536650f8c6d464de4a0afeecfa4d4ff2`  
		Last Modified: Mon, 22 Jun 2026 20:09:40 GMT  
		Size: 245.1 KB (245120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7513b5f147f33fb6ccf00097d7d82d45382d3837232b4c9224c1268840362c3`  
		Last Modified: Mon, 22 Jun 2026 20:09:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edb95be02eeaec011063fcb8dff0691ef110dd3e7b3dfb7f9600cc4c69536e4`  
		Last Modified: Mon, 22 Jun 2026 20:51:30 GMT  
		Size: 5.9 MB (5859500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0396eb2c5753e9a2933685b879cec1ab47dfd0666d90da2204219e5de1540ac7`  
		Last Modified: Mon, 22 Jun 2026 20:51:30 GMT  
		Size: 1.7 MB (1738757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f2bda3bdeee0cf6452e515aa08eb41c559a7d0748428dde33944f698f90a13`  
		Last Modified: Mon, 22 Jun 2026 20:51:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3f79c0d860e2b3b37eac1edb1562e11ba44a122f3bbebdf22243a776539fc531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 KB (286530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c97e39fc54a07c1accf4d87b592b2612a095a24a6bc4d546c5182d9dcd86c1`

```dockerfile
```

-	Layers:
	-	`sha256:25109dc1925cd706ce929758cfbfe9477c73f0d818efddccf07443fbdafe6f4d`  
		Last Modified: Mon, 22 Jun 2026 20:51:30 GMT  
		Size: 266.3 KB (266276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1de7d9e5eaf4e759b81fd6c9cd09088879bf81a79368c4e3c6a63267afede7fa`  
		Last Modified: Mon, 22 Jun 2026 20:51:30 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:aa26e9dd596539026002cfc92cfc667a561c2ed48c0d035ea5695c7f33cab0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76887738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7385be1c2ec7af592102519ef84a218ae47ffc9fac7aecf3241a67255f7f847`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:06 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 20:01:01 GMT
ENV GOLANG_VERSION=1.26.4
# Mon, 22 Jun 2026 20:01:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 20:01:01 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 20:01:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:01:01 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 20:01:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 20:01:04 GMT
WORKDIR /go
# Mon, 22 Jun 2026 20:58:31 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 22 Jun 2026 20:58:31 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 22 Jun 2026 20:58:31 GMT
ENV CADDY_VERSION=v2.11.4
# Mon, 22 Jun 2026 20:58:31 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 22 Jun 2026 20:58:31 GMT
ENV XCADDY_SETCAP=1
# Mon, 22 Jun 2026 20:58:31 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 22 Jun 2026 20:58:31 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 22 Jun 2026 20:58:31 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b7518a8a2c3c1bed624e92a35486bb1e8285483cbf07acacca0055e663b88a`  
		Last Modified: Mon, 22 Jun 2026 19:54:17 GMT  
		Size: 247.5 KB (247486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3bb8322ea6de6e6d4347f858a75e201d9252ab274018c73a97cb97dfa7238b`  
		Last Modified: Mon, 22 Jun 2026 20:01:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54152cfdc94e44dce57368173646d9231e39bd5e0efde34a8ed071d616a3e355`  
		Last Modified: Mon, 22 Jun 2026 20:58:39 GMT  
		Size: 6.6 MB (6574449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4291f4d0b93ef13edba300cea0203289dc4ade8abec6f5922a78a0c1194d3ad`  
		Last Modified: Mon, 22 Jun 2026 20:58:39 GMT  
		Size: 1.7 MB (1716380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79df9948d49ef538f7064e233c2d90722a972a2c778c38af51ffe2ed2fd218ad`  
		Last Modified: Mon, 22 Jun 2026 20:58:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:4f9f7538e119383c779af0c08d047e53ada45fec71d9aeaa8148d665d89c60bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 KB (283634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2460629e28cd8e4ac39a2e97350da9ac411acfd3aa000ac085c80a412d2b6403`

```dockerfile
```

-	Layers:
	-	`sha256:034c82189af86fdf411493e753882dc1f7ee50e3af157b936bcc92eb44452eac`  
		Last Modified: Mon, 22 Jun 2026 20:58:38 GMT  
		Size: 263.3 KB (263338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c51feba190eb8d0b526718762eaff49c228732263b464092be9f1290a31831`  
		Last Modified: Mon, 22 Jun 2026 20:58:38 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:0b3868ec18074a3f9d3a62f3644cba9b7d239ada3cc1cf19fda7240153093b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77513077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac9e1fa25f776d5e0c4cd8873e0242bec22565a651502f7903557a43b31ad94`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:21 GMT
ADD alpine-minirootfs-3.23.5-ppc64le.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:49:25 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:42:40 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:42:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:42:40 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 20:58:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 20:58:29 GMT
WORKDIR /go
# Mon, 22 Jun 2026 22:07:51 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 22 Jun 2026 22:07:52 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 22 Jun 2026 22:07:52 GMT
ENV CADDY_VERSION=v2.11.4
# Mon, 22 Jun 2026 22:07:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 22 Jun 2026 22:07:52 GMT
ENV XCADDY_SETCAP=1
# Mon, 22 Jun 2026 22:07:52 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 22 Jun 2026 22:07:52 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 22 Jun 2026 22:07:52 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8593c4b2127f4c903557fc9d975d78f121957a1e927c866a1c54d29f11b3ba76`  
		Last Modified: Mon, 22 Jun 2026 12:03:30 GMT  
		Size: 3.8 MB (3812299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2afe4ddf70535a87895dd2928115f13eed6bd80bb630863f6b224ede37a652`  
		Last Modified: Mon, 22 Jun 2026 20:49:43 GMT  
		Size: 247.9 KB (247906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29e9f384b63bdee3470b1afb6bf0229c9990ca6917431da96ac2583d1aa8896`  
		Last Modified: Mon, 22 Jun 2026 20:58:49 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20dd6c03aea79ffe47f1f9a9bae5e84119f9e216181e37abc2463033acf121bf`  
		Last Modified: Mon, 22 Jun 2026 22:08:08 GMT  
		Size: 6.9 MB (6905735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde1994e2b3164ba591475bb5fc2820819ec6395efa24e5101d305ea27963d48`  
		Last Modified: Mon, 22 Jun 2026 22:08:08 GMT  
		Size: 1.7 MB (1705995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8928b7c88e2770ffa61b11b1ec3c431660a45c285b9540c96ee394b45720ba`  
		Last Modified: Mon, 22 Jun 2026 22:08:07 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:db486bf76b91d61f13bab8a23ba688ca56bd131a7fdc571a08e6f4a869ee2cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 KB (283505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35ed24381e2673db4be3cb3d177d9c7d79a7b36881e46980f1e24e035c977bf`

```dockerfile
```

-	Layers:
	-	`sha256:82a932dd5b24164dafa9469be60a1ecfce38dc3d44f5e79469ac54417ea00360`  
		Last Modified: Mon, 22 Jun 2026 22:08:07 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:312e04c23ccf325f315336a6a43f00d8a23aad5e678e48f12e3e716bdf55fe28`  
		Last Modified: Mon, 22 Jun 2026 22:08:07 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:502a607a6afd084aa35aa29bf43e16794a7c9ade70f92d6653d7bea5fc1d36ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6c50594ae8b5f92626b6657447b607d1d521516fac1547542c7e2c2d4b75d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 23:12:42 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 23:12:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 23:12:42 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 23:21:02 GMT
WORKDIR /go
# Wed, 03 Jun 2026 05:24:30 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Thu, 04 Jun 2026 03:37:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 04 Jun 2026 03:37:16 GMT
ENV CADDY_VERSION=v2.11.4
# Thu, 04 Jun 2026 03:37:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 04 Jun 2026 03:37:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 04 Jun 2026 03:37:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 04 Jun 2026 03:37:17 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 04 Jun 2026 03:37:17 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3257359d78e33ee12c186b4248dac6627cb8e26d6fd747ad8f46ed2b4fb8e1`  
		Last Modified: Thu, 16 Apr 2026 16:19:53 GMT  
		Size: 290.6 KB (290553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8f135b9aec9b42cabcdbc9e60e1e2b738fe71cb50c44dd091c53fb8edc94a`  
		Last Modified: Tue, 02 Jun 2026 23:19:15 GMT  
		Size: 65.1 MB (65148394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309c4848fcf3e91f4413c1666bace4337c4f1c12c50976959bd29ad011c4d936`  
		Last Modified: Tue, 02 Jun 2026 23:22:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc28d768f2c71e4a402e2f4424963bfaa465d9c4a2f36c428bd41b08e3d6d2d`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 6.7 MB (6672809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39085496bc301b93c742105c53cdd6eb9c25b9f670b3eab37958f1b91c1de822`  
		Last Modified: Thu, 04 Jun 2026 03:38:04 GMT  
		Size: 1.7 MB (1724226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c009078033432c6db2dc48122c2e06cee86f36595d3838bddf2c9434667e8f4`  
		Last Modified: Thu, 04 Jun 2026 03:38:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e39f14273e77a6ee7649fcda64356b3149c9dbe8cf678a0f721f79a330b292da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1271c286280908c181b1c025432ea4c3e2c91c2eeeeb5a5fc235ef45f3181364`

```dockerfile
```

-	Layers:
	-	`sha256:e0878bda489fe21abd909c0ec0186f7b7e32b126803f669c602372923e74269e`  
		Last Modified: Thu, 04 Jun 2026 03:38:04 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8263240805cf9d694953330ceaa8df2a156b379cc72fd9d96df5a51067e691d8`  
		Last Modified: Thu, 04 Jun 2026 03:38:03 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:d001bf2ef83a64b9ba5eab3cb176ab3fe0494e50d0f6987074c7d07603b3e637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (79030245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d56adf617a7c5f27a2b4b546f004991ecb406e78d06e2926cb213e470000cc0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:13 GMT
ADD alpine-minirootfs-3.23.5-s390x.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:13 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:10:55 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 22 Jun 2026 20:15:54 GMT
ENV GOLANG_VERSION=1.26.4
# Mon, 22 Jun 2026 20:15:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 20:15:54 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 20:15:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:15:54 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 20:15:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 20:15:56 GMT
WORKDIR /go
# Mon, 22 Jun 2026 21:52:33 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Mon, 22 Jun 2026 21:52:33 GMT
ENV XCADDY_VERSION=v0.4.5
# Mon, 22 Jun 2026 21:52:33 GMT
ENV CADDY_VERSION=v2.11.4
# Mon, 22 Jun 2026 21:52:33 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 22 Jun 2026 21:52:33 GMT
ENV XCADDY_SETCAP=1
# Mon, 22 Jun 2026 21:52:33 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 22 Jun 2026 21:52:33 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 22 Jun 2026 21:52:33 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e7ed98545f58cf5b2daa8ddc132c859b15cb780cb2ee2246e28415eaba3d63c8`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.7 MB (3707249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470176434bca20b0199baf086b0e5f5cba5a0bee165b8e1094c1885f4df27c81`  
		Last Modified: Mon, 22 Jun 2026 20:11:11 GMT  
		Size: 246.1 KB (246139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ebdacc8a1b421e6eafe70203b300549326cedd77a6612ccc0d95baeff917f4`  
		Last Modified: Mon, 22 Jun 2026 20:16:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff36093e8d0838c0387f4ecfe19235a7f30ac0c94de7d1905c2a4f22c21a60dd`  
		Last Modified: Mon, 22 Jun 2026 21:52:45 GMT  
		Size: 6.8 MB (6779587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8f0dabf6980de5e276c5e47295b5c271e18d5627408c4b9ea4edfde8b11815`  
		Last Modified: Mon, 22 Jun 2026 21:52:45 GMT  
		Size: 1.8 MB (1782856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363f575700ecb7cdfd69d1ca29f41d1aefcf18e8c1894e5015cf29f61ee39fc4`  
		Last Modified: Mon, 22 Jun 2026 21:52:45 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ff665d04da1a4de54d3eab0ec6fff5fc726103214ab3ba02b36f40b2c0f5619e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 KB (283362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c62e337f5dccc2004fa330356d4c2bdca35b04e066ae951208be06936be6d01`

```dockerfile
```

-	Layers:
	-	`sha256:3886ec70c30d06e7a379f105bef4e15fbd12e0ec82bdd1630149fd2718ab8d63`  
		Last Modified: Mon, 22 Jun 2026 21:52:45 GMT  
		Size: 263.2 KB (263233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7f736d138b1d832fa22c71bab90b7b4cdbcd27d16b49968dfde94d44b5b13d6`  
		Last Modified: Mon, 22 Jun 2026 21:52:45 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json
