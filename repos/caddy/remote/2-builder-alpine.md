## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:b18f5ef8d7dafeec585196c6952e4218d7bb8d5b621ce53c31bd091b18db5509
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

### `caddy:2-builder-alpine` - linux; amd64

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

### `caddy:2-builder-alpine` - unknown; unknown

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

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dbcb4b52a21e563618f662f7945295a4753fd2c6330bbd60e5144964d67eca41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70740771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0dc9068e3fe183a0d5a2ae55a16fbd8d890628395af264a2d89376511e3fff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
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
	-	`sha256:85ab2d2f547d457177385ee8c584aeec12becde8a813a88d8e3692d56d6bdc11`  
		Last Modified: Tue, 07 Oct 2025 19:34:31 GMT  
		Size: 292.4 KB (292396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a729a3e231583976ae1f9cca817bd27dd00673c51d31bb2652e5b51a3d2ea3d`  
		Last Modified: Tue, 07 Oct 2025 19:34:35 GMT  
		Size: 59.1 MB (59074026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d646ee4c0b471ce651bb2f27d2e4931233fdd6815c76626a4dd325719044b1d7`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6991d0bd1dac463d19255050afce12898c6203eea1afdaffc7e382aa4b6b5`  
		Last Modified: Tue, 07 Oct 2025 20:12:14 GMT  
		Size: 6.1 MB (6127845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8829aa3ae0e4b71cef1f5bbd6677d28717d01f759bc91b802bb881fe92f418a`  
		Last Modified: Tue, 07 Oct 2025 20:12:17 GMT  
		Size: 1.7 MB (1745003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c16be77d1aa138673ce1f4bf5b67b4c4eccf657f0acc0b632975954800bbb`  
		Last Modified: Tue, 07 Oct 2025 20:12:14 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:6f23375f3fae2b01324efb52c7047cec90a65be029dbe4af9e2b8f496871b295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7df9e3cbf651eb77e9c6c0209dbc6c40b3dead61d79f24c760a1984356a918`

```dockerfile
```

-	Layers:
	-	`sha256:92f3d64b31106af35280fbe4f489a177291948ea7aa509b75990dccd2f8d34a7`  
		Last Modified: Tue, 07 Oct 2025 21:52:47 GMT  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:55b114f5252af20f0b160f60b8e33dd28b0c979f9cd4f1223ff5b0ffa6c13045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69928250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d481af99da9494069c9116222dd4d7794083456e8e74cd739b338c7f28fbdc2e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
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
	-	`sha256:f4a288a79ca6a4350337b07c932262e8f347ed6880fe59b5563ac73c9f803137`  
		Last Modified: Tue, 07 Oct 2025 19:34:07 GMT  
		Size: 291.2 KB (291250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28977543608eb3d47060855462d9576fb750f3b4671b32d32fcc7f41fe2a4f4`  
		Last Modified: Tue, 07 Oct 2025 19:34:15 GMT  
		Size: 59.1 MB (59074083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816d18ba2c391dce999f8d624e00e98d0750960159838ad5a758a1c823370d0`  
		Last Modified: Tue, 07 Oct 2025 19:34:07 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170a7711e720e61a5bea9c3e9f89d43f9b7cff046fdb448464ff7852495a7a29`  
		Last Modified: Tue, 07 Oct 2025 20:12:34 GMT  
		Size: 5.6 MB (5604533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37cd6cbc3ecaa5366265b2f2123fd3fc396bbd11f243ebbf65b2818815e3633`  
		Last Modified: Tue, 07 Oct 2025 20:12:31 GMT  
		Size: 1.7 MB (1738755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2a0ee9d76fad199709a7ed41987fed2b3a1328d22f52fe7a471b1d44816e92`  
		Last Modified: Tue, 07 Oct 2025 20:12:31 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:090872a581fa408bbcb6c36b988f85a4bf91ec6e9d77b041b9f7cfece1ae3499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915116088f16b2607edef8699dce078a526f4daf9629312a3752f32988dad930`

```dockerfile
```

-	Layers:
	-	`sha256:19926eb98d13a1aa5d7d42a724a81a9c8ce3766554c90a492738310bbacbf158`  
		Last Modified: Tue, 07 Oct 2025 21:52:50 GMT  
		Size: 283.5 KB (283539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acb47d7b9f091f502bbefcb2d9b1ddebe7f46211f298501aa5068160accaf25`  
		Last Modified: Tue, 07 Oct 2025 21:52:51 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:28c20c8d5c79bff85a1ecdf837438bb14cfe6d39577d09e1736333e030c48174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70050945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f64bf90acbf44558cd2643514517f920b14a9e7290622e76bb7eb2148d2af3f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
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
	-	`sha256:5caf2aa38194e3316af15efb06580b5313b6b61b78cf72e3b0e60a4f16867695`  
		Last Modified: Tue, 07 Oct 2025 19:34:24 GMT  
		Size: 294.2 KB (294173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66626199bcfab248906ccbdd0d977cc77ec2231a37f1710a42892109d86b2544`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 57.6 MB (57647819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9329b66302da068245ed3133e27e7639b7a02a085eea51633dfcc2b5235878c`  
		Last Modified: Tue, 07 Oct 2025 19:34:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b391423c5f2cdf00c56a29e8223db59d8e39a0d51927768e24fa0344bea1`  
		Last Modified: Tue, 07 Oct 2025 20:12:28 GMT  
		Size: 6.3 MB (6261231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1896c4d7e6f8cb4114d3f54e0711a612f2c56eba974e387bc42ab3a48a3df1a1`  
		Last Modified: Tue, 07 Oct 2025 20:12:28 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981659c68f611dbe6c2ea8fba91db5ae7cb4eaac38ff210b2fe33d3450b16960`  
		Last Modified: Tue, 07 Oct 2025 20:12:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:447b6da8c0ce6c5d234988dc7c21df5d7f99dbd404333a71308b2767579d37bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8611da94ba3561f3144275732519ec48c1182142d1f1cdd7abdbff7c0605b7d9`

```dockerfile
```

-	Layers:
	-	`sha256:5c60325b592b30ce07432c073988c1b49ceecad95190af6c4e50fbae26d4dd61`  
		Last Modified: Tue, 07 Oct 2025 21:52:54 GMT  
		Size: 280.6 KB (280599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b0cb881f1d4cc1746c6affd041d1ade0d71b80981ad60e2720fe446b38bc4c`  
		Last Modified: Tue, 07 Oct 2025 21:52:55 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:bfd27c47f472adffc3c4b342bd11f75c44d66db2435ff4c4509f13542e0b3ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70413039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a643aa4a9d8707188dbdfc64bfc5c93b659470eab595533fd7d70095c1b8c748`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
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
	-	`sha256:eaca2bbec3cff414f53adc5e9634f07a3fa7f1e3320dcbcc3b9d03910b13002d`  
		Last Modified: Mon, 06 Oct 2025 21:14:02 GMT  
		Size: 294.6 KB (294637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab16c006e3e87a0bd86bfecf5ca21f23b4930a744517459433c08bfbfc59e0`  
		Last Modified: Tue, 07 Oct 2025 19:34:11 GMT  
		Size: 58.1 MB (58133794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe88dcf3b18f587d64a41496f38d15ab3a9062aa436fbed7f50769b5a5117d`  
		Last Modified: Tue, 07 Oct 2025 19:36:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db3d6298b2f8a34ff2a490580e9c5ea2277eb347071a2ec6f1632325b583986`  
		Last Modified: Tue, 07 Oct 2025 20:28:06 GMT  
		Size: 6.6 MB (6550910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3c14c7bee57d4adc49ccce6ac034b13dcb5db867000c75647b217850ca8baf`  
		Last Modified: Tue, 07 Oct 2025 20:28:05 GMT  
		Size: 1.7 MB (1705995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fec154ff68a954f91b7bd72086666da7cd2388bc865261d0a25a10165a8c2d5`  
		Last Modified: Tue, 07 Oct 2025 20:28:05 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:1149c8da89183d39ed8f0a31f8caaaae75e95489a5a6342aeff9a583ce149bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 KB (298801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f390e23b0b41c71009cc5871a85ee36b3fabe5162c54c175ce2fa416f6680491`

```dockerfile
```

-	Layers:
	-	`sha256:969eb51652472e13fdd12f56aef9191d9b7e0c22cdca0aaf75e5c7166151115a`  
		Last Modified: Tue, 07 Oct 2025 21:52:58 GMT  
		Size: 278.6 KB (278616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4266f2f01d20f4f9f02587ce16e605d0cb56c8c1845365a8e76744b67a0bc91`  
		Last Modified: Tue, 07 Oct 2025 21:52:59 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:7f3f151e19ff9e7d6dec04d49ac0a97fc6b38186e2a81b8cbf9e3bf75f5fff4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70467658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1988a0efdec2cc50c6f8dd5096bebdfba60c5d9d39ab66403709c6ae7bee82`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09396f9703679f1457da8ea8533cdf5f2a459c8f9efa4664152e578880b25`  
		Last Modified: Mon, 21 Jul 2025 22:46:21 GMT  
		Size: 282.8 KB (282780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41271712fdf69bbd5435fcdb57d1cca7c9114e983cf470cc61ed6e9d72e6a385`  
		Last Modified: Fri, 05 Sep 2025 14:47:51 GMT  
		Size: 58.6 MB (58572885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e775d8e9524582abf421438ee797b775d135796d56bc7e24a9e3c45c80b837a6`  
		Last Modified: Fri, 05 Sep 2025 14:50:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5641d61dd99e4f4969f4dea9a411a0841bfd723f064e58e55f2b4cd81aa34a`  
		Last Modified: Mon, 08 Sep 2025 10:27:41 GMT  
		Size: 6.4 MB (6374385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c957bdb37fe768b77c6df14dbb252bd4cffe87cd662d0a92e38d9e9c895a1382`  
		Last Modified: Mon, 08 Sep 2025 08:22:09 GMT  
		Size: 1.7 MB (1724216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43f03cea1b9a56012ca5f5380ae7b9b3e2779f7e62714f79bb839544b45f3c3`  
		Last Modified: Mon, 08 Sep 2025 08:22:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e268b6ee3ec33cbba9a6da4c8e7035662172d87c9f07431f6a2da210a2a81e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 KB (295101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb4b8428886be0a77547d116ed24e694762a531b8a7986aafebb5a24d495bb7`

```dockerfile
```

-	Layers:
	-	`sha256:e8e40690843b20aa3b827fde12fc71093c92550b16ea32640314d275b2dd8999`  
		Last Modified: Mon, 08 Sep 2025 09:52:35 GMT  
		Size: 274.9 KB (274916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02a54cff1130b5ba1886d74c8e22d339fbedfda270498d55dac8379ffda9a2a`  
		Last Modified: Mon, 08 Sep 2025 09:52:36 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:fe545b819b04e4631316e4d35f8a4ed024bc8b6ce28dc55a8beb0f49876cca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71704662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837355b7ca8f1fadc32f483a8aaf771779498b1a09a21861f7599c6e500b70c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Sat, 23 Aug 2025 03:19:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
ENV GOLANG_VERSION=1.25.2
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
	-	`sha256:50a4b5681964cbbac71727dc93824660a7b57f0fcfeb79eaa856084f3c55796e`  
		Last Modified: Mon, 06 Oct 2025 21:12:02 GMT  
		Size: 292.2 KB (292182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ba33a49b3f3080422ca98d26430f3e1c1ba8f8f41bc6d8af4cff9843f4da`  
		Last Modified: Tue, 07 Oct 2025 19:36:10 GMT  
		Size: 59.5 MB (59478805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb90e3589cde6accb78ee3a4a577fbd3998fb696c061a079258149ad9758b6`  
		Last Modified: Tue, 07 Oct 2025 19:40:06 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b14013c99815ed3f97c915d71f33b5c259564001159d8f6b87a087316387c1c`  
		Last Modified: Tue, 07 Oct 2025 20:39:21 GMT  
		Size: 6.5 MB (6505260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aaa8704567e642c9785b366700c077f06e5c3274bf0a2f34ea745b7a3eae6be`  
		Last Modified: Tue, 07 Oct 2025 20:39:20 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4ef5098c1fb46629cb880c4920744ba464d13d81bb9eb004f9d387bbc40cfb`  
		Last Modified: Tue, 07 Oct 2025 20:39:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9a16a68f79c4215486319b7ade85e7889d5b478d28ffb5ddcffa57df6371b919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 KB (298659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5634305189bfd1996ae4dfeb59803421ba179809d452c543ffe03179f11e72e`

```dockerfile
```

-	Layers:
	-	`sha256:742a0a291c38881018fe3e966961c218e91ed740573431d58b25ceaa6ac39f40`  
		Last Modified: Tue, 07 Oct 2025 21:53:05 GMT  
		Size: 278.5 KB (278544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262a602743c7ccde18939a7815658efb729575104661e09c5d5caf23ffc5cd8b`  
		Last Modified: Tue, 07 Oct 2025 21:53:06 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json
