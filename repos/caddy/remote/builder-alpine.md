## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:247b0b18c3d698ebcc93cb3557921b18806c2c48e318572abf8150705eb5e05b
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
$ docker pull caddy@sha256:6b133f8e010abba20ec5256ed891a40a846d1f13c0c79cf5191438f495d839b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80670788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3f961c4f24ff3d6807109abaf339559fca4aeefcdd80ab09b6da52af7daa2a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b759c742c820da15e6f90e261cd98cb6a80a2aa86df3805a613d0deffebb691`  
		Last Modified: Tue, 04 Jun 2024 20:15:52 GMT  
		Size: 292.4 KB (292426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59181b2ee0371ba1fa663cb5405beb80a23dc447143acf303c5c64d36a7309d`  
		Last Modified: Tue, 04 Jun 2024 20:15:54 GMT  
		Size: 69.3 MB (69345545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bdb513516e191c7fec827f345aba47b6533196cecece14e1aa7dcd848cd3f6`  
		Last Modified: Tue, 04 Jun 2024 20:15:52 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7075843834c6cffbc94c0a0b6508ecb29a2e9712d0cd368bc52a653dadfe60`  
		Last Modified: Wed, 05 Jun 2024 01:06:22 GMT  
		Size: 5.9 MB (5909461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ac4b2499e39cd68cf75497fa205304aa9f13c9dbe511b522369bb185899752`  
		Last Modified: Wed, 05 Jun 2024 01:06:21 GMT  
		Size: 1.5 MB (1500668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080a5ef136f6d6c62ae32522f9a79f20b6e2c0074f2ab1e2c056cc833f9298cd`  
		Last Modified: Wed, 05 Jun 2024 01:06:21 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:59c40dfffa8e77df6973e9697b80b9fed00a10f5d1c92f6f6543ec1ab4eeeffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 KB (296477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5de3b08d4f129013729568c6a76b684a0404824451f5481d57ac91a6b16634`

```dockerfile
```

-	Layers:
	-	`sha256:9e79926d7c2cf5bc691ec8d5083f8ff423a03f1cd1c4f2652579ad05d227de1b`  
		Last Modified: Wed, 05 Jun 2024 01:06:21 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:115923316e4e0ffcccb3020e5faae42eba35f088ae273f028a31cec487163710`  
		Last Modified: Wed, 05 Jun 2024 01:06:21 GMT  
		Size: 20.0 KB (20020 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:82f6a0422c3a2547a9ac52d068e71c24a1f1ec8c5c2ff44cb80ed6f4da089c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78653801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d03d0448327b86bc15b37057880e95cebd874edb2c952f33b04b1645bbfa39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a2577dc35c4def2519dc8dda43a837cd36c563f04d6fdebf42f9e60a0fd369`  
		Last Modified: Tue, 04 Jun 2024 20:20:31 GMT  
		Size: 293.6 KB (293616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2388fa1f9ceced099ac1af7a1054215236ac4f41428b02ea4d6e98d46f5da9d6`  
		Last Modified: Tue, 04 Jun 2024 20:20:34 GMT  
		Size: 67.7 MB (67713314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a03ecbd23d0b5264014f7d2234b2f2e951cf316e805ce0125dfe2f91e2530ff`  
		Last Modified: Tue, 04 Jun 2024 20:20:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8be60202438d8e68a6042a7a74bc40483320f4c9096411368a935dd2b8665`  
		Last Modified: Tue, 04 Jun 2024 20:53:14 GMT  
		Size: 5.9 MB (5857397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2803e5ba2dac141cc024c9efb1f0c19f66910b803717280d3dd7aae496ea570f`  
		Last Modified: Wed, 05 Jun 2024 01:54:11 GMT  
		Size: 1.4 MB (1423819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0762c1f23db2b393bfe70f7eae657925291a8a19c4ea2eccd686941238f90d4f`  
		Last Modified: Wed, 05 Jun 2024 01:54:11 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:47f870095e8245f608251cee3157c4d2415d7915d5a091fa4cfa1f09c9999934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (19951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ad8dd9544ea46cdab1e31de8b2540928fc2e120268b2f2fbbb7511bff40a25`

```dockerfile
```

-	Layers:
	-	`sha256:9f669512f49ef18b8b8d45afaf88f09bab0f1653e9332b3081eb8ea3ddca535b`  
		Last Modified: Wed, 05 Jun 2024 01:54:11 GMT  
		Size: 20.0 KB (19951 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:e551e2835a75dd7407ed00aee4fc51a046f636e30729803993b44b9450480463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77867841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89dec0117d71e3b130cb1f1d5d71614480e1589b07d7510d97a5fab7f0658b49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f0fec4aa5208228cdd97142cd6f1bcef97090cb45801ea77c0386c3d9d0f9a`  
		Last Modified: Tue, 04 Jun 2024 20:22:09 GMT  
		Size: 292.5 KB (292456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f2d60982f3278ca26e0dd4a91fb30e80076051e36da023e58e47681cc2934e`  
		Last Modified: Tue, 04 Jun 2024 20:20:28 GMT  
		Size: 67.7 MB (67713391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c532efaafc9914f6e2208ddc89abe6b57176d33b64744c3da150ef40c2cb3fdf`  
		Last Modified: Tue, 04 Jun 2024 20:22:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678090d3d52c54eb99f55839a9e374125c2363a55968f65ac692e8a9f38f2017`  
		Last Modified: Tue, 04 Jun 2024 21:08:42 GMT  
		Size: 5.3 MB (5346597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b884f52149958e3f9d10976df98c27c9422d434832830239b4302441f0fb8d`  
		Last Modified: Wed, 05 Jun 2024 04:13:13 GMT  
		Size: 1.4 MB (1420764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d9e36bd5418f9d8ea2800c4ba84d03942c19d750b6bebdd10462b16ac99050`  
		Last Modified: Wed, 05 Jun 2024 04:13:12 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0de6a9a28e20eb6e5ecd2e590cd961cb10b3d0797789a4f70e437c473aee3ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 KB (299239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993bc54f40b724e71503f0bf2070d77e3cf60f8add898460682dd209b7fb5d2b`

```dockerfile
```

-	Layers:
	-	`sha256:df60fc6062a844c5165863fe8f97e9135d4840b91defb396e02637d22b42d523`  
		Last Modified: Wed, 05 Jun 2024 04:13:12 GMT  
		Size: 279.1 KB (279069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110194735782c03d1f01b558c8d7e66b5f3aba45e6e87f102004b128b19305d4`  
		Last Modified: Wed, 05 Jun 2024 04:13:12 GMT  
		Size: 20.2 KB (20170 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0e70454943d37a64344820181d8396714d91d40ffd3a04844076a3b41d69a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78085757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb59a6bfcf30a2dfc3705ca6f25183cd395301a7a185380c978cea1117557ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Thu, 30 May 2024 14:50:16 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 14:50:16 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 14:50:16 GMT
ENV XCADDY_SETCAP=1
# Thu, 30 May 2024 14:50:16 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Thu, 30 May 2024 14:50:16 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Thu, 30 May 2024 14:50:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fd4d77c1150ba7c64d2b9cb1ad73058c134eea51cdf8a7c969379c3fe358c3`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 295.4 KB (295445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d540c1f502e66badd39f9acbd5037011b4a4a15454c8fb22de7aa4378ae97`  
		Last Modified: Wed, 15 May 2024 09:08:33 GMT  
		Size: 66.3 MB (66272038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6930e6242b08ff7992e85b10519d54167d7ffdedf7199e086b7c8be95e4baf6`  
		Last Modified: Thu, 23 May 2024 06:26:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d49fbb06d2ec1fb8e7c2633794d12f435fe6098384a1ba28e82e7be07d06a38`  
		Last Modified: Thu, 30 May 2024 14:42:18 GMT  
		Size: 6.0 MB (6033730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dd998a75477c407a2dee8c594a80ba41fdac4dd42d9d67a7c414c4c8997b9`  
		Last Modified: Thu, 30 May 2024 22:40:31 GMT  
		Size: 1.4 MB (1397169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770803ae5abd93eb1dcbc65ce6b1ccdfd01a538b7c537f05e868e88c81d9d430`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:acae0dfa758b68833a5e19bd4804c3a3916e795ee6dde565fc338a83efe0a840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 KB (295844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de6d746bee70c9e18f38b0e19e943d1a7fcdb8b1b73856d337570218ce8c0bb`

```dockerfile
```

-	Layers:
	-	`sha256:1abefdba7275d0ce20e30a7257a2ed4eae90e1997c2acdafc5dae8ae0afccec3`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 275.8 KB (275813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5fee8e57abbb9909e5460f0b9e029723da0ba965f905c8d24ee042cab953b8`  
		Last Modified: Thu, 30 May 2024 22:40:30 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:880d9c0e39034151914de6989f21e24b404813d597f00ad014d30ea0458cf58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77931798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b38548bd7deb171bec7038ddb20c8985702d2206da80569677a194f8624e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV GOLANG_VERSION=1.22.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Jun 2024 03:28:41 GMT
ENV GOPATH=/go
# Mon, 03 Jun 2024 03:28:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Jun 2024 03:28:41 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d80f5a26e017a5de387ee9062b6045acd39de2769d99f89412d8bf3a06a818e`  
		Last Modified: Tue, 04 Jun 2024 20:22:25 GMT  
		Size: 295.9 KB (295901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236cbdc316b6a948ffe0177ed252011a6646360d0cbcf8cbfc819b8774160a29`  
		Last Modified: Tue, 04 Jun 2024 20:19:26 GMT  
		Size: 66.4 MB (66440839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5985a784d420c5c73caa2c2183b088f1cccc5f594e8f17d1863c4e7cec5cd64b`  
		Last Modified: Tue, 04 Jun 2024 20:22:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f0f069ca8387566d3df27b551a607264af653c0b031d98590751950193ab7b`  
		Last Modified: Tue, 04 Jun 2024 21:08:49 GMT  
		Size: 6.2 MB (6234590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff459de908b06bbbd6bf7865e4b7543581002b2a392c0aa4da5c8227a5953b6a`  
		Last Modified: Tue, 04 Jun 2024 21:08:49 GMT  
		Size: 1.4 MB (1390027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7583914653da2ffe5156991b3ffa852f724b4cf5f969c798c03476b3658d59b2`  
		Last Modified: Tue, 04 Jun 2024 21:08:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:fb9510626438a4c7bb00ea24f9bb4c2191e46db3589aa775e1a8c247c375e0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.3 KB (294264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef95b80f5a16b35228a4c286c8d92f93df327837bfa313d88dde959ce158378`

```dockerfile
```

-	Layers:
	-	`sha256:675dc8f9f8447073d0a5007163ace90269107affe7adfacf5bd05b6ee4ed309f`  
		Last Modified: Tue, 04 Jun 2024 21:08:49 GMT  
		Size: 274.6 KB (274595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e2a762d865b1a5f2709b219267fb5815b4b3233b01ab14a61e41bc2d0859d`  
		Last Modified: Tue, 04 Jun 2024 21:08:49 GMT  
		Size: 19.7 KB (19669 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:985fd8690c6cfe8d98ec16c0216f6e500f4114c486948f1d7a29b2199f0bf261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78086072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58444eb6ec66d56879916049bc4f4acf5b7fec348dd774661c762dbc557d5706`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 19:06:26 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 19:06:26 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 19:06:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 19:06:26 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 19:06:26 GMT
WORKDIR /go
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 04 Jun 2024 22:12:59 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Jun 2024 22:12:59 GMT
ENV XCADDY_SETCAP=1
# Tue, 04 Jun 2024 22:12:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		riscv64) binArch='riscv64'; checksum='afaf940189942adfe0518d06b42f2624f387a02d88ce9ec5f8cc5a99347e032e2dcae3e3cd5856ac1a6ce107a7654e62b04f635f1dd891ca192b23758946b45b' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9039d2f2c483de6ff6c0473136ee343e37b5ba2966df43c0a127325eb07e13c5`  
		Last Modified: Tue, 04 Jun 2024 20:20:42 GMT  
		Size: 293.2 KB (293177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ff39e1364b0235a20bcb68f2b89e444ffc6e6d6c5e999fc435f593f5280802`  
		Last Modified: Tue, 04 Jun 2024 20:20:52 GMT  
		Size: 66.9 MB (66893432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f0a03e5723c69044ce64d202b7ba1c936486b812d17c227b680101a2b3caa2`  
		Last Modified: Tue, 04 Jun 2024 20:20:42 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07657bdc0ab59c33c1995edeb28c18f00692c4c861a324ade155b967d39379`  
		Last Modified: Wed, 05 Jun 2024 01:12:02 GMT  
		Size: 6.1 MB (6126016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e597cc74989ed509f969a83b0496d0d651776b17e8154f665188cc468385a6`  
		Last Modified: Wed, 05 Jun 2024 01:12:01 GMT  
		Size: 1.4 MB (1404294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c03811950fef9811cda2d94ea204c150ab05ed8fb7da15720d5e454528d023`  
		Last Modified: Wed, 05 Jun 2024 01:12:01 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a84bf5e908c004c629b88a09b7905e571b42fed0eaa5f280918a7ea384b833b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 KB (294711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17ace45b2dd3cf0daea40fe5a9c50faad205f04215bf67b50687d9860a64419`

```dockerfile
```

-	Layers:
	-	`sha256:8a33ccb51d7eddb786c03ccdde6b2239319840fa29946c18c963a560227dc2f3`  
		Last Modified: Wed, 05 Jun 2024 01:12:01 GMT  
		Size: 274.6 KB (274591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec64c73445ae1b03f1c00d67be023ff01a4c78c7dacf41ccc4f0760356e41d2b`  
		Last Modified: Wed, 05 Jun 2024 01:12:00 GMT  
		Size: 20.1 KB (20120 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:bbd371f55e5fd21330c24bcfd34a1a8702191867cceb0b340c3b21002c23a3f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af99e1c137b5b73332bc84f34766ea766f1369cccc49d900bc35cd805ff0dfc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 12:22:57 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 12:22:57 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:22:57 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 22 May 2024 12:22:57 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 22 May 2024 12:22:57 GMT
ENV GOTOOLCHAIN=local
# Wed, 22 May 2024 12:22:57 GMT
ENV GOPATH=/go
# Wed, 22 May 2024 12:22:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:22:57 GMT
COPY /usr/local/go/ /usr/local/go/ # buildkit
# Wed, 22 May 2024 12:22:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 22 May 2024 12:22:57 GMT
WORKDIR /go
# Mon, 03 Jun 2024 03:28:41 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_VERSION=v0.4.2
# Mon, 03 Jun 2024 03:28:41 GMT
ENV CADDY_VERSION=v2.8.4
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 03 Jun 2024 03:28:41 GMT
ENV XCADDY_SETCAP=1
# Mon, 03 Jun 2024 03:28:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='a726e4b7992f3c6c11c585b6100f796f035c6757d247110c6af9bb4f218b7ec67d07db0013c6834e9b881582d75ba4fe8e78f6ca5883b1017da6b5407d1ca25c' ;; 		armhf)   binArch='armv6'; checksum='c0a94f2e59547fe5d4793ec2447ba0b832731c7b1387ae3c90e43f081da57ad68ab506de43ad91a35754a779b591dc5a39a92b6cf3b5ef352622cfb811e92157' ;; 		armv7)   binArch='armv7'; checksum='4820d03ed4a805cf52803725fd1eda9d96f15692ab3cd2803fe91e676f1a24a48b31c4e6a1ec043e5f7f077f302e003e4997ca620c9674ed65e7804417a91af6' ;; 		aarch64) binArch='arm64'; checksum='41033dc721e799583eac2014b6e409d65a704d0a4360c131662aa651e7fbd129dce03c460661a51e0ba192d27fb3af19faa054da8c037c642b24a12124f6d4a8' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ea454e90519f46eeaf785a5789d455a01378dc543838d0b57448509036f3a215913c8a6e1fcb0b9249e9b941f29a29257367609e1ef7ce7f2e0522c768eaf2cf' ;; 		s390x)   binArch='s390x'; checksum='d8d3bf402107dad8f07ed9d5df008b3f6cfd021c93d00f6fc31c641d69649255f2e95d65a46553fb06bf9738158d0ba92d3bbd548e878f4569523b6e6fdeacb5' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy; # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
COPY caddy-builder.sh /usr/bin/caddy-builder # buildkit
# Mon, 03 Jun 2024 03:28:41 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e66d9c1932c81dc738c92566c80482d80ffdd93de4411f25e01523a5c4c859`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 293.4 KB (293402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2482b2ed92bc4103a166e8c33b88d4d23fd167f50526ca1710fcfd6050c54952`  
		Last Modified: Thu, 23 May 2024 03:14:14 GMT  
		Size: 68.4 MB (68399077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b16ac5f62001aa9fecfa7a1deaef728e369ce04bde6ae9c4ce50e5b79638a9`  
		Last Modified: Thu, 23 May 2024 03:14:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7fb356c901d4b14e02b6bca1b10852f4a9f85dc695ab3239d771383ee632a5`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 6.2 MB (6179567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62ccaf0be9fd4c408957b5068154bc456143c35dc8c818955199c1cc19412fd`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 1.5 MB (1451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216b4bc58f3ca32cc60a50bb5a7f1d89bc4c869fcbcc8a3d79cfc455e3a829aa`  
		Last Modified: Mon, 03 Jun 2024 21:32:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a0cd00361f284c2509ee135e57e9ba892603c9babba263a8c9a4019ec816f9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.4 KB (293353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea05560489e0436aeabee2b1d096e6ef1883871da7006a5f427be424a1588525`

```dockerfile
```

-	Layers:
	-	`sha256:7a0297889ae2bc64168bf10de6cb03222bf8a8d3915e6eb4e76077607f4f1dca`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 273.8 KB (273754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76f562e536bfdd4352eb3a45746b1c36b9bcb4b47e266c037b4ef05073aa9771`  
		Last Modified: Mon, 03 Jun 2024 21:32:19 GMT  
		Size: 19.6 KB (19599 bytes)  
		MIME: application/vnd.in-toto+json
