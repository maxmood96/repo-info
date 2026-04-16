## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:1e770e28d9fe30cc199850a038d5046b942b87d1a17fc07f2f7117aef5e7d23c
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
$ docker pull caddy@sha256:a933556c29a031e3c70b54813e8ab1e78223c608ee6a4d28a37712b583a8a357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79797276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c775a1a3336e255042d46d7838902b6358b321f724ad2ae84b513fc24f92f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:35:18 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:35:25 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:35:25 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:35:25 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:35:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:35:25 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:35:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:35:27 GMT
WORKDIR /go
# Wed, 15 Apr 2026 21:59:45 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 15 Apr 2026 21:59:46 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 21:59:46 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Apr 2026 21:59:46 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Apr 2026 21:59:46 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 15 Apr 2026 21:59:46 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3aca1499f06ff02939c8f744463049feecb3965f1319b86b5e91790a9631e6`  
		Last Modified: Wed, 15 Apr 2026 20:35:40 GMT  
		Size: 290.2 KB (290242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55da06e3b41084804b2e5dbba71d35d26478b19ba8055d07a393cae22e9935f`  
		Last Modified: Tue, 07 Apr 2026 21:13:57 GMT  
		Size: 67.2 MB (67220501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973f1b4898e9c2c22c54ff9d1bc2e2d45d59d4c2e53c60281dde84ef43df4c79`  
		Last Modified: Wed, 15 Apr 2026 20:35:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd13beaa21b2fdfeab9c4009df7d5fec607cf31002866fd1cd4b827c9aa9f0e`  
		Last Modified: Wed, 15 Apr 2026 22:00:09 GMT  
		Size: 6.6 MB (6575253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5305edff610a3d0428163646659186d7addf172dcf154b1eaaec7c72cd4c0f6a`  
		Last Modified: Wed, 15 Apr 2026 22:00:10 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662c9183e063ce4c225f0ec3a17d3abcd8b5403f5aac9961c824c3801314a6ef`  
		Last Modified: Wed, 15 Apr 2026 22:00:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:eb8ff0bc747a21fc9eabfa3c191a33d2448474c68e8225d41e553d620c39bd42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 KB (302499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb0ca09cd5177abf3f5b00d35cb0ac8bce5df99c6ef8a755e6c4d2f9b0360ef`

```dockerfile
```

-	Layers:
	-	`sha256:cae0ed77407c18cc2f20b6ed67f1a8ecf74b54a1378d46931643d8cd1909d6ad`  
		Last Modified: Wed, 15 Apr 2026 22:00:06 GMT  
		Size: 282.4 KB (282370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9369cb56bfd16ca30b712419f4f05e457263dc07a9b99401fa8b72e2e955b5d3`  
		Last Modified: Wed, 15 Apr 2026 22:00:05 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:d4a0da3708131fef71ef541cea4dad2ae2388299de865dce2a6e69f8a2af8e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77844571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf655f5856b81e633cf9bce8b127cd39606014afea7b18504ff6c521ac863c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:30:46 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:31:41 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:31:41 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:31:41 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:31:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:31:41 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:31:44 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:31:44 GMT
WORKDIR /go
# Wed, 15 Apr 2026 21:26:18 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 15 Apr 2026 21:26:18 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 15 Apr 2026 21:26:18 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 21:26:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Apr 2026 21:26:18 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Apr 2026 21:26:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 15 Apr 2026 21:26:18 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 15 Apr 2026 21:26:19 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c5793b7330baba2bdbdcfc15c9c30a01c808c080ac6caa02bf3b5585d2f0b`  
		Last Modified: Wed, 15 Apr 2026 20:30:53 GMT  
		Size: 291.0 KB (291020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e327e2b14e32d059b1daa22f82c1fb7fa98060bc20d47dd6686da42229cba8b`  
		Last Modified: Tue, 07 Apr 2026 21:13:32 GMT  
		Size: 65.8 MB (65751024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff205b28ed383fd21ca44ed521626fb5d29207a307ecbcd118b32b80d9f4d7`  
		Last Modified: Wed, 15 Apr 2026 20:31:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc572b2d570cc6a112e7787de08db3b1ae38b29f96e302726663bb3344b6c57`  
		Last Modified: Wed, 15 Apr 2026 21:26:23 GMT  
		Size: 6.5 MB (6485072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67034377cff32a591fd5e7581dee2fa329fd9e17fa41cee43d1b6d3dc6021504`  
		Last Modified: Wed, 15 Apr 2026 21:26:23 GMT  
		Size: 1.7 MB (1745001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d37c6afc2b09444fcd7ab435f379383d45052c1b8cf26c39a48cee080245882`  
		Last Modified: Wed, 15 Apr 2026 21:26:23 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a3bfdf810d2e46621e383526c835b30472411595f32d43fe8be17764f09bd287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2091d766955eee4746dd16967ed4c2284bb0ddaa3c61548f561298815d5d0b2`

```dockerfile
```

-	Layers:
	-	`sha256:b6f5022420389e1ac3c64e0102248ce1a2b458f1dde6190be6df97236784836d`  
		Last Modified: Wed, 15 Apr 2026 21:26:23 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:579dab0404ed6e0b6a7dcfc21f23af098674b15ef33c57e4ac8834534cc227ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76998141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a97153921a6338bb0c2bfc216194174d4ae0c8438296e84a04d3694b2e793f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:38:49 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:38:57 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:38:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:38:57 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:38:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:38:57 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:39:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:39:00 GMT
WORKDIR /go
# Wed, 15 Apr 2026 21:40:05 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 15 Apr 2026 21:40:06 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 15 Apr 2026 21:40:06 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 21:40:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Apr 2026 21:40:06 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Apr 2026 21:40:06 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 15 Apr 2026 21:40:06 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 15 Apr 2026 21:40:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3ba670b4c9b2ddf01d859a649370597580dda4e52512417fb0791b9dee3e0`  
		Last Modified: Wed, 15 Apr 2026 20:39:14 GMT  
		Size: 290.2 KB (290155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3c0c93980268a0e43ceabcbfa19841d8859d03f3623b4521a7ead3d6e1badd`  
		Last Modified: Tue, 07 Apr 2026 21:13:54 GMT  
		Size: 65.8 MB (65750977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4507fefe92406dc44db071c79b3b8d25445798810ce36b9e7f4459278f0b10`  
		Last Modified: Wed, 15 Apr 2026 20:39:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b21d833b62f87475e29de301e10d0e894f4f1fb3fba693ee57fad88138dda25`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 5.9 MB (5934541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e253d406d4b31660c7010c58ad0857e1b3a1ae06ee7c335cd38b49caa1639`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 1.7 MB (1738756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5dfd37b2b467466648b98b89ac88269f678cb31637b8d3ad80e82c2c4b5a4`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:42cfec51b143eb79fc46dc737eb1a7b1d034c31c1f9ca2c54080982a8bba9525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 KB (305016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0222f886947371458138267c54c53e322043c5906c2fd510f0859325ca2368d4`

```dockerfile
```

-	Layers:
	-	`sha256:8208491786ca21eb11ef262615c593cc8b0a55099fadb6e57c4fc374d4d734c7`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 284.8 KB (284762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3328792f4c08d239c7618365cf12fd92fbac200121a4ad0b6b198750ae9945d`  
		Last Modified: Wed, 15 Apr 2026 21:40:14 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a856882573707cbfeff41ee191c699d84c634da091af083e40c6731a195a90bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76976731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96da546473e378d8fdba2f83bbc5c4615373991d509360ba0e457be3eb443e39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:35:32 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 15 Apr 2026 20:35:40 GMT
ENV GOLANG_VERSION=1.26.2
# Wed, 15 Apr 2026 20:35:40 GMT
ENV GOTOOLCHAIN=local
# Wed, 15 Apr 2026 20:35:40 GMT
ENV GOPATH=/go
# Wed, 15 Apr 2026 20:35:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:35:40 GMT
COPY /target/ / # buildkit
# Wed, 15 Apr 2026 20:35:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:35:43 GMT
WORKDIR /go
# Wed, 15 Apr 2026 22:11:53 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 15 Apr 2026 22:11:54 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 15 Apr 2026 22:11:54 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 15 Apr 2026 22:11:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Apr 2026 22:11:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 15 Apr 2026 22:11:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 15 Apr 2026 22:11:54 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 15 Apr 2026 22:11:54 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89244935705494e38d5fa051ae5221080d8446b496516d3888d3cb64c7a7d51f`  
		Last Modified: Wed, 15 Apr 2026 20:35:57 GMT  
		Size: 292.8 KB (292841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e89efc4b5ec39fa30d639b12ad2c7fd994a11ffa608e77427a882d73768d76`  
		Last Modified: Tue, 07 Apr 2026 21:13:44 GMT  
		Size: 64.1 MB (64108758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e813a1647e7ea7745c1c15436c1f86a82eadb5436933163091db860d16ed923d`  
		Last Modified: Wed, 15 Apr 2026 20:35:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f47fd971bb6b95ce849f6f8c10fb7ce093e2702ed004661ddb3371996f7aa9b`  
		Last Modified: Wed, 15 Apr 2026 22:12:03 GMT  
		Size: 6.7 MB (6658285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d79316e527f1c7fa66f132b86e688f5902ed133f22c0df2e5f161b51d84203f`  
		Last Modified: Wed, 15 Apr 2026 22:12:03 GMT  
		Size: 1.7 MB (1716384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc277e7bd628f5b4228fac6953184d5c86babf2181457ddf870cfe33e336aa1b`  
		Last Modified: Wed, 15 Apr 2026 22:12:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d3748d7f759f5b95071e1232c4a1601d234bca875f2a205e3d533a94afba1553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 KB (302120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3918aaa9c32df9dded7f5d38493cc8f2a63d10d59ac273d891f0531b66840260`

```dockerfile
```

-	Layers:
	-	`sha256:6510bbc75b701965f310f53955909ac3a9893055288ee593905558f4056e4d0a`  
		Last Modified: Wed, 15 Apr 2026 22:12:03 GMT  
		Size: 281.8 KB (281824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68782e2b3cfb84c0ead772416218c19e174253dde329832fdd999b537679e0d8`  
		Last Modified: Wed, 15 Apr 2026 22:12:03 GMT  
		Size: 20.3 KB (20296 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:63b759413cedfce94857f811ff24bf4f16722ba78f52f2d6fa932636e37d8077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77586607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c16a668c0d704966b7aee5b27f48f5e6c597b77bd23bb8ce4c7c01776d3041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:28:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:27:19 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:27:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:27:19 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:28:48 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:28:49 GMT
WORKDIR /go
# Wed, 08 Apr 2026 02:40:53 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Wed, 08 Apr 2026 02:40:54 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 08 Apr 2026 02:40:54 GMT
ENV CADDY_VERSION=v2.11.2
# Wed, 08 Apr 2026 02:40:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 08 Apr 2026 02:40:54 GMT
ENV XCADDY_SETCAP=1
# Wed, 08 Apr 2026 02:40:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Wed, 08 Apr 2026 02:40:54 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Wed, 08 Apr 2026 02:40:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c157c37b8ca35f88bf66161b72bc1761ade8e543ac3a14868075a68b5dff95e5`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 299.3 KB (299270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59cd64739ee2c1db9b4eb7c08338d6773eef47b2c94a225b64cb228ac665cec`  
		Last Modified: Tue, 07 Apr 2026 21:29:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d7660240a58a343791f9ddfc593fed679ae836be1f5efebfdd6c616d996c61`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 7.0 MB (6993346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3367975427940e88bc1d08204bc0b02e3d5825c56364e6c9d4c4fbabea9e42a8`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 1.7 MB (1705992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9459b8d487af4148880bab184d49b8cc5d3cd615a2b79b4bc57198594109b007`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:e24b0b95b5c9fe33e5128c1c08cfca98e2d51b29ab6b4b419b981340b9989e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788a1a3c73ccac753cb34992ca5abe9acedc402f240ba6ec60c211aa65c01bab`

```dockerfile
```

-	Layers:
	-	`sha256:01cac4bdcfc723c6d6bf41140df184150407905a42d81a66c7ec9ca42136f591`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 283.7 KB (283748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acbe01d6b3aba68e1719acfe1806d184952ff5eafd14a564dacd6744586d81c1`  
		Last Modified: Wed, 08 Apr 2026 02:41:09 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:061764f40bbb07975c70576eef0ba931894ff4be8adf309d33d2a92cd4f90c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77451742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638708ebdea0f4f9ba216b2947c6112c4a1ed589aa89bf74c0ca1d5cd745763b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2026 08:51:29 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:31:22 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:31:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:31:22 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:31:40 GMT
WORKDIR /go
# Sat, 11 Apr 2026 21:09:24 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Sat, 11 Apr 2026 21:09:25 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 11 Apr 2026 21:09:25 GMT
ENV CADDY_VERSION=v2.11.2
# Sat, 11 Apr 2026 21:09:25 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 11 Apr 2026 21:09:25 GMT
ENV XCADDY_SETCAP=1
# Sat, 11 Apr 2026 21:09:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 11 Apr 2026 21:09:26 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 11 Apr 2026 21:09:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653a48053074547bb1f8e43c4e508d8a803d45b52e98210c3539d09ceb870090`  
		Last Modified: Tue, 24 Mar 2026 08:53:11 GMT  
		Size: 296.5 KB (296514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18820a12075d850af6085d052799ca6c42481c33ddc318143f5caa48480e4d17`  
		Last Modified: Tue, 07 Apr 2026 21:34:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc15650f7980fbf7a29c9e27c7b1c34c70c9e717c7e182174c904a0c55105760`  
		Last Modified: Sat, 11 Apr 2026 21:10:47 GMT  
		Size: 6.8 MB (6751286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3749dd26165bd4355faf91142f39910cbda5876e1dc4cf4dab9fddf2554fd`  
		Last Modified: Sat, 11 Apr 2026 21:10:47 GMT  
		Size: 1.7 MB (1724209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a25c28e9947ea6e2c6000af587456747f7aa3e55efa5c7eadf4a007e844b3d`  
		Last Modified: Sat, 11 Apr 2026 21:10:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:cc81ed4864c4f09898f412d01a8eaff9537e120ba4be38a625b82a6ee7addefa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 KB (303943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9def5331bf193c0ea89a0eccb20423a36caa6cc7d600ff96b97342b281b6039`

```dockerfile
```

-	Layers:
	-	`sha256:d19d6adde38b5da7d5191598e003d9bb649d2083eafce71d538afdc41b8df1d3`  
		Last Modified: Sat, 11 Apr 2026 21:10:46 GMT  
		Size: 283.7 KB (283744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ae938f7d1610628dd37ea8092027495f22925a718f97c11ca6796d6c7b1f203`  
		Last Modified: Sat, 11 Apr 2026 21:10:46 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:eb106425c2387dbc6faf5dd55a484ef040bf0cfa8cc00f67e20d66124ae964ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79099900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9c84295d8be77d8ae7ac50aff7ac12c9bf4eaaa26b76cc49c7fd1a3105cbe2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 21:13:30 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOLANG_VERSION=1.26.2
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Apr 2026 21:13:11 GMT
ENV GOPATH=/go
# Tue, 07 Apr 2026 21:13:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 21:13:11 GMT
COPY /target/ / # buildkit
# Tue, 07 Apr 2026 21:13:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Apr 2026 21:13:40 GMT
WORKDIR /go
# Tue, 07 Apr 2026 22:04:17 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Tue, 07 Apr 2026 22:04:18 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 07 Apr 2026 22:04:18 GMT
ENV CADDY_VERSION=v2.11.2
# Tue, 07 Apr 2026 22:04:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 Apr 2026 22:04:18 GMT
ENV XCADDY_SETCAP=1
# Tue, 07 Apr 2026 22:04:18 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 07 Apr 2026 22:04:18 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 07 Apr 2026 22:04:18 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09b3320db87c0fbe713adce5ff43836b299964a204ab829de72270c3d2d4c3`  
		Last Modified: Tue, 07 Apr 2026 21:14:59 GMT  
		Size: 297.2 KB (297199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8b98e3267789cad196300f0ede7760a8353c331b3221d7fb9a3a72d8fbfdf`  
		Last Modified: Tue, 07 Apr 2026 21:14:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29b737ea8ec9d63365ff60c8b99e726ff26aa8514f669bb267ae37f69899128`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 6.9 MB (6861734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b7ddcbac288653a375c431efa9f8af6443cf4a3c5ae9782b10be536504644`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 1.8 MB (1782858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f29edf9e907c0fa4161754bbf36af59b2935e2c722f9fb74dbcd3a6a5f1544`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ca448a2154011b1db01eda252697e59d68aedcdae5e41b7e88a50340a6b7313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 KB (303803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4e0ab570344fecd612ffc77eb9ca78f2ccc6246f882cad274c477a2ded8192`

```dockerfile
```

-	Layers:
	-	`sha256:6676fb82501162c57b41e7f1c6453d26500db360347fbdf3179464bf46be0564`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 283.7 KB (283674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632d4c353f354beac0125d53b75d1105e3ea2144de4689874b46f12b90f6c591`  
		Last Modified: Tue, 07 Apr 2026 22:04:35 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json
