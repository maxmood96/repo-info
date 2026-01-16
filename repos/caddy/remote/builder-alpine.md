## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:20ef083ddfa3ff8bc8e8243fa376a835345978b60f0e40229042b52d8b18a3c3
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
$ docker pull caddy@sha256:9c6ce6bb84af334f98a0abdbd2c09a0a4ce13c29c18347f38388cae217b2bf04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72334246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733fb1f5656733f4a6edc9e0e8c748c7ff6e9c46db6c3e6fce946b9949510d03`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:31:16 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:31:22 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:22 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:22 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:22 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:24 GMT
WORKDIR /go
# Thu, 15 Jan 2026 21:45:11 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 15 Jan 2026 21:45:11 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 15 Jan 2026 21:45:11 GMT
ENV CADDY_VERSION=v2.10.2
# Thu, 15 Jan 2026 21:45:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Jan 2026 21:45:11 GMT
ENV XCADDY_SETCAP=1
# Thu, 15 Jan 2026 21:45:11 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 15 Jan 2026 21:45:11 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 15 Jan 2026 21:45:11 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04359908d71f40ff9248e788f307d4f87b0a4b94cb454f132b639e7f0ec8ecf`  
		Last Modified: Thu, 15 Jan 2026 19:31:42 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c503e035cd5c1ea67986d21ed1fb2f4305f801555c52f9f16ce0f0f5cf2e16`  
		Last Modified: Thu, 15 Jan 2026 19:31:22 GMT  
		Size: 60.2 MB (60154290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f623491ce62a94ef5702034414027a10617289994624ce3648ceaac425f6842`  
		Last Modified: Thu, 15 Jan 2026 19:31:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a610b60633bfb359e663d41a9c9fb8c5d7cb4cebe5693a0b7a4ca81f9378ae89`  
		Last Modified: Thu, 15 Jan 2026 21:45:26 GMT  
		Size: 6.2 MB (6239248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5711fce0f6468eff27032d9df0e0ad9751141ee71a618d526538d0b09485d7`  
		Last Modified: Thu, 15 Jan 2026 21:45:25 GMT  
		Size: 1.8 MB (1846503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3fc2d0002a014c2ea8fe684fd58f030513d2d502c59098fa1270e14b89f2b2`  
		Last Modified: Thu, 15 Jan 2026 21:45:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:9c6b7baef7640e6f2d202ebba3772758e5e75237f23eaae75e9f72db574e17de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.5 KB (299484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e97507d62f1e0d9d685d25c52c17d5f5c6a6d87e52e5bf7d21cd32e4f97f4d`

```dockerfile
```

-	Layers:
	-	`sha256:2400b86dc26fd7ca18d07ab7c0c40dda477117c74c59a188247d984cd2d24bdf`  
		Last Modified: Thu, 15 Jan 2026 22:53:25 GMT  
		Size: 279.4 KB (279412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6807bdc49638ce5122af487cdcd68bd8a73245562354a47b8f630f892b123d`  
		Last Modified: Thu, 15 Jan 2026 22:53:26 GMT  
		Size: 20.1 KB (20072 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:17d7897a875aeaff719a9b7d5178f66e265fb6770f957f044bc12eb608ddbd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70770041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f4be2ef20d52a0e1f547aaf6d7f2b1439725aa3ceb1ad76835c1c5078e03d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:30:53 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:01 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:01 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:03 GMT
WORKDIR /go
# Thu, 15 Jan 2026 21:43:24 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 15 Jan 2026 21:43:24 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 15 Jan 2026 21:43:24 GMT
ENV CADDY_VERSION=v2.10.2
# Thu, 15 Jan 2026 21:43:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Jan 2026 21:43:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 15 Jan 2026 21:43:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 15 Jan 2026 21:43:24 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 15 Jan 2026 21:43:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a232bd9335f4d8ecafc77b46310417937667c2826d90bef350cb29dd7b441a3e`  
		Last Modified: Thu, 15 Jan 2026 19:31:21 GMT  
		Size: 292.3 KB (292312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9281733a6226838b038c2bdb015b61227dfc767db0d5160e59d01708503f8e5c`  
		Last Modified: Thu, 15 Jan 2026 19:31:32 GMT  
		Size: 59.1 MB (59073822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df32dd2d1c9739a4a386ae3c7570d64272629b8b46a9a5e0c5b5268cb3853658`  
		Last Modified: Thu, 15 Jan 2026 19:31:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0592c0c2a47ee2788a0032a4695ad7e0f4184c86d094243441be9919a4baacd`  
		Last Modified: Thu, 15 Jan 2026 21:43:36 GMT  
		Size: 6.2 MB (6154234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175f375c4f1b5b03b08b2b91c888454a590a239181d74d6d498318a288f242c3`  
		Last Modified: Thu, 15 Jan 2026 21:43:35 GMT  
		Size: 1.7 MB (1745000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eec18cf0f288b8ebb00885ca2693c0780ce9882753e2433b423e6f913432b40`  
		Last Modified: Thu, 15 Jan 2026 21:43:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e3f047c5c9bcf8264c189929f420884dab4f5e887db214a01597ee9e2e9842eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (19982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d9af980009b9870afae0c071048f85caa648912748593be9bcf4c64f27e11a`

```dockerfile
```

-	Layers:
	-	`sha256:a57fe2399fada9f9b8c2cee4796fc0ca4476d0649739a2c384ee20a62ee997b9`  
		Last Modified: Thu, 15 Jan 2026 22:53:30 GMT  
		Size: 20.0 KB (19982 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:df40e29fde6a27b7693feae89f29976b5d95187a319e924389a2b4aeba81a9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69955318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70cffdd4de5635d60c0ca53169266b7efcea85b25a58a85f1fd2a5a1881453cf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:29:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:29:47 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:29:47 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:29:47 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:29:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:29:47 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:29:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:29:50 GMT
WORKDIR /go
# Thu, 15 Jan 2026 21:48:06 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 15 Jan 2026 21:48:06 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 15 Jan 2026 21:48:06 GMT
ENV CADDY_VERSION=v2.10.2
# Thu, 15 Jan 2026 21:48:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Jan 2026 21:48:06 GMT
ENV XCADDY_SETCAP=1
# Thu, 15 Jan 2026 21:48:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 15 Jan 2026 21:48:06 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 15 Jan 2026 21:48:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Sun, 07 Dec 2025 13:57:17 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1fa75c1ae467d2f90d851bf512fe8db3431ae8f08fc808154bb8bf0c7f04fa`  
		Last Modified: Thu, 15 Jan 2026 19:30:23 GMT  
		Size: 291.2 KB (291207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9858bd230951a4669967b265976b2f7dbd9f374059998fadb8d8956bf7de2a2`  
		Last Modified: Thu, 15 Jan 2026 19:30:32 GMT  
		Size: 59.1 MB (59073810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc8c3d3f494f5d77bcecf38517d8a38d28a73e2588d1893c20b5fba6466b73a`  
		Last Modified: Thu, 15 Jan 2026 19:30:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1bb8205efb5c1608bde66a29bf92d3852f9b94d14074fb75a5e3b5ce33d816`  
		Last Modified: Thu, 15 Jan 2026 21:48:20 GMT  
		Size: 5.6 MB (5629398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdb402f4c82621334101468ce79e6195572517ee30d65db904888d60f989ea9`  
		Last Modified: Thu, 15 Jan 2026 21:48:19 GMT  
		Size: 1.7 MB (1738758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa3bfba36737395dd12b753d20da1051725c01a28548f30fa6795632b9f295`  
		Last Modified: Thu, 15 Jan 2026 21:48:19 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f58e625eb9693d59317897691c938851c204f17f8797a9194ea207a61686cd0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 KB (302652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7200a52f5d7affe6e8529d8effc2b2d305777c6153ca153cb8f7fe0eb93019d3`

```dockerfile
```

-	Layers:
	-	`sha256:88d773c5062f0e398a29cccc545fbfe891f464507fdff558123bb730fa50a7f9`  
		Last Modified: Thu, 15 Jan 2026 22:53:33 GMT  
		Size: 282.5 KB (282456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e47b05f3a8736f4d2b13a6a81f7cdf779803f16991aea6a4948422dabf70e13`  
		Last Modified: Thu, 15 Jan 2026 22:53:34 GMT  
		Size: 20.2 KB (20196 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:012626f22b10d73f62a0dde5ff04e5e604775198cd76a2feff4ba12489a88af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70099353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c605fb81391a37e76b20dd12e4692854278763bf8251a5cf93f45efa695321`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:31:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:32:06 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:32:06 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:32:06 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:32:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:32:06 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:32:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:32:08 GMT
WORKDIR /go
# Thu, 15 Jan 2026 21:45:23 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 15 Jan 2026 21:45:24 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 15 Jan 2026 21:45:24 GMT
ENV CADDY_VERSION=v2.10.2
# Thu, 15 Jan 2026 21:45:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Jan 2026 21:45:24 GMT
ENV XCADDY_SETCAP=1
# Thu, 15 Jan 2026 21:45:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 15 Jan 2026 21:45:24 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 15 Jan 2026 21:45:24 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7794a9a5c43f3decb40710e694b07c837f04f174b527f22507335eb2ad0f7b28`  
		Last Modified: Thu, 15 Jan 2026 19:32:25 GMT  
		Size: 294.1 KB (294100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a2f381e4cd3963e3af5194953e3e2807c452e833bf69397dee70610e428e6`  
		Last Modified: Thu, 15 Jan 2026 19:30:48 GMT  
		Size: 57.7 MB (57659196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3af9a7c43f543ae2eefe2ac716712963d2a64f7f0e040856f25c539ef93396`  
		Last Modified: Thu, 15 Jan 2026 19:32:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6022abdf8653c5a157f41f3a1070dbff5e4bba612f27bf7f90e575f167928166`  
		Last Modified: Thu, 15 Jan 2026 21:45:39 GMT  
		Size: 6.3 MB (6291015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf5444d0f98ed1513ea3ca7dbec5b110710ddde52fa0e115ae7501ec3927d46`  
		Last Modified: Thu, 15 Jan 2026 21:45:38 GMT  
		Size: 1.7 MB (1716381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909f51dc1aff16f4a170ab8497e1fa624f50d5ed605f9edbc8bb92089212eb7b`  
		Last Modified: Thu, 15 Jan 2026 21:45:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b8c53dfc1f03e807e33f820874bcec3d841c0a9eacbdced96fb41ed6d7b7f376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 KB (299755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed622ce1dad85c4d61618076be27ac916640c7dbf1d43ebf034b6abf37c2dd30`

```dockerfile
```

-	Layers:
	-	`sha256:93be72c7459e51495b03e6076ac032f2cfae37f42752f483f39b65cb04d81b91`  
		Last Modified: Thu, 15 Jan 2026 22:53:37 GMT  
		Size: 279.5 KB (279516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e33e401da1fcc22ab5e9a54c60b323152d108ad01f1d85cc07315594d65f70`  
		Last Modified: Thu, 15 Jan 2026 22:53:38 GMT  
		Size: 20.2 KB (20239 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:688edec04413cdb2080a9815f6a58ea2adf72c0aed372f07e6d5f9db91439b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70449706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de6e69fa5a1cbe8822a84306e65c4e7c5a266cceedf37a47ff67b3242f3e4aa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 24 Nov 2025 22:43:33 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:15 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:15 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:33:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:33:44 GMT
WORKDIR /go
# Thu, 15 Jan 2026 21:53:34 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 15 Jan 2026 21:53:36 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 15 Jan 2026 21:53:36 GMT
ENV CADDY_VERSION=v2.10.2
# Thu, 15 Jan 2026 21:53:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Jan 2026 21:53:36 GMT
ENV XCADDY_SETCAP=1
# Thu, 15 Jan 2026 21:53:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 15 Jan 2026 21:53:37 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 15 Jan 2026 21:53:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Sun, 07 Dec 2025 14:06:45 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64958bce21ae47528776dd8bd6794140e1f5086c72ae8807ba8f48bb37fce769`  
		Last Modified: Mon, 24 Nov 2025 22:43:59 GMT  
		Size: 294.6 KB (294592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de1d7ce58974e33ace56f0654af975ba4e29402893e2d90d191005bed4dae95`  
		Last Modified: Thu, 15 Jan 2026 19:32:34 GMT  
		Size: 58.1 MB (58135270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e052c5c16761da78755f52c5f66e215087c00201c99b1a0c31fb9e28000716`  
		Last Modified: Thu, 15 Jan 2026 19:34:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaf18bde59b0557d1f039d54f43cbe0571fc101f2c8725334e8833b8a8aa186`  
		Last Modified: Thu, 15 Jan 2026 21:54:04 GMT  
		Size: 6.6 MB (6581018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c50549e1a4a707778534496c459d7b3328ace569fd7fafb962e0ac2103b87e5`  
		Last Modified: Thu, 15 Jan 2026 21:54:04 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279e9a5eba6c1b853875978646b52876c78b77d3afef3cc1df19cda5f6115840`  
		Last Modified: Thu, 15 Jan 2026 21:54:04 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b0b9b734c6398b10d0c0c5109d7a18107a076f3a25a2858c504bd717c46f96ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a641b4e42e0cefced7db468499a0575ca84e282a605113684697ca5676b17761`

```dockerfile
```

-	Layers:
	-	`sha256:daead294447179825bbff67d24eb9cc25e5ba522626c6882ddfb76a045223d68`  
		Last Modified: Thu, 15 Jan 2026 22:53:41 GMT  
		Size: 277.5 KB (277533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4608557bfd56cd6df8e823ab720b960ec25baea293bf58d49b37642b1b50766`  
		Last Modified: Thu, 15 Jan 2026 22:53:42 GMT  
		Size: 20.1 KB (20142 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:94446f1b948644e339625b04d36bfee884f2b497bb10c3df4ac80f800eed1437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70600188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4cbe9ed08ca9800aa17d567cc7b5623d0b559f1ac57911d88577160bd78eba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 25 Nov 2025 07:20:45 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 17:47:21 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 17:47:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 17:47:21 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 17:55:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 17:55:48 GMT
WORKDIR /go
# Tue, 02 Dec 2025 20:25:32 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 02 Dec 2025 20:25:34 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 20:25:34 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 20:25:34 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 20:25:34 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Dec 2025 20:25:34 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Dec 2025 20:25:34 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Dec 2025 20:25:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Sun, 07 Dec 2025 22:49:04 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a984176d166c6f9d398140e2c603deed3f1a52311d2a418b830c1cfdaffb3c`  
		Last Modified: Tue, 25 Nov 2025 07:22:38 GMT  
		Size: 291.5 KB (291523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f6199a15922cf0533082f2bfb9bf03dc54fb7fdb4f830e8dae324efa57d8b9`  
		Last Modified: Tue, 02 Dec 2025 17:54:10 GMT  
		Size: 58.7 MB (58672443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dece81b84dd08929374b6e8e9e38b7015785ac31adf38602fb02b1dbd442d0ce`  
		Last Modified: Tue, 02 Dec 2025 17:57:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126003ba150c1d5c3ec1cc51aedbdad1ff2ebf9cc0346d5c6a5fdd1d040e342`  
		Last Modified: Tue, 02 Dec 2025 20:26:55 GMT  
		Size: 6.4 MB (6396184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eeb197d3bfdc8bb806a9021109891a57c69fa39569a30c23c297202ed71e065`  
		Last Modified: Tue, 02 Dec 2025 20:26:54 GMT  
		Size: 1.7 MB (1724207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41546e4c12ec170a76a9f2e04e2c0eb7f230662517ed451e92d5205f26adcd3d`  
		Last Modified: Tue, 02 Dec 2025 20:26:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:292e1b44a7b48d3c100f5cd9b786cfa30d1ea6dd902c3d27792c33f984758965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 KB (297671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ed4c766112c346341ef2ea370fcb59c276aa431a7cff99ca97c7cdef3ee21`

```dockerfile
```

-	Layers:
	-	`sha256:f3b3ab1c4b1ae7d0dc06a93a06151880fb6d4a385b5f0c30139001e4e02eb78b`  
		Last Modified: Tue, 02 Dec 2025 22:52:32 GMT  
		Size: 277.5 KB (277529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a57413cc0ec68e6250d1502ca3e0e071b769f341d9aa645aeea01e235aeadb7`  
		Last Modified: Tue, 02 Dec 2025 22:52:33 GMT  
		Size: 20.1 KB (20142 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:4c1dd33a8d5f799aedad695e77e138d0e85c064267cbcc7cefce946e77a17a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71746863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc35da77265ffe3d61420d5081817d5d87e08e9fdc8fef9a006865168a05dde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Jan 2026 19:31:03 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOLANG_VERSION=1.25.6
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOTOOLCHAIN=local
# Thu, 15 Jan 2026 19:31:09 GMT
ENV GOPATH=/go
# Thu, 15 Jan 2026 19:31:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 19:31:09 GMT
COPY /target/ / # buildkit
# Thu, 15 Jan 2026 19:31:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 15 Jan 2026 19:31:32 GMT
WORKDIR /go
# Thu, 15 Jan 2026 21:48:15 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 15 Jan 2026 21:48:15 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 15 Jan 2026 21:48:15 GMT
ENV CADDY_VERSION=v2.10.2
# Thu, 15 Jan 2026 21:48:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 15 Jan 2026 21:48:15 GMT
ENV XCADDY_SETCAP=1
# Thu, 15 Jan 2026 21:48:15 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 15 Jan 2026 21:48:15 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 15 Jan 2026 21:48:15 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Sun, 07 Dec 2025 14:06:46 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4477625ae0958d0e9b2655402cac23110eb0328923e9ab75f1482f7e600bb6`  
		Last Modified: Thu, 15 Jan 2026 19:31:45 GMT  
		Size: 292.2 KB (292153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb26ceadf9d37827849921e4f034b2107b0a7ec09f97f2b6301929ee5e50569`  
		Last Modified: Thu, 15 Jan 2026 19:31:47 GMT  
		Size: 59.5 MB (59491172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1efd5513f6831bc017ed1d81af029b50d24695b60f8ff591b9d0d2788fe7438`  
		Last Modified: Thu, 15 Jan 2026 19:31:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c1d374bbfb334b4c73d950e4067f6273e49eabb53bfc053e3908b89d64193e`  
		Last Modified: Thu, 15 Jan 2026 21:48:33 GMT  
		Size: 6.5 MB (6530861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586fd5f6dd11d21db362fcadfb92a7a5236e782b4031dadc5eb5bc0d08b14181`  
		Last Modified: Thu, 15 Jan 2026 21:48:26 GMT  
		Size: 1.8 MB (1782843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e58852377fa96054d9c3f9ca29e88c8a457be1274cf0c0b3c8d0d86e1fe902`  
		Last Modified: Thu, 15 Jan 2026 21:48:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:25375648892dd173b7d45ebcf4a6f3636889af2726bf959ce5216e970b01e09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 KB (297532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6629438831ec8eb1698771a37a65e29e99c79dee8cc7a178aa70a2ae6c5ab321`

```dockerfile
```

-	Layers:
	-	`sha256:90407aa9de338308fe76a0d269d3a6bcd1d0fbee46094815c43b20e519e0a206`  
		Last Modified: Thu, 15 Jan 2026 22:53:48 GMT  
		Size: 277.5 KB (277461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1242970cf41bd31f03af115a04f40b6af9da38f6107f269a85c61943c6801cc`  
		Last Modified: Thu, 15 Jan 2026 22:53:49 GMT  
		Size: 20.1 KB (20071 bytes)  
		MIME: application/vnd.in-toto+json
