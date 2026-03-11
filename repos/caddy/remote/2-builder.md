## `caddy:2-builder`

```console
$ docker pull caddy@sha256:84dfc3479309c690643ada9279b3e0b4352ce56b0ec8fd802c668f42b546e98f
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
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:e52cc41757d6d2bed05c107cef9722331fe2d5892353651c1581a931cf325a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79797145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd7049791fdde605f85b7171e0d582b56f4e561a015715a3f2acc89f2d14be65`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:05 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:05 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:12:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:12:07 GMT
WORKDIR /go
# Fri, 06 Mar 2026 18:15:57 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 18:15:58 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 18:15:58 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:15:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 18:15:58 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 18:15:58 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 18:15:58 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 18:15:58 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644a983862e3898a5575fef5c81590cbc92d1c1e1bf5f61112c0cd35e6b7be98`  
		Last Modified: Fri, 06 Mar 2026 01:12:20 GMT  
		Size: 296.1 KB (296074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbff1d4eb7eece408734c05c8c63a49bb181871bc1280cff3f0e28d25a4ea28`  
		Last Modified: Fri, 06 Mar 2026 01:12:19 GMT  
		Size: 67.2 MB (67216879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ee208a3600503f47e9ec1ced0e8abb825a045473b092f1fe872b81d9873706`  
		Last Modified: Fri, 06 Mar 2026 01:12:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0a58e10754cdd8595828021650e25fc410c579364b4c0476b5a618ce4128e7`  
		Last Modified: Fri, 06 Mar 2026 18:16:06 GMT  
		Size: 6.6 MB (6575280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c530dd449db2f043a350a68581f2f44f8c05f85218cf4bc59eda6dfc223b0ebb`  
		Last Modified: Fri, 06 Mar 2026 18:16:06 GMT  
		Size: 1.8 MB (1846499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac9f7732f1ae9d302994648ac1d89ae739952622ed04cf97d08f2bb9cca3bac`  
		Last Modified: Fri, 06 Mar 2026 18:16:06 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:eb71f230352c6c2955e8dd117f8be3173e4d501ee66d6ac429ab22de2266356a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 KB (304453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f5a0ac243b40e923fd854694d70bedaafd32eb22385301624124b7b355df4d`

```dockerfile
```

-	Layers:
	-	`sha256:3cbf0cc72a88cb45cd9ec65947b737069d4eb82f1516af125ab5b2b7ec534558`  
		Last Modified: Fri, 06 Mar 2026 18:16:06 GMT  
		Size: 284.3 KB (284325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da7541854a9b637f98c72038fe6acefe993ad9d7e04ded6c63de48d60163faf`  
		Last Modified: Fri, 06 Mar 2026 18:16:06 GMT  
		Size: 20.1 KB (20128 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:4c82b74a73c16dd3a65b4ba3933362b1ea8224a2ee5bcf2417b9aa1a6b5a604c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77854475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dcc9ea6a208ee296de3cf09cb7fccba61bf689dc98529350a6d362500bc03e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:48 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:13:12 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:13:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:13:12 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:13:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:13:15 GMT
WORKDIR /go
# Fri, 06 Mar 2026 18:16:02 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 18:16:02 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 18:16:02 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:16:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 18:16:02 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 18:16:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 18:16:02 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 18:16:02 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1109a5071b02b1044612a78906bb866947d31adddc34582210c9b1df0d6c2d`  
		Last Modified: Fri, 06 Mar 2026 01:13:26 GMT  
		Size: 297.3 KB (297262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96dfc026f620d0674c1a89536cf39d64e74602dba70d199d21c90c7b01bd9ba2`  
		Last Modified: Fri, 06 Mar 2026 01:13:28 GMT  
		Size: 65.8 MB (65757141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bf8dd9810462b9c3cf1794258fb5fb3448a3b8ff5e6eee0b1449b61acbdab2`  
		Last Modified: Fri, 06 Mar 2026 01:13:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bf95c95b762c31ef896c09aad1f19f0f6967575bef46874589ebfbab9f439c`  
		Last Modified: Fri, 06 Mar 2026 18:16:07 GMT  
		Size: 6.5 MB (6484657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0649c8571034f98f879327218131bc8bc323009a3e1de488c82c9122f83b1ea1`  
		Last Modified: Fri, 06 Mar 2026 18:16:07 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c296837776f310205e9645b5007fc18ac666eb9c088f4c47607a63c67f5d62`  
		Last Modified: Fri, 06 Mar 2026 18:16:07 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:836c8f1c13702421f6b2c55fa0beb961bea459bd0b8143e08427bdfdc275cfb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503f575790a2c45196282c8a8d0cc57efe1fb3c825c858719bfaac574025a94e`

```dockerfile
```

-	Layers:
	-	`sha256:1af7ea40df00fe1969485836961433faf8f393d464da3b1fcf3667443b05c90f`  
		Last Modified: Fri, 06 Mar 2026 18:16:07 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:199e364c9e5a1903336f4bc915d751e3697dd9211edd54722ecdf9ba700c3dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77008705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3ca83f1458d01bec2e97fc34942216a544fbef77a9f765c0a90d621adeb2c9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:40 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:11:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:11:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:11:52 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:11:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:11:55 GMT
WORKDIR /go
# Fri, 06 Mar 2026 18:15:08 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 18:15:09 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 18:15:09 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:15:09 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 18:15:09 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 18:15:09 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 18:15:09 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 18:15:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8528f8fd0be7185e5fdd156634e845361ee385919d5f74f4dcdcdb37ceb8ff5`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 296.2 KB (296202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71a08a325c7d5f7b73bc8da93a0980d5401206ec7c3b40584ca8d21ca82f77`  
		Last Modified: Fri, 06 Mar 2026 01:11:53 GMT  
		Size: 65.8 MB (65757104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffb5ff6c2a264c2b3f1d07eb347799ecf4b393d1b4bfabb7c4d26a87c7354ae`  
		Last Modified: Fri, 06 Mar 2026 01:12:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe8d8cd272a22df6d79b9718cd92636031ea407a0c509ada9877a67dc2f47dd`  
		Last Modified: Fri, 06 Mar 2026 18:15:16 GMT  
		Size: 5.9 MB (5934324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b2c43745a42589f12f7dcd7bc4fe7bd336423a7d831c8d65ccd9a97e528a1`  
		Last Modified: Fri, 06 Mar 2026 18:15:16 GMT  
		Size: 1.7 MB (1738758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3d968cb17a041386c2ada9be0f45d4ab783abb1b51d633bb3898983966392`  
		Last Modified: Fri, 06 Mar 2026 18:15:16 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:dc19f4921825f249bc901f1f171a4097921ff1794bf5290373dfbabb1a6349ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 KB (306970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a093c8666bc8bf476a92222a9c07a1b1838a80a0908242802cb000ce4921ab`

```dockerfile
```

-	Layers:
	-	`sha256:b341e911ea016121a5c1626059b444b3aa6e12c883337558f7b07b628c602893`  
		Last Modified: Fri, 06 Mar 2026 18:15:16 GMT  
		Size: 286.7 KB (286717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90b8c45d0ee7995efbf86ec1b0b4bea0a031f1510575f1e5fe42411c3dfc33f6`  
		Last Modified: Fri, 06 Mar 2026 18:15:16 GMT  
		Size: 20.3 KB (20253 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:468e72658ebdc4ab12b17ba73c093c2a3b9a50f4b2b885ce0ea9308262bfd59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76977272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46facef166232936e68ca6f2bd97322bc88538a571f47b73f136933559432eaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:11:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:11:46 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:11:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:11:46 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:11:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:11:48 GMT
WORKDIR /go
# Fri, 06 Mar 2026 18:15:25 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 18:15:25 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 18:15:25 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:15:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 18:15:25 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 18:15:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 18:15:25 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 18:15:25 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62764d53541d11f63129956ccd8b52d20597aca289f431759deb77ea2275f569`  
		Last Modified: Fri, 06 Mar 2026 01:12:03 GMT  
		Size: 298.8 KB (298849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49db9bb2f958b7444a4f28145af7a815dd0a47fec1608d03e2f1c673b3aa858b`  
		Last Modified: Fri, 06 Mar 2026 01:12:04 GMT  
		Size: 64.1 MB (64106129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4901bef231fb8a6d26e9c2ceb808c5c0ed8319bb7a5f6b5a284cac28d8f72b8e`  
		Last Modified: Fri, 06 Mar 2026 01:12:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed044b647d8daca0ee5d38f61f259362f6435c43dfc9f2d11abc6d7e1e5c587`  
		Last Modified: Fri, 06 Mar 2026 18:15:33 GMT  
		Size: 6.7 MB (6658230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bb8463ea2fba063e0f97a453f31a020ffe85f0a724939005c319b0007367ce`  
		Last Modified: Fri, 06 Mar 2026 18:15:33 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7840e9b41bd3a5448c9e528e25554af209de08288639a3a5cfe58a129680d5a`  
		Last Modified: Fri, 06 Mar 2026 18:15:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:8593b94aec2feaa2331cc41027217c895a862dac07ad000e514db7df360d8ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 KB (304075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d060c6cb21f95265e9fae149ffc35b89ea72a94f626d7cf6a11848da9bbf1b`

```dockerfile
```

-	Layers:
	-	`sha256:1230aab644e2ad77a953dc495d9efb3e87be6a368c156c163de0b5cce8a32140`  
		Last Modified: Fri, 06 Mar 2026 18:15:33 GMT  
		Size: 283.8 KB (283779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab408355873f1beb558d5a7f8d139d6cab98d1babe066e59c2cea2000be35354`  
		Last Modified: Fri, 06 Mar 2026 18:15:33 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:e71c3844a9bcbe4bcc19216a9358f69e5a673e2efd3e7e92d0f02956a6df6e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77594662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e6e86816e798386b59728317514a6565dc409ea56c0a27c839532e27f65717`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:12:22 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:37 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:37 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:12:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:12:41 GMT
WORKDIR /go
# Fri, 06 Mar 2026 02:07:35 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 18:14:04 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 18:14:04 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:14:04 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 18:14:04 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 18:14:04 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 18:14:04 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 18:14:05 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e662a4a3a7cbf153b23a38a961b2078122cec8354bbb9cc27381fb9fd6abd628`  
		Last Modified: Fri, 06 Mar 2026 01:12:55 GMT  
		Size: 299.3 KB (299266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace710cfb3bb4da72d185d83d05e86cb22a686c0abd5be3e83cdf74e34b68d02`  
		Last Modified: Fri, 06 Mar 2026 01:12:05 GMT  
		Size: 64.8 MB (64765980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645e9a27139f1a82b884568a2ebeca4b84caad36f011c206583bab85d758e73`  
		Last Modified: Fri, 06 Mar 2026 01:12:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1a66af16688cd52acc6e44bd18a39dba777cd311ad70462741a2ad39c4dbf3`  
		Last Modified: Fri, 06 Mar 2026 02:07:57 GMT  
		Size: 7.0 MB (6993179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742a68653ad0851496c7dec3a5573dfa3485e622f776c070471c0a16dc53141e`  
		Last Modified: Fri, 06 Mar 2026 18:14:20 GMT  
		Size: 1.7 MB (1705998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273f013445b84f9fa4c1a0bbdcdba2ff7c119b36a0263cddb31681d4e3efe97b`  
		Last Modified: Fri, 06 Mar 2026 18:14:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:15867025e7b32bb768e8842ba9098c927af426c34e65441e7855ea774a9ef651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dabfb1d6e91d7f7212ec4fa5bc7d5ac90a7b78a86fe3ec864af03a7be7acaba`

```dockerfile
```

-	Layers:
	-	`sha256:9c8a33583c1187593772d8d5498691a952435314cf1be9bc7d9f5c098ea8122d`  
		Last Modified: Fri, 06 Mar 2026 18:14:20 GMT  
		Size: 283.7 KB (283748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edd81d7a8f10f5ea2b80345e1b7bdfe92b5cd38ca21215f2879aad16a22c328f`  
		Last Modified: Fri, 06 Mar 2026 18:14:20 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:56e827985d3d8a02c06e8767906f50b9b148f113db0cfdc5984777a83c5b9a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77435283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f972db7818662a0398aaa8bcdf58514f053c4af59e0bdaf800520bcd4c396850`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 19:12:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:12:00 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:12:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:12:00 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:20:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:20:33 GMT
WORKDIR /go
# Fri, 06 Mar 2026 03:23:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 18:16:22 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 18:16:22 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:16:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 18:16:22 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 18:16:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 18:16:22 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 18:16:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f6a28a44ff91c18ab295ffef6822bbaccafe002bd1f4a117c179d363e86328`  
		Last Modified: Thu, 29 Jan 2026 19:14:45 GMT  
		Size: 296.5 KB (296505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7741c0adede1d2e9597a871420fa82f196151039c468eac7755d531cfe50922`  
		Last Modified: Fri, 06 Mar 2026 01:18:47 GMT  
		Size: 65.1 MB (65077505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15647ffd280dd6c01380ff7053031d8b9c620450567c4be60c59090f35528445`  
		Last Modified: Fri, 06 Mar 2026 01:21:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87114ce9ff5981d8be6f900576f8ea469d86991e6cdf84ceddb9c9f8c48f3e57`  
		Last Modified: Fri, 06 Mar 2026 03:24:37 GMT  
		Size: 6.8 MB (6751171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33261180a6b133efefd1fdbe700a0e98395134c8cbf1bc7270ca95493406235a`  
		Last Modified: Fri, 06 Mar 2026 18:17:08 GMT  
		Size: 1.7 MB (1724220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940b79da1dd85ac9e3e0824f449350dd643e0979635c6c6fe10944259380ca84`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:6ae929de0b617bf403628b191fe28058797d1f29271edac1c8dcbaccbc960674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0cd181e0df8bd1b9cd5f0d320b6ff5432814eb87313c6f8687336b58ed0428`

```dockerfile
```

-	Layers:
	-	`sha256:6f43b60ab5a5e1e473d032936d898de793e7277a884fbe485cfaa037e3c8c3b1`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 283.7 KB (283744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4da034d691fcf2e5aceec8f8163b4784ffa39ef5daaeb53dc20e93cf6f91b22c`  
		Last Modified: Fri, 06 Mar 2026 18:17:07 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:0e34474704ac93a9e3282cc64f4cc99e14745af40e42935638baf4c7aa07627a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79100397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e01627f78a8f247bab717939ffa50fff13777444fd1eeb96f4a4dce71bf2bc3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 01:10:35 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 01:10:52 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 01:10:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 01:10:52 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 01:10:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 01:10:56 GMT
WORKDIR /go
# Fri, 06 Mar 2026 18:14:20 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Fri, 06 Mar 2026 18:14:21 GMT
ENV XCADDY_VERSION=v0.4.5
# Fri, 06 Mar 2026 18:14:21 GMT
ENV CADDY_VERSION=v2.11.2
# Fri, 06 Mar 2026 18:14:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Fri, 06 Mar 2026 18:14:21 GMT
ENV XCADDY_SETCAP=1
# Fri, 06 Mar 2026 18:14:21 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Fri, 06 Mar 2026 18:14:21 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Fri, 06 Mar 2026 18:14:21 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79449d8f37ca627569c53e700d0b5ae9b25ebeef0a08dac074cc719821e22ba7`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 297.2 KB (297183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ac4fc296175935efd55931d7d181f8e7c85d38405c6fdcb1a96bcb9115d7eb`  
		Last Modified: Fri, 06 Mar 2026 01:11:11 GMT  
		Size: 66.4 MB (66432747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d729dd9fe0b725e8d914a70685a29638ee35da82ebe402e075a4ca4768e879b3`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9dff215039e2b0565d84decbcd7b13b520437bf2c47b0c6ea0bfc765f6160a`  
		Last Modified: Fri, 06 Mar 2026 18:14:32 GMT  
		Size: 6.9 MB (6861686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf04599c6863c3818f47566fd9dfbd0f4d9d251462bd885e5ca0628dca434f1`  
		Last Modified: Fri, 06 Mar 2026 18:14:32 GMT  
		Size: 1.8 MB (1782856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c3cdecd3f805d94e29bb6ed51e2a414ee5df8212111bee1f5c71f9ca0d97b4`  
		Last Modified: Fri, 06 Mar 2026 18:14:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:52153738047f47d85bf3edb37b7a271fbf28f79d76e5e3c9fabaaf5f4593c966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bbeed820ce8b8ffe864e63baa3414646aeab99151f7e95f5dc9a373fb87d5a`

```dockerfile
```

-	Layers:
	-	`sha256:977e2cbbcaa2bab6499c1e7eee7eb7c965230295bbd9377a77e237485842f341`  
		Last Modified: Fri, 06 Mar 2026 18:14:32 GMT  
		Size: 283.7 KB (283674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78deb7e61c8f18d01b342a8257b653fb2725cc9f8a1cf0ca6057e7bb09085468`  
		Last Modified: Fri, 06 Mar 2026 18:14:32 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.32522; amd64

```console
$ docker pull caddy@sha256:e7a5f83bd97676690f9437948fd2d5695706b0bd60a476364c7d1ab197943bcc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204887473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eeff8260c36307bf3ffce4052322f299744d536536239d9e629568e6552e06`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:57:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:00 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Mar 2026 22:05:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Mar 2026 22:05:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Mar 2026 22:05:01 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Mar 2026 22:05:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:05:15 GMT
ENV GOPATH=C:\go
# Tue, 10 Mar 2026 22:05:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:05:21 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 10 Mar 2026 22:06:46 GMT
RUN $url = 'https://dl.google.com/go/go1.26.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9b68112c913f45b7aebbf13c036721264bbba7e03a642f8f7490c561eebd1ecc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:06:47 GMT
WORKDIR C:\go
# Tue, 10 Mar 2026 22:45:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:45:17 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 10 Mar 2026 22:45:17 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 10 Mar 2026 22:45:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Mar 2026 22:45:28 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 10 Mar 2026 22:45:29 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158f9b4eb4f13cf841ba448566ccd79f22d7a8ca6bcd04fdb96cd2841e725493`  
		Last Modified: Tue, 10 Mar 2026 21:58:01 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537c58fb7d6a751d67b7371e24ce8226663f9217eacb731043dd2b73c112496`  
		Last Modified: Tue, 10 Mar 2026 22:07:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bacc48570a713ce4f010416e60e52c8a550c9ee36efd079f8a6fe4d6f99da3`  
		Last Modified: Tue, 10 Mar 2026 22:06:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaeeed7c63e20322a8d7311517fa65e57b1764b007458e759c5462b6f416df8`  
		Last Modified: Tue, 10 Mar 2026 22:06:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aa9143f21f5416348d4437a34a725d5cd729524fa25522685e5b39bcfe18ea`  
		Last Modified: Tue, 10 Mar 2026 22:06:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b4484cf7d31295b26e1ae322f9930bf2c7b6663b4c620012eba3119c3e9628`  
		Last Modified: Tue, 10 Mar 2026 22:07:05 GMT  
		Size: 51.2 MB (51220336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e06ed3ea7e9138b78745d00fd7f65e2c5a3c74c62b7e36f5fc72470616b6aa2`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af935961bb05c557aec8648fc00a747e08111ca5b6d6effc28e2db7223b4127a`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 343.5 KB (343519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a520c69ecc8202751ef255e3376b6c3e53cb8d57f3901ad6040cff68deb2d0f`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beece69de6888783a8e4e26ac3c5a09f43ca50d4a3a09326cbc53d8b2c00983c`  
		Last Modified: Tue, 10 Mar 2026 22:07:09 GMT  
		Size: 69.8 MB (69820785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369d2d0eb3f781b19f0e37e0f5f4d389a635dfe78b9f5b6b4329f2d3fcf8256`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 1.5 KB (1464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbdb68cc051780630a4e329c7eaa3ae2bd1194fd0ba9aefd4e7d82a47faa8be4`  
		Last Modified: Tue, 10 Mar 2026 22:45:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4417d3ae006bbaf18fc300eacf6933336c41bb2d540ed8db257351e6256c5acc`  
		Last Modified: Tue, 10 Mar 2026 22:45:33 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeefd36b02ae79e471f32390b09664c08d6ad101d158223f00e23a004cf3e99`  
		Last Modified: Tue, 10 Mar 2026 22:45:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833b5752b9988794103e936b60228fde85d9e3d2ad1eafb129302e8811f0c36d`  
		Last Modified: Tue, 10 Mar 2026 22:45:33 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c901760ca1561bd52ba911727f4e1ac4da42c40c13394cbd18b309c85f630c`  
		Last Modified: Tue, 10 Mar 2026 22:45:33 GMT  
		Size: 2.3 MB (2289558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71435147c4ea7e7fb3c83a98240829b8c764e5f2b94caf963aa3122c994fd954`  
		Last Modified: Tue, 10 Mar 2026 22:45:33 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.4893; amd64

```console
$ docker pull caddy@sha256:846922e030c788d5c040a49f860a8f9afbf5db28f0aa2851c50f4c8117e66918
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2106154498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1daab4d1121843177c972d388ff7db7a67b7878295245b1f54e885d38a3ffaa9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:56:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:08:15 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Mar 2026 22:08:15 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Mar 2026 22:08:16 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Mar 2026 22:08:17 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Mar 2026 22:08:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:08:30 GMT
ENV GOPATH=C:\go
# Tue, 10 Mar 2026 22:08:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:08:36 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 10 Mar 2026 22:10:08 GMT
RUN $url = 'https://dl.google.com/go/go1.26.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9b68112c913f45b7aebbf13c036721264bbba7e03a642f8f7490c561eebd1ecc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:10:09 GMT
WORKDIR C:\go
# Tue, 10 Mar 2026 22:42:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:42:26 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 10 Mar 2026 22:42:27 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 10 Mar 2026 22:42:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Mar 2026 22:42:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 10 Mar 2026 22:42:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01bce865a5fef3c3d366224bb94ee05dc622261950fdd529edc41f69aa86a82`  
		Last Modified: Tue, 10 Mar 2026 21:59:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9059baa231ace69538d98801b5f30ffe2126f2644971c0a5e1f1ff7ea4d7d6c8`  
		Last Modified: Tue, 10 Mar 2026 22:10:27 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651107031cb9c76c72a3dff51a55e12db7465a0608babbd79ed3c05c4f323bc6`  
		Last Modified: Tue, 10 Mar 2026 22:10:26 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5cfcc106b1cd6c8910dcb8c9c502287340907aa4d1da09f36e2c5d89470b9e`  
		Last Modified: Tue, 10 Mar 2026 22:10:26 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcba0c26b8ed8ce7c95303ef278e96880371b58a262f9eaa8f2b27391a331d60`  
		Last Modified: Tue, 10 Mar 2026 22:10:26 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e501a5641cc66390105a05d8e6acedc3b550b45c321a2b407e6369e56a3502`  
		Last Modified: Tue, 10 Mar 2026 22:10:32 GMT  
		Size: 51.4 MB (51354870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bd5c4ee5cb757bcc3cc84dda430bbcb5af5184bd5a32e4c8a41457d871233f`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b83f542f1e29c3e63c29d942116e301b7ccf3a81fa94d26674444c9215986ec`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 348.3 KB (348328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6f90bdaf8f7759ae4c97e8a498bd1a94a4a7c77e0d7584c692fbb00728fd33`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794087f7e9b49f5acfbcea536844ab35b1dd3f0e614139ab194710f93902aba0`  
		Last Modified: Tue, 10 Mar 2026 22:10:36 GMT  
		Size: 69.8 MB (69834349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f77d6574ad874837b8aad143b0dede2ed5826b8e18afe75a15edcacd11dedeb`  
		Last Modified: Tue, 10 Mar 2026 22:10:24 GMT  
		Size: 1.5 KB (1488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e225d1f38de1035075f14aa400055847a8810c7a6b01cfec7b8bc6bb42812e0`  
		Last Modified: Tue, 10 Mar 2026 22:42:40 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a815006c14eba66a81da6401b6bea3f292cf2a95666888dcd89378d8c021351`  
		Last Modified: Tue, 10 Mar 2026 22:42:39 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca0e47d283f89a29b0ee931fc636a271484809d64782ca9bfb650297bcf79efc`  
		Last Modified: Tue, 10 Mar 2026 22:42:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6986f93bbed732551319643662469f263b107f2e0c3940b5e0ed6e2cd3717af`  
		Last Modified: Tue, 10 Mar 2026 22:42:38 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543c972c1ce32d3ef3375dbb0b6c3172d21e5d2b535aa348a99d29f748174cd5`  
		Last Modified: Tue, 10 Mar 2026 22:42:39 GMT  
		Size: 2.3 MB (2318246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560b8b4f8e4f33afa43a217661d75d089c948f00318e7eeb4f134fbb3575d90b`  
		Last Modified: Tue, 10 Mar 2026 22:42:38 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
