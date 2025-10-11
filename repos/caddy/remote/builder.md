## `caddy:builder`

```console
$ docker pull caddy@sha256:5ffdd1eb7c262d118977dfd8c4a0c34c7781366fbadef3b4daeac459cb30e99e
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
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:51ad4e13256a287e190b8863f8c1afcf044e54c024bf97f3bbe38ddebdcb9c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72303117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53df702f8ae8580ee43b354bf2c0a791f8122c7164d0f6f0d2a0c6f5a90c09fb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35fb4624d26424571dfb821ae83d912cb463420dcedd6224f36bb5f96f92542`  
		Last Modified: Wed, 08 Oct 2025 23:03:29 GMT  
		Size: 291.1 KB (291148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2aec7ef170b5f02e240ef6c8aac64fb96a14688ea0750c962c145c141f3830`  
		Last Modified: Tue, 07 Oct 2025 20:47:28 GMT  
		Size: 60.1 MB (60149177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333b49ad6fbf2b99bf7532e840b5bff11ea42e960a0a8851832dbe82fa3d7c00`  
		Last Modified: Wed, 08 Oct 2025 23:03:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af5a2e9b9fceeb5a3b6fd41d35fe235adac28dc6f667a3a5d24500e317fa91c`  
		Last Modified: Wed, 08 Oct 2025 23:47:13 GMT  
		Size: 6.2 MB (6213251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cc03736d3cb48227c6f905558b4adf3040b7db1d47e7e1206f6970f1430d1c`  
		Last Modified: Wed, 08 Oct 2025 23:47:13 GMT  
		Size: 1.8 MB (1846500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5112dc17c514a2731df451c977b2d07dcc85a92de085d7bb5a4b91bc0ce4c82a`  
		Last Modified: Wed, 08 Oct 2025 23:47:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:98ba64d7acda52e7aa5d9056ab4725a8a8cea783537ac3b8dcfb2195f72faa2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 KB (299527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a9a61f243ef362fef491aae773a56403af8bb6b854b2fa09f468af3e0479a0`

```dockerfile
```

-	Layers:
	-	`sha256:506ed6ff9240035f2024e34051bee8976b16d3ee26cf2cdabe617d35a7f93194`  
		Last Modified: Thu, 09 Oct 2025 00:52:46 GMT  
		Size: 279.4 KB (279412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae870e496b762160ec6b97390893abd8ffdfc978b257c2a9f6e3adcdc1eeae74`  
		Last Modified: Thu, 09 Oct 2025 00:52:47 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:dd278977f84adc5a1c9129cd836d540cca6de20e6b840ec573aab0b397c39e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70743771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54154929258f01004552b88277bcaf7ad38ff2c4dcb8862429a52f181a45030a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60994a2fa6b267edd2843cd5fc3f2d8c2924451ede829846056191379774525`  
		Last Modified: Wed, 08 Oct 2025 22:10:35 GMT  
		Size: 292.3 KB (292299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a729a3e231583976ae1f9cca817bd27dd00673c51d31bb2652e5b51a3d2ea3d`  
		Last Modified: Tue, 07 Oct 2025 19:34:35 GMT  
		Size: 59.1 MB (59074026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a144a8289ff4ec4a0f9128ce6b7dc6f717724bc579d510f16fa276fe7e0ac938`  
		Last Modified: Wed, 08 Oct 2025 22:10:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489309bacd6594fd4a34047d1650f9f4bf5780d593a2caa20ba9bec3e528d6ae`  
		Last Modified: Wed, 08 Oct 2025 23:13:05 GMT  
		Size: 6.1 MB (6127775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339175886b0ae9c7c18537794d41a7dcd74762c3daafd1b942693c6d1c3d15ec`  
		Last Modified: Wed, 08 Oct 2025 23:13:05 GMT  
		Size: 1.7 MB (1744999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201a02dd3c392282efa2642d8ac03370d22fc34571988fbb166b468adad844c9`  
		Last Modified: Wed, 08 Oct 2025 23:13:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:685cb42d74489ef73bafcaff243442231e438c0ef42df270840afff3714665d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302056ff80f819882f6571dd729b211879955d425e4852de6c586d5e99d6f6db`

```dockerfile
```

-	Layers:
	-	`sha256:43988f3865f7ac3e6778272a9188916e1e19dfb565093bb25a251e38c676315e`  
		Last Modified: Thu, 09 Oct 2025 00:52:50 GMT  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:fcc0ac6222231544ae7ed510400f5c250431a599fdae01d1a14c362367bc68ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69930578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5736ca22b1c671c5dfed4b1a6c0385ed46bb8c1b22d1bb63118680b4c7ca55d8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
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
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2c26235c37292159dc019803ebd2435f82dd20bd64043f085ba7daa47b28c9`  
		Last Modified: Wed, 08 Oct 2025 22:13:09 GMT  
		Size: 291.2 KB (291213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28977543608eb3d47060855462d9576fb750f3b4671b32d32fcc7f41fe2a4f4`  
		Last Modified: Tue, 07 Oct 2025 19:34:15 GMT  
		Size: 59.1 MB (59074083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac6fb7af5cbe0bd826c2f8c108ebcc4a5d1178c58d9f83207a6d0924695cec3`  
		Last Modified: Wed, 08 Oct 2025 22:13:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ee4bddc23842993933ad36a6980173dc40135910cecb418f09c0992a2b3833`  
		Last Modified: Thu, 09 Oct 2025 00:18:29 GMT  
		Size: 5.6 MB (5604381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f8db293bd3573c23e9a45f392a799aae005480824df7a5a999859894cb372d`  
		Last Modified: Thu, 09 Oct 2025 00:18:29 GMT  
		Size: 1.7 MB (1738755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ae390009e67d30fac3a4168bf72fd99980a48a8d8b6fa77492ea262af21058`  
		Last Modified: Thu, 09 Oct 2025 00:18:28 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:1f1fcd305c2aafca9bf21f75d183ed7670b1367ac77155ca78ba24c65e3fdaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 KB (302696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db020b21a52865778712f7bee55a0616c6872514d3aaff0497cd5affabcd272`

```dockerfile
```

-	Layers:
	-	`sha256:94de7df363b098d9951a312fd6d6447237b1b79828cd73ac519a1253fc42ccd6`  
		Last Modified: Thu, 09 Oct 2025 00:52:53 GMT  
		Size: 282.5 KB (282456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a087bd4c28530dcfdfbf34e25942e3e85b157cb73000499dbfd7f3d245e7c0e0`  
		Last Modified: Thu, 09 Oct 2025 00:52:55 GMT  
		Size: 20.2 KB (20240 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:dfb316bf78bf79a18b348a04e6cc79cd3dc98bd65ed572b975eca9bfe57cc71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70058355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13ffc42f9f84c017fcff4fbc0f2a6bf66aec89daf9be478638842fe6d444072`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00abc3ba1385e30f6e4c6e0525cb316aa3afd1e3a6ce37bd5dae6bf03aae2b97`  
		Last Modified: Wed, 08 Oct 2025 21:49:25 GMT  
		Size: 294.1 KB (294091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66626199bcfab248906ccbdd0d977cc77ec2231a37f1710a42892109d86b2544`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 57.6 MB (57647819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89982c427569fa227db8454803b4026b779be40fa10f2a70f135a6fa03475dc`  
		Last Modified: Wed, 08 Oct 2025 21:49:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedf84927274338bffcb8080be43a65ca1681711bf1a0a3d7f074925dd18c8ce`  
		Last Modified: Wed, 08 Oct 2025 23:15:31 GMT  
		Size: 6.3 MB (6261404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdad4e3f431b6e543cc8805ca9eba10549a389fccf30553e11fa2575c9de0ff`  
		Last Modified: Wed, 08 Oct 2025 23:15:30 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371c9c0873bd073f11e436f76fbd6c3c13cd6d7c7753a62d73c8aac73c3abf97`  
		Last Modified: Wed, 08 Oct 2025 23:15:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:736dbaecbfdb8eee75f00d0101e4b9caa27aeccbe1f4c2f9d966d857d2020c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 KB (299798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69d44fe16b38dae8f04d272359c69bd0ebfb2e1ab5b0d4ae18ff392746927d2`

```dockerfile
```

-	Layers:
	-	`sha256:a509840925c5aa3615f0dad1bfd1aacb2502525aec7e2f71a638968663da80ca`  
		Last Modified: Thu, 09 Oct 2025 00:52:58 GMT  
		Size: 279.5 KB (279516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410c9bb47cd82569f0694d36a59f9a6d8251fb758bfd2328f8c7d5dc12dae8bb`  
		Last Modified: Thu, 09 Oct 2025 00:52:59 GMT  
		Size: 20.3 KB (20282 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:b37d8c84cb1e6ef6b2191c54179ab58d17e3693b8fa47d7224ed92eebb81fdf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70418109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df48a5c118dee9b04de0ca709bccdf631e9b78c5583ef1a3dcd8359b371eee4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
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
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34403a3833161e7317f5f43c031b3114df383a82ea83c5851edc4d5c8b921a`  
		Last Modified: Thu, 09 Oct 2025 04:12:57 GMT  
		Size: 294.6 KB (294579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab16c006e3e87a0bd86bfecf5ca21f23b4930a744517459433c08bfbfc59e0`  
		Last Modified: Tue, 07 Oct 2025 19:34:11 GMT  
		Size: 58.1 MB (58133794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4273071d0d29fa1710b0b144feb490014c3531d770a922413a9bd76359d9c503`  
		Last Modified: Thu, 09 Oct 2025 04:13:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65888d005703dc58b5cf2adf825d88c09b7aa1242e3dcf02dca5d4292f578608`  
		Last Modified: Thu, 09 Oct 2025 09:23:21 GMT  
		Size: 6.6 MB (6550908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5aea76393c5a8eca6886b8423022443a807fc6002b19d1731053e629841385`  
		Last Modified: Thu, 09 Oct 2025 09:23:22 GMT  
		Size: 1.7 MB (1705995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d80519c33274bda25939fb303dadbb8fa861080e6c7e5bc148654530b6ac7d7`  
		Last Modified: Thu, 09 Oct 2025 09:23:21 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:a2f9fc6e1f8f3eb79183c9a842f60fd17e3d3ccc1ecf87a0ce485fec42cbf21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70a554a8f6e7796dd5364efc6f5a46b13e11db7f18e8b50dbad09db02b9ba4c`

```dockerfile
```

-	Layers:
	-	`sha256:588ef1d3726aa217ce18597b719b3a1bc1d7df0ae51e0fe9d34dd6649926f1ce`  
		Last Modified: Thu, 09 Oct 2025 12:52:32 GMT  
		Size: 277.5 KB (277533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1042f7b6c8f08b0171dcee41f518d22bfd0bef4f4b41e8451f00c2bc7374a51`  
		Last Modified: Thu, 09 Oct 2025 12:52:33 GMT  
		Size: 20.2 KB (20185 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; riscv64

```console
$ docker pull caddy@sha256:0fde6a6983fe51c0acb146b70eb8c8df63aa2bc912db989644f4f223de50d8fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70576538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0464cc1a52bea2da627b70a70b28c91bee9bd256aeebd16f1e2366efbb7c71`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cc4f79972d3401fde161bf76b9618d80cbd1ea7fcdbebdc630185f4cf612cd`  
		Last Modified: Tue, 07 Oct 2025 14:20:26 GMT  
		Size: 291.6 KB (291608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d54fbaaf4f44943b5fd17aacabad20b0db0f29394c2b0f581a3a300b124c2`  
		Last Modified: Tue, 07 Oct 2025 19:40:12 GMT  
		Size: 58.7 MB (58670209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eb0ec517215215e4738f4ed22dccbdd571638b449e06fb45910fe6c13bf32a`  
		Last Modified: Tue, 07 Oct 2025 19:43:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69d23250e929faa84021b94619116bd3d245f4b59453f1b9172309f0ea5f8da`  
		Last Modified: Tue, 07 Oct 2025 21:59:32 GMT  
		Size: 6.4 MB (6377120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ecbd34bf74a90b357655ba06e701f98148120c832975f78a0f26f1d93d585b`  
		Last Modified: Tue, 07 Oct 2025 21:59:32 GMT  
		Size: 1.7 MB (1724209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52857f9761fe43fb0c131c352f082b495d4cd959e4651c18ae99ea17e899675`  
		Last Modified: Tue, 07 Oct 2025 21:59:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:3fd3f490dd581cadae05918741ee7b9fd4e06a249219588518ef0789c509a6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 KB (298796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cb3367c1fa6ae06bb44aebc276e6ec5e71f05f64300383031fec74acdb8029`

```dockerfile
```

-	Layers:
	-	`sha256:e6102514bee60ceb228d8c7e9d26aedbf6a0158de3052ace6739b4fdab282f28`  
		Last Modified: Wed, 08 Oct 2025 00:52:38 GMT  
		Size: 278.6 KB (278612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620a83401f41c3e648853020bca837eb7ef9b9e651ba56af9d5272ddcaa6c030`  
		Last Modified: Wed, 08 Oct 2025 00:52:39 GMT  
		Size: 20.2 KB (20184 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:98920242c65eab10239e4c84758ed2bc8b4216836a7b13f4b592f1cec7f21b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71708809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db020283d3512a27f480d7e03a00e2429a1418ef056eae8d49818b76cd7501d5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 23 Aug 2025 03:19:59 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Sat, 23 Aug 2025 03:19:59 GMT
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
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2de0d30ada31da192f5016a4897bdd65bd1ab1a8a13dcbc1a8bf1e887eba8f`  
		Last Modified: Thu, 09 Oct 2025 02:39:03 GMT  
		Size: 292.2 KB (292158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ba33a49b3f3080422ca98d26430f3e1c1ba8f8f41bc6d8af4cff9843f4da`  
		Last Modified: Tue, 07 Oct 2025 19:36:10 GMT  
		Size: 59.5 MB (59478805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc1af17613180179944931e348017c6e19f85695f4ebedf0ef0a4eeb22ea448`  
		Last Modified: Thu, 09 Oct 2025 02:39:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0a41e2ef3ff108c69c0e0b3144aa8cd58e2feb0927600996328071f0a9f331`  
		Last Modified: Thu, 09 Oct 2025 13:54:19 GMT  
		Size: 6.5 MB (6505157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2392e571c0181b82b28a8c9074cdefa649fdc18af33f68f52f8b0efcc1aa5aa`  
		Last Modified: Thu, 09 Oct 2025 13:54:18 GMT  
		Size: 1.8 MB (1782855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa2be4cd0f96430f078b4f9c5177dd3e86e13aa5f4a1b5bcf7bbb19d35ce26`  
		Last Modified: Thu, 09 Oct 2025 13:54:18 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder` - unknown; unknown

```console
$ docker pull caddy@sha256:28a69b3fbfbdd53cac5da619a3456ceb1ba572c547a66f64b53b34735cc5a243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 KB (297576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1687e3205d21a0f95fa479c4e968a0825fd5427deecd303dc99a8afd43a01d80`

```dockerfile
```

-	Layers:
	-	`sha256:c6d2f48a410db58c729a2278b131b8e0f9554919704ec088391f6a6d4d3c77dd`  
		Last Modified: Thu, 09 Oct 2025 15:52:38 GMT  
		Size: 277.5 KB (277461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:597489ab03446fb6edbca3d6af3168c171caa256c775f12f4842847c2d7141da`  
		Last Modified: Thu, 09 Oct 2025 15:52:39 GMT  
		Size: 20.1 KB (20115 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder` - windows version 10.0.26100.6584; amd64

```console
$ docker pull caddy@sha256:45612766f9a81d040ec6c38dcda8c0455f82675c787f46af642574668eda6fcf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3687922565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba592b60b4afe8e5dd88a965b2e75f33799aa9d07e1142c80b4cdb1a7d7096`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 07 Oct 2025 19:33:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 19:33:56 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Oct 2025 19:33:57 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Oct 2025 19:33:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Oct 2025 19:33:58 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Oct 2025 19:34:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:34:33 GMT
ENV GOPATH=C:\go
# Tue, 07 Oct 2025 19:34:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Oct 2025 19:34:39 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:36:19 GMT
RUN $url = 'https://dl.google.com/go/go1.25.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c18b46f6aa44dbfcd54a9db19dd2fcc5ad684819addcfcf968aa75dad89a89c8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:36:20 GMT
WORKDIR C:\go
# Tue, 07 Oct 2025 20:11:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:11:31 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Oct 2025 20:11:32 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 07 Oct 2025 20:11:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Oct 2025 20:11:40 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 Oct 2025 20:11:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c930722fa7c27b5f2ebcabd1d48f0ae46ca0f73ac356015926639bd386b929`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f28534faffd08baac64096bd10b6745e014b7345aa17e28356aa9db4ff8fcf8`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829a0f666da6074e2b2d567760a1c76ed46b9da380d7ceadb553a8ff3e3c728b`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec59792f5ba5dfb0c092b355a01157fa49d5881b9558abb40f0cbcf7e144c45`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888bb4f563cdd2d81289f9ab878ad6566ef787bbae76c658fc98d85d3cb2598d`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4ce5bd76392c952d3a401ad4ff2c1028c1cfaa77a6594dc331317b2e5a6097`  
		Last Modified: Tue, 07 Oct 2025 19:45:11 GMT  
		Size: 51.2 MB (51237312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccf4b274abdacf8985b388b8c531bcb842d9e84a3a790ecc872d9be15580667`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5490d449e6678ba6cbc1af67fd8e2a19ea2e0e33e61e92de62454328c02474d`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 353.2 KB (353221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3babdd19ee1f6f0d71eaf042b33d45818541c9f05cb69ea225a414f423538a1f`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abb5f4d05f51b0eed124d4766c0914601db8a25f062531d1db8aed39da68eb4`  
		Last Modified: Tue, 07 Oct 2025 19:45:21 GMT  
		Size: 62.6 MB (62578590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b07091315c7619c64765c65e948733b3b88385392d329c100de65fcf269bc`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.5 KB (1505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1699e8b8ec682fbfd5d7a69ad44d06ee2a7a6d9fa92c538d93183380abc31668`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4a55ed9c24500af4d1b69c57e99fe8c8aabdd88acc1a21fd0af8ca4fd504e9`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08082371c55bb8748e92920c154a9739b61d89eb49ef69cd48027b5f3a865a08`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bdf4936d055887737af4dd9bdcf868c33ec70faeba6aa38a3979066820fa22`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3991ee4ba1b9bc9782085d8a7cf422965b5e26f5434396f9da6f5b2a1ea7026`  
		Last Modified: Tue, 07 Oct 2025 20:12:07 GMT  
		Size: 2.3 MB (2296398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4713c6cdcce2284960a5122353d9e92f4db330eaf5bc65daf7a8cf3897e28fcc`  
		Last Modified: Tue, 07 Oct 2025 20:17:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - windows version 10.0.20348.4171; amd64

```console
$ docker pull caddy@sha256:715492b0f944cd127eb6bbb8a4c0cc689f7707fa7a5e2b472fc6452b4f07b90d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2398610240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c6d1145422423f4bf0e98d89ef4f0a046b691c5549c52870927143d9f07d39`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 07 Oct 2025 19:34:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 19:34:31 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Oct 2025 19:34:33 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Oct 2025 19:34:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Oct 2025 19:34:35 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Oct 2025 19:35:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:35:38 GMT
ENV GOPATH=C:\go
# Tue, 07 Oct 2025 19:35:44 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Oct 2025 19:35:44 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:37:16 GMT
RUN $url = 'https://dl.google.com/go/go1.25.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c18b46f6aa44dbfcd54a9db19dd2fcc5ad684819addcfcf968aa75dad89a89c8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:37:17 GMT
WORKDIR C:\go
# Tue, 07 Oct 2025 20:12:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 20:12:28 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Oct 2025 20:12:28 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 07 Oct 2025 20:12:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Oct 2025 20:12:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 Oct 2025 20:12:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Thu, 09 Oct 2025 10:32:05 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84669fff65b3c9be81e40b9990f09af6d79236a36c89b48837a2c56193e23d4`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e60c3731686204945190028a490513225d391212a27fae945d09b2858d31e55`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d31081e3081cc502401b5490ba7207796e551806afd0270bd8a99cd079aeb`  
		Last Modified: Tue, 07 Oct 2025 19:46:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0ae39107ec10a072379114022d2a65f0876026a506d6d97879b0690375ff5a`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448a9e7b99aa2b469a3ce0476da3574a6f1a3fd1a31ab60d087e3b241be8b602`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad8795f0cd8577898069910151345b5cceb653b95293f0e07bd3ef305d4b319`  
		Last Modified: Tue, 07 Oct 2025 19:46:21 GMT  
		Size: 51.2 MB (51222673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b85e42e9abcbae149b2e2d9b074fa1b76e74cd88f54622eaef24b9ea51ab81`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d664c422bbdd3f488f9b864b914e4867001ad3abd4164492dce75542a29e954`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 353.6 KB (353616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3564e813d9de7e1f20fa71a8b4a152f09f76719c04ba40966f67fbefadab5d`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02b4977a05998859250a8498907467403796eda2afc717329e301fd821c6f1b`  
		Last Modified: Tue, 07 Oct 2025 19:46:41 GMT  
		Size: 62.6 MB (62575489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fb0b5a044068825be258eb2d74f38322a83d5679674bb7247d7c482011f670`  
		Last Modified: Tue, 07 Oct 2025 19:46:12 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd774b4fe59f6b1be84c9ca72d0ec51480732efec0d929ef8e9b38c2a3fc89dc`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c00883df518d9fb471f8a5583a0e58e0373a64e003dc5396513f3f766eec53d`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7881cce5aa1a5935de2405658071a0e5b1d9661b5487bc3c9aa9f53b6c5c10c1`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b38591ce3e10db96fe64de0a8ebc6f65514f302b2028d68b100a86fadde6d60`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aececf11534a88cf9a95165200a3a9f75ba72ec567775b4df9c7d596afc439f5`  
		Last Modified: Tue, 07 Oct 2025 20:13:07 GMT  
		Size: 2.3 MB (2296303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efede2e44e94f6e665f2ecf900a0cd611dff2a029759937c9b5a480d4b3df131`  
		Last Modified: Tue, 07 Oct 2025 20:13:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
