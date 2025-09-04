## `caddy:2-builder`

```console
$ docker pull caddy@sha256:3c711fcf9a64d31e8927a2efb538cf99e6f758f737aadcde5fd7dfadc93287a8
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:e9307b3c84ee81547edcdd3c410a6e4619febd1fd0e52c70703c864b1531f59b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72186128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b162328aa7169c134ebb2c22d4ed3e1a2a27758fe016d98ddaeffc8c699874`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e451c10b31532d8616ff155adb8383bcfe95b7388ad69363af6512986430f9`  
		Last Modified: Wed, 03 Sep 2025 18:49:01 GMT  
		Size: 282.4 KB (282439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330457f0054be4c07fbaeac90483ac4f534113ccd944fe16beb9e079a3ab3a36`  
		Last Modified: Wed, 03 Sep 2025 18:49:05 GMT  
		Size: 60.0 MB (60045609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47af78ce4e7644116937dd73c4624dd335cedafdcfbb998d89e8c4d7c652854`  
		Last Modified: Wed, 03 Sep 2025 18:49:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb8baf6d509358fd3b8528ab977b19d67244054abae2c1d4a6d2108c7ff423d`  
		Last Modified: Wed, 03 Sep 2025 19:04:50 GMT  
		Size: 6.2 MB (6211297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7027281b0f60a8c0f26ec2aefd033c6363d8ca95db0875ecf2c8b2b6e428604e`  
		Last Modified: Wed, 03 Sep 2025 19:04:47 GMT  
		Size: 1.8 MB (1846502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ced54791a1656fc651d2bc1b1bed917de1e6214e5dad06b0bd08e8bbd661e74`  
		Last Modified: Wed, 03 Sep 2025 19:04:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3d6434eab855e7550a0a16935ffe9278cd98c81850e91643e32e941a8a741d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 KB (296914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d815305762e587b7c0a1e94d92afd35c115946430bf5c80c6c774a759e28f681`

```dockerfile
```

-	Layers:
	-	`sha256:5ed2541599af0981e6d501146f6c9f51e266075fcca30154cf5986f6e4f03cae`  
		Last Modified: Wed, 03 Sep 2025 21:52:43 GMT  
		Size: 276.8 KB (276799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f1a536e6e92a2db8d0fbfa0798019d3f11b3d43074a76ca06eeb23aac3fc5d6`  
		Last Modified: Wed, 03 Sep 2025 21:52:45 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3a565290b03a1aa1313eefe894100e6d5404dfb8fef96cbd0172ded1ac7d7d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70632273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d0d04b8d168a220ae2484b77856a85d8f1642d6c71de5740d3a5cd9d3a5b57`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95cea4c439fb384d1bd6927f75cd3bde82d7a5909bb38cec72c9923ca463a`  
		Last Modified: Tue, 15 Jul 2025 22:55:40 GMT  
		Size: 283.3 KB (283329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a44638bfcc9a284518c23ffdd9987c08149ae934bfdc646c64661f53945d956`  
		Last Modified: Wed, 03 Sep 2025 18:48:34 GMT  
		Size: 59.0 MB (58978196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4631275be0b0e97c3cbcc9d86f045fb292508dc13ce4dce1e2653b9ba1d4bfb`  
		Last Modified: Wed, 03 Sep 2025 18:48:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314bb5bc0fbd277a0ef297ffb152b030cdb61cd2c8d07ea357a82f5bdc1ffe39`  
		Last Modified: Wed, 03 Sep 2025 19:10:59 GMT  
		Size: 6.1 MB (6124248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea28770f17e79318c638a67d2d34789cc4f246202b6ec756cc192948a6fb8f00`  
		Last Modified: Wed, 03 Sep 2025 19:11:01 GMT  
		Size: 1.7 MB (1744998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bbc7c14662d7372a4c3f10ca1f9b8c3a4e453b6b097d682ab20155182504bc`  
		Last Modified: Wed, 03 Sep 2025 19:11:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:2256c145bc644d1e45bd39cd48665cba245b5a74d08362555b1c6b73db9c87a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b724eca9a72ad8e4578431091350ab28b843cac59ac52cb8b1269ab7397f5402`

```dockerfile
```

-	Layers:
	-	`sha256:a5450dcb80fa06d1f6c7846cb59b31cc7007f3daff965a076382b356b1842858`  
		Last Modified: Wed, 03 Sep 2025 21:52:48 GMT  
		Size: 20.0 KB (20021 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:d2b87ac7bde0ec1205ec5c26aa2f6717dcd71503dfab6de7be742d2a3f8d0d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69822487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54beed9f43f8b43a08a5045b17de96a9e6fcc05fbfd0f2564bc1d4e0c29c52e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
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
	-	`sha256:ec999c8e928607a0bc4da54080226a6c247c744815a64f6c10bf38b015958ebf`  
		Last Modified: Wed, 03 Sep 2025 19:08:36 GMT  
		Size: 59.0 MB (58978176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588ecf6b5dcc843c1c6a16f9c6243ed7412f88950d57d90fd50cd05e0a125b21`  
		Last Modified: Wed, 03 Sep 2025 18:50:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9acda26afbe1e05cf70daa41184b9d5cf0bc2fd9107754c95637a67b0bec77`  
		Last Modified: Wed, 03 Sep 2025 19:16:50 GMT  
		Size: 5.6 MB (5603440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590efba8c0f0a81da58bd2a49200f5e177c8074b09f152d8ef562a228dfedb2f`  
		Last Modified: Wed, 03 Sep 2025 19:16:49 GMT  
		Size: 1.7 MB (1738757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c40bb68466ac65d34122d4bf15962d7a37c42c2b9cb4ce60186614a6349a62`  
		Last Modified: Wed, 03 Sep 2025 19:16:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:14dedff55ddb0787ac998e099cfd99490ac7cd54b83e7b4d301dc405ece8c3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 KB (300079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fb9d5ce69f985011d10c0a9d5d1c09b5c68931e99e566848b5948cdfdf5e76`

```dockerfile
```

-	Layers:
	-	`sha256:13950bf3a67e466f5c61cb569e0127d2bf632f8d55758a0da26137893e03ba60`  
		Last Modified: Wed, 03 Sep 2025 21:52:51 GMT  
		Size: 279.8 KB (279843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a10259db06c4b6bd8b83c6de786a09960a849de441b5dc4736c342ce6bf04f9`  
		Last Modified: Wed, 03 Sep 2025 21:52:52 GMT  
		Size: 20.2 KB (20236 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:519aa0f730b7e932bdced7e59143a4e6d597f89c323d0f205eda3ec79ab8aab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69951460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc15f95831b3a07979eed691b509255794d3818b6474e9784d696d22c3d3342`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
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
	-	`sha256:4681030a890db37290ab2fddf45adb75dbd1fbf983ba1b16efefb7221b97b1ec`  
		Last Modified: Wed, 03 Sep 2025 18:48:35 GMT  
		Size: 57.6 MB (57555480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1263033b96d9290f4969661ad0abb50c064aa016a442c57ef7309a1372f7ce`  
		Last Modified: Wed, 03 Sep 2025 18:55:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256bb7b272288a70777004e010f2a89ccf4c8d96c8abb300e846ce14b25d5c45`  
		Last Modified: Wed, 03 Sep 2025 19:19:47 GMT  
		Size: 6.3 MB (6263550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2744703386da93bd4a9b6951a9f05baa0491827c1399f2cee03513eb9a62802`  
		Last Modified: Wed, 03 Sep 2025 19:19:47 GMT  
		Size: 1.7 MB (1716383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06054ab71586c4e70318817c20053b76fa881d1178cd217f9957549e3f64d883`  
		Last Modified: Wed, 03 Sep 2025 19:19:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a3b9b0660c1f01848483c868c5c73f36a30501492dbdc4c892f2b4d8f892ecb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.2 KB (297185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6735c1f609dc6e5b923354b515d9ccd5912a1fa3d9132de980007bc63d86969a`

```dockerfile
```

-	Layers:
	-	`sha256:2086c9e3036859c82c900f216616b304f9c4c0b028c2faa92fcb08214f1383ba`  
		Last Modified: Wed, 03 Sep 2025 21:52:56 GMT  
		Size: 276.9 KB (276903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04836afa19489a9b46c3a6095dfed123a3a3193f8c50fa781ebd637126a0476b`  
		Last Modified: Wed, 03 Sep 2025 21:52:57 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:18f6e23e9937fee2c5efc047b2710333c5a1a2dec17a0c6691c9a93bae18c8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70305772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d32b2422bdd49103b386c4bd34fb4705b3adf92112e7c7dfd3cb7e32cce54f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
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
	-	`sha256:9295eaa21ceb778d7859c40f41ccdf7cdeffaaa99a56ac388f747e3eb72308f3`  
		Last Modified: Wed, 03 Sep 2025 18:50:02 GMT  
		Size: 58.0 MB (58036165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01c481c7763c179c2e7a07ee1c506a1b64587a0dd8c90777578db6698e870bb`  
		Last Modified: Wed, 03 Sep 2025 18:51:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ee195a54aab5a7a72f7367ec3a8022797b427809e3f6fc9712f218920b4ede`  
		Last Modified: Wed, 03 Sep 2025 19:19:17 GMT  
		Size: 6.6 MB (6550790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0641511d93182f8d23d572d3e1ec7258bdcbc1839d225ca1ff4f4ef5183678f0`  
		Last Modified: Wed, 03 Sep 2025 19:19:17 GMT  
		Size: 1.7 MB (1705995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994ae162ac70682ba8fd3095abd61e90c8d46a93ad122a87fdbf44e4ce8bea8`  
		Last Modified: Wed, 03 Sep 2025 19:19:17 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:7babcec06e587e5524608ab53617eadfdebe01fb5b8e6f5bd069e0b9e1f02039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442424dbf29d0e38fa065c5a2fc9e3be728ac326c4774b8d5220f264ff799ecb`

```dockerfile
```

-	Layers:
	-	`sha256:3bc8af133f45eba46cdae3fd28e0a91e7898ea1e698489731eb503aac0e78cbc`  
		Last Modified: Wed, 03 Sep 2025 21:53:00 GMT  
		Size: 274.9 KB (274920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46a4fa0c341c9282ddd6583f21eab30d89909b7ed806de17fc1924b4ae046431`  
		Last Modified: Wed, 03 Sep 2025 21:53:01 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:adbd91bb32fe943585ce6f301f3a25f9b0da2ea80b489cc2af45356b82025921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70464823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe13fd1d2ea3fc5551c50b7d9190bb0e9d662f7c6df070f7a176f9d6f6f9cf9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 22:46:39 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOLANG_VERSION=1.25.0
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 Aug 2025 22:46:39 GMT
ENV GOPATH=/go
# Tue, 12 Aug 2025 22:46:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 22:46:39 GMT
COPY /target/ / # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 Aug 2025 22:46:39 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
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
	-	`sha256:b8818a250444a855ca5b23afc25325ec1add801f7bb83153c967335fb20cce8c`  
		Last Modified: Sun, 17 Aug 2025 10:47:36 GMT  
		Size: 58.6 MB (58570045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa73a00a8f5fcc1c6a012f631aad24947f80e562087eaca0a51207300fd3461`  
		Last Modified: Sun, 17 Aug 2025 10:47:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa6e6611bfc95880cdb9a6ec68b7e7f5dae83d74b35fba3bccdbb6d8cedb4c5`  
		Last Modified: Wed, 27 Aug 2025 08:51:52 GMT  
		Size: 6.4 MB (6374400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc90d4fb95a13bd99cf2988eb82ea4d84ccef11b2c0e544cbc8ed8cbd8885d`  
		Last Modified: Wed, 27 Aug 2025 08:51:53 GMT  
		Size: 1.7 MB (1724206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c2e5bf079f2342f0aaee4179928bd37596b777d8f0686112ff197d45eef04f`  
		Last Modified: Wed, 27 Aug 2025 08:51:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:c363037f46ed49b3e930627f31b8829e532b5ed80dc7e363a830467cbb808ac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f7e1b5e063d7f3d027b4c2b5c26db812184c4a67d03d70805a18d9515373351`

```dockerfile
```

-	Layers:
	-	`sha256:11f952b1ab032d2f623a7f4ff3adaaf5860a409fbd08fcfbcda701a2d604c6f4`  
		Last Modified: Wed, 27 Aug 2025 09:52:38 GMT  
		Size: 274.9 KB (274916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a764d37e5c7dc8d97d989bb5feaf5a87ddb8560f5b45c8e12d817dfdd498b036`  
		Last Modified: Wed, 27 Aug 2025 09:52:39 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:1dd4a4f755b330dd984933e049d7d96d6e7b9072043f33d4e6236a3c05b4f68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71592127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bdcc89c465fff8a25646af206f7399350b35f56c698df02c4568fdc0b4d9f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOTOOLCHAIN=local
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOPATH=/go
# Sat, 23 Aug 2025 03:19:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Aug 2025 03:19:59 GMT
COPY /target/ / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /go
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 23 Aug 2025 03:19:59 GMT
ENV CADDY_VERSION=v2.10.2
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 23 Aug 2025 03:19:59 GMT
ENV XCADDY_SETCAP=1
# Sat, 23 Aug 2025 03:19:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
WORKDIR /usr/bin
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
	-	`sha256:6af48389d563ccb39441056114ee8bb4fefdded621ed594eb028cdf9787ad997`  
		Last Modified: Wed, 03 Sep 2025 20:23:25 GMT  
		Size: 59.4 MB (59378188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a182d4ee22ff61422f6f3ab1d522915b82804bce4757474e672d4f4503a7a14c`  
		Last Modified: Wed, 03 Sep 2025 21:11:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4adfac2a3c51fd371fa5ca17ce44724a52eb91e314c8507f73b1d779f53ae`  
		Last Modified: Wed, 03 Sep 2025 22:11:14 GMT  
		Size: 6.5 MB (6502063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962afaf68132bdc3a14219a3f45934f92f93b41f626e750a81526d69486cc5a6`  
		Last Modified: Wed, 03 Sep 2025 22:11:16 GMT  
		Size: 1.8 MB (1782840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d568976339b270481956fc44f9f92309945cdf55667f600453f2c6eb9573e8a4`  
		Last Modified: Wed, 03 Sep 2025 22:11:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a94a3e3157c0c0f946d02ec00e4b74f7663ddca01c03451ce3ce2a8f632a46b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 KB (294963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65d7e717a6b85cac95cfc9bab6e31e9be15accd9ba70fa0f0432b91287e11d7`

```dockerfile
```

-	Layers:
	-	`sha256:61f94969eccbec88ce5ef68e169a45cdc1d0ca391566965a0275fa14a14f76c7`  
		Last Modified: Thu, 04 Sep 2025 00:52:34 GMT  
		Size: 274.8 KB (274848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ecf7bd5fd90b5829276516a327a8b77498a5c5616aeeae82158214c386f19a2`  
		Last Modified: Thu, 04 Sep 2025 00:52:35 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:37ed736284e56457e89c30926c1257594d397979614fa28e29e51899c27ed628
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615337218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71482ccb5d5af02699b97417cfd4f52c3c33539b15ef2c581fb7e935f781901a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 03 Sep 2025 18:54:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 18:54:11 GMT
ENV GIT_VERSION=2.48.1
# Wed, 03 Sep 2025 18:54:12 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 03 Sep 2025 18:54:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 03 Sep 2025 18:54:14 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 03 Sep 2025 18:54:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:54:32 GMT
ENV GOPATH=C:\go
# Wed, 03 Sep 2025 18:54:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Sep 2025 18:54:41 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:56:23 GMT
RUN $url = 'https://dl.google.com/go/go1.25.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4a974de310e7ee1d523d2fcedb114ba5fa75408c98eb3652023e55ccf3fa7cab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:56:24 GMT
WORKDIR C:\go
# Wed, 03 Sep 2025 19:11:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 19:11:13 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Sep 2025 19:11:15 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 03 Sep 2025 19:11:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Sep 2025 19:11:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Sep 2025 19:11:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f495bbd35ca8371e7ec2ae6c370e5682cb4115fab536c9282a01229768afc4`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43216771afdda44565d262c41cb4e449d6be29edd33e3e8bb55360a9da328d53`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a19e361e0b9d583cb99cba5f0bc5e433894e70eb6bcfd03408daa7e0513885`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc3cdf339cc1b15f23e17648fb50e6dfa0a82edee34b12a0edc43f3304b8f8c`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59f12ead65b3b97d30afe4e69cd209e7eb29dadd77a965d9616f7e60f3ccab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1920035ea1acffe071d8a1a6e540cbc05a2227b03f219f5f60cfeea15d4f5a2`  
		Last Modified: Wed, 03 Sep 2025 18:59:55 GMT  
		Size: 51.3 MB (51255221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6209f159116204b114dc0a4ee1f3c7ab824b77eeb134fa89a6c4db43f33457ab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520317e2ec06ea76cc88364e82fab6db4e97c7a1f8841409d5bad1ed377db1ab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 376.9 KB (376942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b200dd9d7936388cee63e986533a5e6f4c5cd3e17fd0cd0c8ce10689499288`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66a3739df18124532e005e6e2f676fee662b557add1fb9f756e2fa1aa3a235`  
		Last Modified: Wed, 03 Sep 2025 19:00:01 GMT  
		Size: 62.5 MB (62497761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d4085daa7946c18453d6431bca13352e3a418408ce342846fab2a53a4750e3`  
		Last Modified: Wed, 03 Sep 2025 18:59:55 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4bf37adc617b100596b6a009b9fdfb4704df92567918df0860d843e837614c`  
		Last Modified: Wed, 03 Sep 2025 19:12:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6739503020df128d5a7c8c2b1703f54d6bcf8f07e266c9e36f71218257de2aad`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34327dfc9e027bd4fb48ecc98431f030b8805d7cabcd6e9d06c07da75c830573`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee194ebeba1a7109f4c0e3411aa368bd73a494a319a134bd9526f64623ac5808`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c8dc90ad4deeb81b118eaf911a780b0a098cbf0020a22c20254ffe09a5880`  
		Last Modified: Wed, 03 Sep 2025 19:12:02 GMT  
		Size: 2.4 MB (2359656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a274434bed633e280c8a09f9223295eee584629c55942b864767c8069a4e7b8`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:7731ace86cf7e6695851ce19b14c2dc5f354914a10b60e3921efb7ee39beb338
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2397880217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd8c1e958209452b37d9673a2fbf9496b429ce7070a04d65dc55f518b0c38ec`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 03 Sep 2025 18:48:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 18:48:02 GMT
ENV GIT_VERSION=2.48.1
# Wed, 03 Sep 2025 18:48:03 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 03 Sep 2025 18:48:04 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 03 Sep 2025 18:48:05 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 03 Sep 2025 18:48:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:48:40 GMT
ENV GOPATH=C:\go
# Wed, 03 Sep 2025 18:48:48 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Sep 2025 18:48:49 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:50:54 GMT
RUN $url = 'https://dl.google.com/go/go1.25.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4a974de310e7ee1d523d2fcedb114ba5fa75408c98eb3652023e55ccf3fa7cab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:50:55 GMT
WORKDIR C:\go
# Wed, 03 Sep 2025 19:05:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 19:05:44 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Sep 2025 19:05:45 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 03 Sep 2025 19:05:47 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Sep 2025 19:06:13 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Sep 2025 19:06:14 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55b4ef7b22d881631bb814f6dc5455e9f552bb1d067b28ce008be2a063e63ce`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dfba081f0cce40b460d95e533de00858b144d90786ce8706d7f37c7e88dc38`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c29706c8046c63eb160ce1b8f6f1c8113d6450c5a6081812ba1b184665d1df`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bf7117a3c722b63bafbe893751fbc9d1f270e9d8a8d02545624993b284fe69`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2416bbf64eff4950370f959628f2ae2bb16ec69741dd79ff9d00d10696a3fcb`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbd241fa90be05d0b54c20c957bb16af4c997344a9ea74ea6076b2ae351c5ea`  
		Last Modified: Wed, 03 Sep 2025 18:51:52 GMT  
		Size: 51.2 MB (51209907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7662d22bdccac02850ff814f6a0bdc0d4d1f409dfc5ecae417260b5afa857f67`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79219794d49356813ef838e353f4bf0f6b5b60f8d110b660146fc95e8592f363`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 348.3 KB (348313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de42a340b60b1f23809e958183e2f7ae8ebcc27c28cbfa4cbcf8c6e1d82890`  
		Last Modified: Wed, 03 Sep 2025 18:51:43 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151d32783f0d4f9471f00d851630ba3b26156e93a30191f50084ef4eafe2d90`  
		Last Modified: Wed, 03 Sep 2025 18:51:56 GMT  
		Size: 62.3 MB (62277112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349e51596a7dbfa83e2250f0505aaeceff684958f862f3d7d67cf01f570577b9`  
		Last Modified: Wed, 03 Sep 2025 18:51:44 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f085cf7bac427d2c8e24d560effb171ec0430d61b424de5fc05dc6dba321b371`  
		Last Modified: Wed, 03 Sep 2025 19:06:42 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8bb2e12b4b8efec6a044749c19a0471d6f24b139978744c76b7d49c05f2362`  
		Last Modified: Wed, 03 Sep 2025 19:06:42 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0ca355174870753d670412d41ac1be064c1a2a66b77db2309273613a76fe9`  
		Last Modified: Wed, 03 Sep 2025 19:06:42 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cae882f30b92f5b4e7a03fdfc9575ec7485229ad73c36913e873bdce7aa6ad`  
		Last Modified: Wed, 03 Sep 2025 19:06:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89413f7de303a97b1510ff09e4873d32a842d012a236a406d50928c180de4b2`  
		Last Modified: Wed, 03 Sep 2025 19:06:43 GMT  
		Size: 2.3 MB (2336044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825aec2c64171d2f671e596057194f37b5193c9dd06615de7751984eaa7eb93c`  
		Last Modified: Wed, 03 Sep 2025 19:06:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
