## `caddy:2-builder`

```console
$ docker pull caddy@sha256:d57008618f743e6308058d7bd990eb3489dfd04e2b82978cca7b953e1b491fc7
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
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:db3ae9a5913d5b9305c729247b8ee6ca7596823a3a9419eaac330e5f374c3157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79773771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591706032a9a5c14da6e7f446e0083d6747768d50d0bf9da36e55c2421e94a2f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:53 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:53 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:55 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:11:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:00 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:00 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:00 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30edd47abbca5172a1775d1ba8a17aef65500a7a1ecc50af582706ad0c19ab`  
		Last Modified: Tue, 02 Jun 2026 21:45:09 GMT  
		Size: 290.2 KB (290247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aaa626ba3010d60ab55d9cdc69c0b12ebff5d1b5ece83ff220fb46a7709b3b`  
		Last Modified: Tue, 02 Jun 2026 21:44:37 GMT  
		Size: 67.3 MB (67283031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abecc8ee46932a01c961a896c3c87dd0efe1301916e124bdac46f96ae6e9dee`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4922139842e28e1d61aaac141bc8576337fa9b8d64d1d9f723d161fb30612`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 6.5 MB (6489213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa1420c37ef3c625b9f14ee901574c588fc49b3eb5a8fca1a8a732fd47620b`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e306254cc3a4dab0c2ccd0f548ad566fa5aa81a412b9b432d81889526a2bbf2`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ddd773e864a4f4e091e1f4bfdbd60371b4c51910be5ccb610589b8a6883de8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 KB (300905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4dc9d9bcee8d699bb42f311997ea36c642596e4004aa8859d0781b30ac2c9d`

```dockerfile
```

-	Layers:
	-	`sha256:d055d9682529a9387da6c4adbc8bdc265d0466484002fca96e29c90f179091be`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 280.8 KB (280776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490b4b762d29e23f9c30e7d63d2f4fde87253b5f126903cfd336647e4cf6c3af`  
		Last Modified: Tue, 02 Jun 2026 22:12:08 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:67c97e86bbcf6c6d84c8a191e6f9c07550c3ff25bfef23d3e8ee6a6407d6d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77801132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8375fe7e15b17bead87deaac11514fa70da1cd8427509b1c228967a15f141eb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:01 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:01 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:15:26 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:15:27 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:15:27 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:15:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:15:27 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc79104d8e3b9e93b7ff3163839b44dd0979c52b2f81f68e01be8f60d9d090`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 291.0 KB (291036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb989b4b1329f80799d899b8d7259a6658047b39b2b670ed0cc8620dd1d357c`  
		Last Modified: Tue, 02 Jun 2026 21:44:18 GMT  
		Size: 65.8 MB (65785954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e947158a0266891a134507f0a6253aec12f2c7656af2daefbed99f399148f5`  
		Last Modified: Tue, 02 Jun 2026 21:44:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620327b269f4fa8f6e186115a4ab2a342dedb497a9044abd4a5b3246f11d3ac3`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 6.4 MB (6406685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a7c7f37dd2ddabcd39c4ec78c16b8efaf799e1db677a0a88c55ba2bd16132e`  
		Last Modified: Tue, 02 Jun 2026 22:15:32 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037287d5c994a910febeca5542dc101d590c0256e293e25e7ddb97f4b25eba7b`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:ee8a613597922f4a0c6ad805948acd213e018eb8e3548ca5b98e7cb6c0410659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a997af74d3004a92cc163aa5d9f843ecd7552d9fad60e39cc23d5f4340ebdbd1`

```dockerfile
```

-	Layers:
	-	`sha256:b77f8ee7de0cc1af47105376a1a978c3bd700001392879cba9b348c38f53c909`  
		Last Modified: Tue, 02 Jun 2026 22:15:31 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:081203e78dbbdf584d644a704dbce3dd01e8d923760b1e4160a615e9c0282f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76958176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cece6d48bcb1d2e37ff13a3299d3382dd7c3a18c66cd620c334b6e7e45b85c5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:44:42 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:44:51 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:44:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:44:51 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:54 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:48 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:48 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:48 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:49 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12aa788fec666273423bc95c719209c3f49b0d2c1c28fdaf669e4ebcab932954`  
		Last Modified: Tue, 02 Jun 2026 21:45:08 GMT  
		Size: 290.2 KB (290169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f46eeae83dd5d801ff20835cd1ea98f630698b9c066e10ddf320a1c9d42c07`  
		Last Modified: Tue, 02 Jun 2026 21:45:10 GMT  
		Size: 65.8 MB (65786124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494a0eb08b28e7075149245f5ff666eeadec03e6b1b08870ad1caa24151d00b`  
		Last Modified: Tue, 02 Jun 2026 21:45:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba6d2d27897ace71b8214e93839ab4dddfb4bf51e5dd9871755073b452fd92`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 5.9 MB (5859405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d200f1ff9040ab5ed074d40e2c5d715e5ca869a8c3c9ca357f24b30cc08f2`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 1.7 MB (1738762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392245d1b10f490bef242becdaf6b658edb173425508af51312e2d0c7703b3c5`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:0207715e319528107b0ca90c4b3ae044a8636067b8544656cf7cfa660dbd93d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 KB (303422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd6848c1a5afb6c01dd7ed0eea80f86a4053eb96a8d94f50bbb86131989d4a`

```dockerfile
```

-	Layers:
	-	`sha256:dda72704ff023245a1d0202ebcabc8675ff1d722be6ba03fec1b7ce479c3a68c`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 283.2 KB (283168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac1a6806382a02068a2684ad9fc775685c890f3913b65b2de640fe3eca324e6`  
		Last Modified: Tue, 02 Jun 2026 22:12:56 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:13da9d8308a65d8402c19528f51e19a2535fcd2f28ee893feabfefab09afb838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76951883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114e448de61888adef08f63408e9426eb63ce6db5c2c1066219d9ba0222717c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 21:43:51 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:58 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:58 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:01 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:12:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:12:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:12:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:12:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:12:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2c0198c180cf41cbfd73e25946fc0ccc373d0fee89deb6e7eeec7b1f8612ee`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 292.9 KB (292861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a477eaf154b7c8070862d9db01681f78c8a60ce90e8936310f6a906696df475a`  
		Last Modified: Tue, 02 Jun 2026 21:43:59 GMT  
		Size: 64.2 MB (64166971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cb4739b26b76346d1281fb8fac14c5bc8025bfc580405cc95aa21736e41116`  
		Last Modified: Tue, 02 Jun 2026 21:44:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98e7c04c5116e56a4edea922d39e62c3fe0cfb06ee580b89926af1db83402ce`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 6.6 MB (6575206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb57c7a67944f4fa914947979e30a6c1db54ab3c9b1aac79a9ebd7b36e8e39b0`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758ee51343f308260ed7fa9020154c216542e21fd2589bc41d85b57f77166a81`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:9613ce914fd434a8d09e7d2f73c5c9b354b42cf9c31d65fefbe292f23eacb6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 KB (300526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbed50fbf772e7e0ff9b816eb3a8dc3e213df0f8c75ba10dc5924412b0e4d841`

```dockerfile
```

-	Layers:
	-	`sha256:add9c054a1ac3653aed38da164cb08126bb46bb4bc153c6f12848191bed15b4b`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 280.2 KB (280230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838bb928d6772b6ebe8d87d60a85b358fd40eb2166c93cb622cee8a22a537ca3`  
		Last Modified: Tue, 02 Jun 2026 22:12:59 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:658d12b9b7e489cdf05a0115f8fd9c8e392ee3160ba5b96d5f6b1e3cf0e02802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77577921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2568f1df66f499486924dad3ad55e9449d549bbb37426e3354addf15c6c7df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:47:20 GMT
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
# Tue, 02 Jun 2026 21:44:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:44:18 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:19:34 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:19:35 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:19:35 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:19:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:19:36 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dfc45c5906cb105fa1bde6a534e8e48deced0c4556f99056c2f76204caa5c2`  
		Last Modified: Tue, 02 Jun 2026 16:47:39 GMT  
		Size: 293.4 KB (293393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94153723d1545849cb54e33c3f8f977f110afcb00da0d5d32236b24537c1a4a3`  
		Last Modified: Tue, 02 Jun 2026 21:43:46 GMT  
		Size: 64.8 MB (64840550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd4ff149d61b69213dc146324696a7a3af1a2b46684c6f928dfca1ae8489a0e`  
		Last Modified: Tue, 02 Jun 2026 21:44:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3cb06425959c67588985a91f934858685c3d7e6f0a3094af6c96ef93508d2`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 6.9 MB (6906465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966eded362018ac5d0b34cafa47d109cf32bbdeac194c1582640c28fd31f3cb0`  
		Last Modified: Tue, 02 Jun 2026 22:19:53 GMT  
		Size: 1.7 MB (1705993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88bcc980b0c8d2d3de3ae12ec5a268bf23ac450cf0e10b8726131fa5f50dd3a`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:636aaf3183699721a688bf9903f4a642af3556d22fb14b8142bb3d77e9e02f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4888dfc41af739498c0157e20326f403f56cd8400b521203907e2cce1bfb8403`

```dockerfile
```

-	Layers:
	-	`sha256:00729d38b67285f7a79eb306240810accdabec647d996c8e36ab458f490a827c`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 280.2 KB (280199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ec6cfbc1bfecb50f2c2e12352351ad7a86aa62458697127bd6d635c92ce4cb`  
		Last Modified: Tue, 02 Jun 2026 22:19:52 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

```console
$ docker pull caddy@sha256:851cb908798b1538ffe3a3053bb98a32903f158a7f1ca9eeafb0fa30f6f34f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77424217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1dfc4a9d5f64621b356f7b47c6c48337fe32d5912cfc96a0484d5c999eabca9`
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
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 05:24:32 GMT
ENV CADDY_VERSION=v2.11.3
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 05:24:32 GMT
ENV XCADDY_SETCAP=1
# Wed, 03 Jun 2026 05:24:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 03 Jun 2026 05:24:32 GMT
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
	-	`sha256:d0b5d5e4441c4e23a30ad21c2b66c3a336df57c4bfda44ff5113b5b3be8e2ffc`  
		Last Modified: Wed, 03 Jun 2026 05:25:48 GMT  
		Size: 1.7 MB (1724208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa80fdf8a500696ba07bd03f2a260b2e578f3e7909bec500d7122de9d25041d6`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:dca192295748614e125d445ca613cc0972469b2e1774dca65dd6b47fe9d2682f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 KB (300394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a911353b6377828995df9827f453d124992e5ff9b7484ef6ebc4da9d7258c820`

```dockerfile
```

-	Layers:
	-	`sha256:e5bc98528c0380ded7049be92a37c9302d44d983dd53bba1648e04dedd55efb4`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 280.2 KB (280195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb92a4e503b3fefa7c0f01279adf8084dd01665b4d68fcef6d623b33d866cb16`  
		Last Modified: Wed, 03 Jun 2026 05:25:47 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:4b90e008693f441e0c5337ba3fedad55597c1c61e2ecf25f2241f3a878b58d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20cee611b412138469260e614e91691e6b1868b70e66aabd6488d8013d7cf3ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 16:41:58 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Jun 2026 21:43:02 GMT
ENV GOPATH=/go
# Tue, 02 Jun 2026 21:43:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Jun 2026 21:43:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Jun 2026 21:43:04 GMT
WORKDIR /go
# Tue, 02 Jun 2026 22:13:49 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:13:50 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:13:50 GMT
ENV XCADDY_SETCAP=1
# Tue, 02 Jun 2026 22:13:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 02 Jun 2026 22:13:50 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42ca9f29dfa6d3e969a05d12ba4b1dd9465b2ec31113dd62c26050eb7eeae28`  
		Last Modified: Tue, 02 Jun 2026 16:42:25 GMT  
		Size: 291.2 KB (291162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa95f9225fe123215e56024e7fcaa3f2eb9fb3081c2d6160ebae532ca6d5eefd`  
		Last Modified: Tue, 02 Jun 2026 21:43:22 GMT  
		Size: 66.5 MB (66513822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9138885877e3f590d4144dfc2ec737113acde73b99374df82c5be8c2901f3dd`  
		Last Modified: Tue, 02 Jun 2026 21:43:26 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91584af5ed277f32349e17cda1214326d518b9f94719dc5c4e741329ee86f375`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 6.8 MB (6779991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30090c473a211354bad44ab67b863187e6614231a73dcf0aa22173ee79b1a359`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 1.8 MB (1782842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3da51a38e8b113b744ea5418d02a52a6b6def3db40a219f602fa5e52065bfb`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:578a971dec1e6528eb9512ec7c3c538b18cbeb2a8d6c72b4f420d6992b30009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 KB (300254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f17854159ec165c92bf0e0220d91246d07bd68f48b8fa569c16a68552d0058`

```dockerfile
```

-	Layers:
	-	`sha256:4915df098870636a12ece0bc09cc5fc8dee8954c6116a7cfb93bf9f3169bd426`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 280.1 KB (280125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97af12336dd47a218f778a32b9bf8cf6ecc4d8ef33a28f7bb8c621a730e6343b`  
		Last Modified: Tue, 02 Jun 2026 22:14:02 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:6bac99d1de9debbb801646208c923809fe18cbb945c6d430cc8f1d38c5ba14ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45bc764ed6ce43900c66e7269ef9b64bff9f78aca8a5412c2bdddba4456a779`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:33:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:33:57 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:33:58 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:33:58 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:34:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:34:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfefceaacb32ce75c4aaba58b81bced50aae117cc616944d49a92ce10e866b2`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897cbe5e09e88bd391baaa18698e2d8eb277aa581a683b8025c4f230f1adf7e`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4b32c912e804ac74f332ad5ab2d2b281dc7e6d481f6f80a4f43df475616659`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f053ec3b21275df3413b9168645d21fb9bb677da4c1d6c12e96049e54cabfcd`  
		Last Modified: Tue, 02 Jun 2026 22:34:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1f65dcb82cba9c705872f745be1ac11720b8c76eebbe4e9942f2f2e810cf7`  
		Last Modified: Tue, 02 Jun 2026 22:34:43 GMT  
		Size: 2.3 MB (2345713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bbcd5aef19be6456c21bb9609b574709a6500a0642321c9435e2421d39818fd`  
		Last Modified: Tue, 02 Jun 2026 22:34:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.20348.5139; amd64

```console
$ docker pull caddy@sha256:5c6e7364201194ab26b433feaf24cec26dd47fa67d0191fd5aac9a3145f2d75a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2246342426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4817db1df805c59c442b0aae0af3740b59c437f926600e3382586defd6c6bd84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 22:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:11:59 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 22:12:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 22:12:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 22:12:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 22:13:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:13:36 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 22:13:42 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 22:13:43 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 22:15:53 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 22:15:55 GMT
WORKDIR C:\go
# Tue, 02 Jun 2026 22:48:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 22:48:16 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Jun 2026 22:48:17 GMT
ENV CADDY_VERSION=v2.11.3
# Tue, 02 Jun 2026 22:48:17 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jun 2026 22:48:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jun 2026 22:48:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16556704259948e469d295ad17c0b83303b045ecaedafdd2e16e153313e1dfb6`  
		Last Modified: Tue, 02 Jun 2026 22:16:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d711fc9f348f8b578e18995374d27b40e5900dd346ce6989dbf8a03d6379ed3`  
		Last Modified: Tue, 02 Jun 2026 22:16:04 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591205aec584bc9bf82bf950d86511bf856df5b80cfc692ffebf5597ca68b7e6`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22c20181a321c9aa31806b3a6299f064d89d5be9ef4ec4b8643e9648f096b20`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3875bb11e80c093d7133bdc63d9eae1ac2b5c3615c2548955f18ce7dc1cbcdd1`  
		Last Modified: Tue, 02 Jun 2026 22:16:02 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec55ad5b4586a55352fbd4acd5057d226c2736b7bf5617ba58c7b1ec5a01595`  
		Last Modified: Tue, 02 Jun 2026 22:16:08 GMT  
		Size: 51.4 MB (51351865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8157f646be5f683d250a6f17ff707476c9c8021878b249e269ce011d3ff874db`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363dcd54d5e980b27d8e067e3aa0681d0a3b914f0cd2fee65597fc3cc09fecb3`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 347.5 KB (347472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89e7d73520ffce5ef45fce95d33eb59c6e81aa2a9b702762d10955702c63f88`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03786a5498c3138a7f68d31bb4b48bba38614a87e19b581dfb213237d20256`  
		Last Modified: Tue, 02 Jun 2026 22:16:12 GMT  
		Size: 69.9 MB (69908615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717522dbb34fae4042da878f0e2b02e156afeb7efa63dd68f87a0e670c1777a0`  
		Last Modified: Tue, 02 Jun 2026 22:16:00 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c100a71c72bd8a3ae733ff302b773d79c1f9d9567e2ea92e5a14cabfad16946`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7973c59f163b420ad3e89ff70cbb614dd936a7c672446a4f96680cf7ea2033b1`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e23746fb5a19760542ceaf1982c31d671001d1e61c45ef53459e38fe02213c2`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d27ae839dc6cc7d7a119bd9b2c302ae49b265e40e36003baed2d882a8b80f`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415c477003a7c45c620ddf022beae3a2649f87cdd579da1617144d132e961953`  
		Last Modified: Tue, 02 Jun 2026 22:48:31 GMT  
		Size: 2.3 MB (2296661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5287c072e6ec74e531802fe71a613d30d89698c4a47bc8e3f1ca00ee98a1249a`  
		Last Modified: Tue, 02 Jun 2026 22:48:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
