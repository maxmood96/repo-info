## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:556058bf580e6323f34adae8e59c09647b4f08e14e2a35b71936c9105e6d8305
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

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

### `caddy:builder-alpine` - linux; arm variant v6

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

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

### `caddy:builder-alpine` - linux; arm variant v7

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

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

### `caddy:builder-alpine` - linux; arm64 variant v8

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

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

### `caddy:builder-alpine` - linux; ppc64le

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

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

### `caddy:builder-alpine` - linux; riscv64

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

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

### `caddy:builder-alpine` - linux; s390x

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

### `caddy:builder-alpine` - unknown; unknown

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
