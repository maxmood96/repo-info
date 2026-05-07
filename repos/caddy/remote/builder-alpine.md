## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:8eeb041bbd45456046f0761bf0c1df49807cdb2723863e96cf40087797ee9212
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
$ docker pull caddy@sha256:9823c0aa283cf35aad12fc79caeb471a2f22de814ef7c7479a4733a41453bf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79861705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bb31f8bd0754f3bda2e78aece79e90cc7c8659600a671f36d4ff9ea479604a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:37:38 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:36:58 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:36:58 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:36:58 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:36:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:36:58 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:37:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:37:46 GMT
WORKDIR /go
# Thu, 07 May 2026 17:43:53 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Thu, 07 May 2026 17:43:53 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 07 May 2026 17:43:53 GMT
ENV CADDY_VERSION=v2.11.2
# Thu, 07 May 2026 17:43:53 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 May 2026 17:43:53 GMT
ENV XCADDY_SETCAP=1
# Thu, 07 May 2026 17:43:53 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 07 May 2026 17:43:53 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 07 May 2026 17:43:53 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17423c887b377ec28c3923bc88337384a7a0c1f2b50b7faf4912760e8d503ebb`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 290.2 KB (290240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70bdedd442d430ea119cf8db8c0031b4eedeb5bde886892773876ded7629e8`  
		Last Modified: Thu, 07 May 2026 17:37:31 GMT  
		Size: 67.3 MB (67285082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1512b43389a873b0519ae3d6c1a3c4d9b19295b8e3330b040d95d73c50ba2f9e`  
		Last Modified: Thu, 07 May 2026 17:37:52 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e211a6761192300122bcc0e39545cbe199e5a443a17c6b7663bd29168c5ad2`  
		Last Modified: Thu, 07 May 2026 17:44:02 GMT  
		Size: 6.6 MB (6575103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc1047ce12b1fe5583b403ae47cf30985588b0e5582825ba225306fc3dcd008`  
		Last Modified: Thu, 07 May 2026 17:44:02 GMT  
		Size: 1.8 MB (1846501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0979d628322a82d166e9f2be3ae7b6228a089d67c2842027f2ddfc3115befcab`  
		Last Modified: Thu, 07 May 2026 17:44:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:81b639e275606e806dac2a0e7e1e8929d49e90f3c6104d1c2084f0a835e365dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 KB (302499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadb5db93735f1c3c309a8c067811e2c616178f642fd28af02f5d11dbe8db993`

```dockerfile
```

-	Layers:
	-	`sha256:571fa499b6637114961bea27548a910f99b97ae14f9ddcbb24b9c231ada7cf02`  
		Last Modified: Thu, 07 May 2026 17:44:01 GMT  
		Size: 282.4 KB (282370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:578b8748f33bf9e1090d7cb22b67ff8f85db43abbb10fba8c203c74a15b17a04`  
		Last Modified: Thu, 07 May 2026 17:44:01 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b2619bfcac03332357c1c31f24b69923607eb31ace34c94c327de39c1a0ad054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77880862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bc4f90f04330677dd6bc7698367fbab9eb31bb43b81d3f0427ef1abf8056bf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:56:43 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:56:53 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:56:53 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:56:53 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:56:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:56:53 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:56:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:56:55 GMT
WORKDIR /go
# Thu, 07 May 2026 18:16:54 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Thu, 07 May 2026 18:16:55 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 07 May 2026 18:16:55 GMT
ENV CADDY_VERSION=v2.11.2
# Thu, 07 May 2026 18:16:55 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 May 2026 18:16:55 GMT
ENV XCADDY_SETCAP=1
# Thu, 07 May 2026 18:16:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 07 May 2026 18:16:55 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 07 May 2026 18:16:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687009092f42112fe3060ede6d29f6140685d07bebd8ce3ea35a0e9641d52139`  
		Last Modified: Thu, 07 May 2026 17:57:07 GMT  
		Size: 291.0 KB (291027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323b6bdac241fc54c2e0e06ca7f4045ec740c882bb235caa36f634f6857573cd`  
		Last Modified: Thu, 07 May 2026 17:57:09 GMT  
		Size: 65.8 MB (65786523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdf014bd07811d672a2f4f8f1dfc9d69bb5aaea6fd7943530bece2bcc12c3f8`  
		Last Modified: Thu, 07 May 2026 17:57:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa73bc682ee507300dcb170005ccd2c8ea6ef01ec52345c6c4369f90d14f804`  
		Last Modified: Thu, 07 May 2026 18:17:00 GMT  
		Size: 6.5 MB (6485856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da3b7decc219d7d6e55a7f319802c5ede9ce1411726ac59f73a169a44b454e`  
		Last Modified: Thu, 07 May 2026 18:17:00 GMT  
		Size: 1.7 MB (1745002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be280ef18a6905a699a5fcd35e7464c9b3abece545ae51ccd4a38f8f5cc413ff`  
		Last Modified: Thu, 07 May 2026 18:17:00 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:ac26d9100dba1dba75209e104a492a53e2cd0cbd6b0485a8e4ab0b382bb0a27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219b3d2fd5fe367eae15443fd482393878631d68e8f3fd66739786e5514d7faf`

```dockerfile
```

-	Layers:
	-	`sha256:abd2abcaffc002a17f6a508f73240825c7ed4ecf624458128cda985d251dcb2c`  
		Last Modified: Thu, 07 May 2026 18:17:00 GMT  
		Size: 20.0 KB (20039 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:aeb722b328edce41f998871795a06c7ac5f89a5264555e7cc79b049a1a466cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77034066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a59f45dfb169584f0462bf10ada11b1ed808eecb8864754c4e2bdd7aab6b31`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 18:01:20 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 18:01:29 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 18:01:29 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 18:01:29 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 18:01:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 18:01:29 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 18:01:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 18:01:32 GMT
WORKDIR /go
# Thu, 07 May 2026 18:16:59 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Thu, 07 May 2026 18:16:59 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 07 May 2026 18:16:59 GMT
ENV CADDY_VERSION=v2.11.2
# Thu, 07 May 2026 18:16:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 May 2026 18:16:59 GMT
ENV XCADDY_SETCAP=1
# Thu, 07 May 2026 18:16:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 07 May 2026 18:16:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 07 May 2026 18:16:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edfdc54fc8b2d0bd0428faa39d6e4e185d5561d50ba518340fae16d2e464d2e`  
		Last Modified: Thu, 07 May 2026 18:01:47 GMT  
		Size: 290.2 KB (290164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e7137c96fc07d2fc9e87f7cec43a327dd6c1385057f6c469907ef731cca2c`  
		Last Modified: Thu, 07 May 2026 18:01:49 GMT  
		Size: 65.8 MB (65786476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1a80c7896f8a764b0302d7643726ecf90ebdd66bc34ddaccaed3b25748d797`  
		Last Modified: Thu, 07 May 2026 18:01:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8181f8a4e6e6730b57b77e1da9ae199089c998bfcbfa772807b8356f95b5d380`  
		Last Modified: Thu, 07 May 2026 18:17:07 GMT  
		Size: 5.9 MB (5934952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde1bfe1cf3a29ff9809757be10f0cf100a1e9d9bd1ef0f760d8a730b0f740ef`  
		Last Modified: Thu, 07 May 2026 18:17:07 GMT  
		Size: 1.7 MB (1738759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13afde0f97ec70b1cb59be594b89934dacfa8fc50640d724004c559b64fb0f72`  
		Last Modified: Thu, 07 May 2026 18:17:07 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b1861d4c6bb8652fbb0afbcffc91f6d4dc864a44b5c71b730fac401e1f14e0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 KB (305016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12efcb5b9891894dc0597a5f63ac0b356c32aa6699a3369e83816890d87c9ebd`

```dockerfile
```

-	Layers:
	-	`sha256:a96d66983b939064eec67c6c0ab4ef422d73fe337b3cb0bdaf1141eb9efcf2a9`  
		Last Modified: Thu, 07 May 2026 18:17:07 GMT  
		Size: 284.8 KB (284762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00460eb9d12b4230c3a0ff831d120cdea59a7b0e32c159963e31481fe03ed83c`  
		Last Modified: Thu, 07 May 2026 18:17:07 GMT  
		Size: 20.3 KB (20254 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:1de4b021ea67d57eedfaafff8edbe929321015e73172213ba25f52820d7faced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77035774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca346b08d6ccdcc84ba811d5551f1bb00ba03d5fe81a4bf11c57e75b53bd79c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Thu, 07 May 2026 17:42:54 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Thu, 07 May 2026 17:42:16 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:42:16 GMT
ENV GOTOOLCHAIN=local
# Thu, 07 May 2026 17:42:16 GMT
ENV GOPATH=/go
# Thu, 07 May 2026 17:42:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 May 2026 17:42:16 GMT
COPY /target/ / # buildkit
# Thu, 07 May 2026 17:43:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 07 May 2026 17:43:03 GMT
WORKDIR /go
# Thu, 07 May 2026 18:03:12 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Thu, 07 May 2026 18:03:12 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 07 May 2026 18:03:12 GMT
ENV CADDY_VERSION=v2.11.2
# Thu, 07 May 2026 18:03:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 May 2026 18:03:12 GMT
ENV XCADDY_SETCAP=1
# Thu, 07 May 2026 18:03:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 07 May 2026 18:03:12 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 07 May 2026 18:03:12 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef948c355a7dc83c698cdbb853ce74cbea62b03bcdffec75a5ddd8453edb8fcc`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 292.9 KB (292856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fa76ba696f7dc4b9e2330d4ae7c03a0f4b2c055caa94b353f7f600a6dab0c6`  
		Last Modified: Thu, 07 May 2026 17:42:45 GMT  
		Size: 64.2 MB (64167785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e696fa36d88793f0869c86c611ba1d605ad3a2a7f60d00018579c8c2c9f935`  
		Last Modified: Thu, 07 May 2026 17:43:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3871bf288b7f1e89b2509e30403ad9393fbb10e672bb215aaed38d9e1e099f0b`  
		Last Modified: Thu, 07 May 2026 18:03:21 GMT  
		Size: 6.7 MB (6658294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd7c4f02eb7d7dde5325af3f8e7fb4a3e0644762845fb2e87f90e28ef7cb912`  
		Last Modified: Thu, 07 May 2026 18:03:21 GMT  
		Size: 1.7 MB (1716379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe432bdf4b211f4b067be191e7644522324eb630e3747d6bc3249594fe3a7a6`  
		Last Modified: Thu, 07 May 2026 18:03:20 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d61b05575a6c3982c7fdadcd29f0e7737655f07fe58fc0f73ff5f8a24b04b90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 KB (302119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2868671c1845313c10c8ee48bab9ce60e634cbd5759f4e258813b8ebb81bf9fe`

```dockerfile
```

-	Layers:
	-	`sha256:d463c7eba3d57fa03b6263022d8bd77ba95e1ed64b4f5298874dbde48b7b1d65`  
		Last Modified: Thu, 07 May 2026 18:03:20 GMT  
		Size: 281.8 KB (281824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3daab0800d810b91000e1ff45d8e0fd7a3f038e1b1e78de405e48cc3ac20b840`  
		Last Modified: Thu, 07 May 2026 18:03:20 GMT  
		Size: 20.3 KB (20295 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:e7fe67fa8f41c34c47083b2709b908f0d9488b9dbbd25cc0291ba6539bfd35fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77582244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e533592d17701109f227ce7eab67fedd2c318236ba44ac9c01c030d9148ca419`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:07:27 GMT
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
# Wed, 15 Apr 2026 21:35:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 21:35:20 GMT
WORKDIR /go
# Thu, 16 Apr 2026 02:27:02 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Thu, 16 Apr 2026 02:27:03 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 16 Apr 2026 02:27:03 GMT
ENV CADDY_VERSION=v2.11.2
# Thu, 16 Apr 2026 02:27:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 16 Apr 2026 02:27:03 GMT
ENV XCADDY_SETCAP=1
# Thu, 16 Apr 2026 02:27:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 16 Apr 2026 02:27:03 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 16 Apr 2026 02:27:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7ccd49384e7556733dfe66ba3c21432bf16a2524fd3822010b69719728c426`  
		Last Modified: Wed, 15 Apr 2026 21:07:48 GMT  
		Size: 293.4 KB (293365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fa701b604ea6f9fea3ed6559e2106d2a891e54c2977fbb8bdbf9d75d69aa40`  
		Last Modified: Tue, 07 Apr 2026 21:28:13 GMT  
		Size: 64.8 MB (64757766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0372cf4e623b54be68928792e5509486cabcf90908b531b460901e913b42b93`  
		Last Modified: Wed, 15 Apr 2026 21:35:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028542da0e085c654caa875682754ebfe8995d782d31d70f796fe355b5924c69`  
		Last Modified: Thu, 16 Apr 2026 02:27:42 GMT  
		Size: 7.0 MB (6993599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819b522902088506880ad78021ad70acb0772236493fb435e3e0352086be6078`  
		Last Modified: Thu, 16 Apr 2026 02:27:42 GMT  
		Size: 1.7 MB (1705994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b554dc0af36c2efed10695c848406ba85818963228c2fb5d2b5011a9e00f44b`  
		Last Modified: Thu, 16 Apr 2026 02:27:41 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:d2e0f9fc631eff25813caf4ac263a810aa757eb4aac19883bb238bde8ef0f474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 KB (301992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa34c96fbf5967686577c151ebd04ec1b45c0f139f72e0b078fa8a8237c410f8`

```dockerfile
```

-	Layers:
	-	`sha256:e6ff4860ce1eba66c986b7143734dd60900a2343129b4accd2e31338cecb95c9`  
		Last Modified: Thu, 16 Apr 2026 02:27:41 GMT  
		Size: 281.8 KB (281793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0f16b84a892627a2f2fb04e3bda467760880071ac66fcc9f8f8ad8492655d9`  
		Last Modified: Thu, 16 Apr 2026 02:27:41 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:702100cc6cb738583fe48f6bc94e6781c0ca8ab60450e45da1510224d10a5cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77448244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96617940106cf0ab245d1e93538ed2afeb3adadf880307554430115443cd97a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 16:18:44 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOLANG_VERSION=1.26.2
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOTOOLCHAIN=local
# Sun, 12 Apr 2026 09:58:49 GMT
ENV GOPATH=/go
# Sun, 12 Apr 2026 09:58:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 09:58:49 GMT
COPY /target/ / # buildkit
# Thu, 16 Apr 2026 17:35:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 16 Apr 2026 17:35:37 GMT
WORKDIR /go
# Sat, 18 Apr 2026 03:59:17 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Sat, 18 Apr 2026 03:59:19 GMT
ENV XCADDY_VERSION=v0.4.5
# Sat, 18 Apr 2026 03:59:19 GMT
ENV CADDY_VERSION=v2.11.2
# Sat, 18 Apr 2026 03:59:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 18 Apr 2026 03:59:19 GMT
ENV XCADDY_SETCAP=1
# Sat, 18 Apr 2026 03:59:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Sat, 18 Apr 2026 03:59:19 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Sat, 18 Apr 2026 03:59:20 GMT
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
	-	`sha256:4f7d1d0582748c5d1e12dadbe34ea1c9ef1815ea945fc3f044f96549146c6e58`  
		Last Modified: Tue, 07 Apr 2026 21:34:28 GMT  
		Size: 65.1 MB (65093854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fd72d900ad96a04e0615b341b3fedc269f4018f44079153195094e01751c01`  
		Last Modified: Thu, 16 Apr 2026 17:36:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98261c5a494e943c71e9f02a9fae234cd5f5fa47beefabe33105e79ee81b051`  
		Last Modified: Sat, 18 Apr 2026 04:00:38 GMT  
		Size: 6.8 MB (6751377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df08615ae0b43d83475265d726b6f1fb344c8df10917db9b12502f5e8ac1fd9`  
		Last Modified: Sat, 18 Apr 2026 04:00:37 GMT  
		Size: 1.7 MB (1724207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047b34906fcc87a21ca627c8887258847eb91e1dd6e22b3954673d79680676fe`  
		Last Modified: Sat, 18 Apr 2026 04:00:39 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:f8ba19f78e0fee4b05e9186cadf2561a17fad42319a5d94f34436cfd41b186ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 KB (301988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1802618434f74332d5a9f4a02848e7ddea67cb764a46f5bbe412ba6925a65d13`

```dockerfile
```

-	Layers:
	-	`sha256:f17a8970e76f50d906e98bbba74a9e9824556a63dc811deb5909a9fda1e8ba29`  
		Last Modified: Sat, 18 Apr 2026 04:00:37 GMT  
		Size: 281.8 KB (281789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01642a6207ada1d033df4b2d754385d9542ca42bd7925f8580d927d9a02f0e2`  
		Last Modified: Sat, 18 Apr 2026 04:00:37 GMT  
		Size: 20.2 KB (20199 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:023eaa1a2c908b10249f52b733650bbfcef905b2d98f11a40f9523f123417e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79094996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09659957f9b27684cfa4f20c3f82f6f8caa9e95c2b2319158b968535f2f3e44e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:41:12 GMT
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
# Wed, 15 Apr 2026 20:49:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 15 Apr 2026 20:49:24 GMT
WORKDIR /go
# Thu, 16 Apr 2026 00:33:32 GMT
RUN apk add --no-cache 	ca-certificates 	curl 	git 	libcap # buildkit
# Thu, 16 Apr 2026 00:33:32 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 16 Apr 2026 00:33:32 GMT
ENV CADDY_VERSION=v2.11.2
# Thu, 16 Apr 2026 00:33:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 16 Apr 2026 00:33:32 GMT
ENV XCADDY_SETCAP=1
# Thu, 16 Apr 2026 00:33:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='edea47d552fd9ac0a533386a72acaa95733ce734f347c11e5513469b5dc0eec0a62a6e21cfa93a83ab00b2dad72e0ee0b9bdf267a9654235f70d4c934739a15b' ;; 		armhf)   binArch='armv6'; checksum='29e4b7c484c0045d192fc8e7721c41988c1b8fc529343499ebb2acf94fba60f6e6c25c0944f7fb778ae25d5f8ccca452fc31d0338d6630d9b5219d5f9210ea44' ;; 		armv7)   binArch='armv7'; checksum='7e115fe60be169ffccff6884f1ab8fbe754d117c39618b02aedab9c857f0dcdc3cc6949f76b6a799cd617b509021bb086a4b2c5fb6c74d409d09429ff591a616' ;; 		aarch64) binArch='arm64'; checksum='2933968a6e759a0406dc864000960fe0e605db9f0fe0662ce245897eaa5b529e322d1b14c2b98463a95e13f1dfd85432541b41f459a237daedb8c68a8f6a5bb1' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='10e5f7e7dc885b278ebf4c5a97df4bde85a96fbc529890263f42af0445790a18669f44e318be1ac7639a283499e679ce9dabd8fe248478095d514bc2b72e6cd1' ;; 		riscv64) binArch='riscv64'; checksum='4b108ef51ee3fd567f13cba3d3e2c89f86894e27b2ae5585e9ee20346b17f71a3bdcb968b25cb6d88a9a9671ef73cf82a1c0060e273d9b2e0c0c680369c83280' ;; 		s390x)   binArch='s390x'; checksum='f2e18d550dc12cb06bedda46c47404a2fbfdfb12363483daf41f5c52736a8ad22c72d7c32edb08aac7a18a1f1faee19aa787ac72b7515f07daf77329f4efbc3f' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 16 Apr 2026 00:33:32 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 16 Apr 2026 00:33:32 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107efaa291b5f83372c13d97ab11aebdd260da2222cd795a4f56930ce905e525`  
		Last Modified: Wed, 15 Apr 2026 20:41:28 GMT  
		Size: 291.1 KB (291147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80b37d7575305ba979d392f19380204aa402def17a0f42736f2c66c815c079e`  
		Last Modified: Tue, 07 Apr 2026 21:15:15 GMT  
		Size: 66.4 MB (66432184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c34c0e0f61bfdc98564c02bc5b7b38c097bc93c1cc028e7ac08cced89a320`  
		Last Modified: Wed, 15 Apr 2026 20:49:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf3a0326749da7e4d5806a052fbd4999a3c204aeedb4dad5d5ff3c65676d3a4`  
		Last Modified: Thu, 16 Apr 2026 00:33:44 GMT  
		Size: 6.9 MB (6861709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393a4ad34ed3cda60b22c5b76efc0565030fcdfefed1267bbc9c8f87d34b3173`  
		Last Modified: Thu, 16 Apr 2026 00:33:44 GMT  
		Size: 1.8 MB (1782838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f901072585c7af95112707a384769786aa79b6d8802f03f30270a67f85ab65a`  
		Last Modified: Thu, 16 Apr 2026 00:33:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:b3672bddf26e3f2f2114460a0636e98d557a4059a463d6126a5eb5830af81a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 KB (301848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e02457a0328f42e52375ecebabb39a9e7a8dd9ce205e13bc16057aa33ca5e9`

```dockerfile
```

-	Layers:
	-	`sha256:5cf1a15be680e85c77f682eebed24b73c946ccc28327c23920c904618d4fa506`  
		Last Modified: Thu, 16 Apr 2026 00:33:43 GMT  
		Size: 281.7 KB (281719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1b35f17a8e96eff33197aae987d2a107c91e64a19c7aa4cf2feeefa7a030b51`  
		Last Modified: Thu, 16 Apr 2026 00:33:44 GMT  
		Size: 20.1 KB (20129 bytes)  
		MIME: application/vnd.in-toto+json
