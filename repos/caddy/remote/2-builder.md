## `caddy:2-builder`

```console
$ docker pull caddy@sha256:66369ac6ee01c3ee6d49774900e3d568c23cdd32f899dcd77c83adb577b1344c
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
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:ccd3c6061c374d09d8bc1dc80d04a50c88009cc548ca6a585c753d5975806526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80670786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1314448ea5d0fe75f1bfd52dd204a6f56fd978feba1b2cd44715340824a122db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:8b732c871fea20cea9c9afe0ee6c127852025cd9f1119819121110f1838b304c`  
		Last Modified: Fri, 14 Jun 2024 17:54:03 GMT  
		Size: 292.4 KB (292416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060aaf7efd0676cdf56165fe26e63a047d7f3c483ab1043d530db9370e6c28e7`  
		Last Modified: Fri, 14 Jun 2024 17:54:07 GMT  
		Size: 69.3 MB (69345548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1964877d6860798d7794738b2706190a440706bbffacdaea35594d1ddac0fc`  
		Last Modified: Fri, 14 Jun 2024 17:54:03 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0246a9aa2a3b6406af961f68fc8cea4ae29580b9b554b907990039d5a4e094a`  
		Last Modified: Fri, 14 Jun 2024 18:54:45 GMT  
		Size: 5.9 MB (5909464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69158900a3d2ea6aad90ccca00264c54a2217466093f2df0aa595846cb00c736`  
		Last Modified: Fri, 14 Jun 2024 18:54:45 GMT  
		Size: 1.5 MB (1500674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a8112a39240e6c91831ea07faac29f766e4319493bbdc44041c42744a613dd`  
		Last Modified: Fri, 14 Jun 2024 18:54:46 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:cf70b5811e444fc608f30988a55a4ef79328cd3653e33fdd3da6b744999985ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 KB (296526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b2258a12eea2b1d9925266bfd3c830fa0e49bfa707e4d25b77714decb963ad`

```dockerfile
```

-	Layers:
	-	`sha256:9ebf3aa6c038092a6e062cb5d5235a12e4caf03d6fed225fcd34e75157af8d14`  
		Last Modified: Fri, 14 Jun 2024 18:54:45 GMT  
		Size: 276.5 KB (276457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9572add926bd37f873cd2e92e205e9b7e1edeff975c30d08a40d67d4186fef`  
		Last Modified: Fri, 14 Jun 2024 18:54:45 GMT  
		Size: 20.1 KB (20069 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm variant v6

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

### `caddy:2-builder` - unknown; unknown

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

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a0f0657bd5ce63ce7f00615fa2e4756a7892b8bffd1031c05c16f1f06090648e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77867902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cf9013ff39cffec50f7292b4cdf4c04f61f507a1dcc2a5be603c95fe9985c1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:ba8d8376f429e08832ffbb91ed771b1b953556865415b4e4c37033a89a2f8aca`  
		Last Modified: Fri, 14 Jun 2024 17:54:08 GMT  
		Size: 67.7 MB (67713411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c2b8aade3e7f812acd81e815726960c5d479cf6fa0a3c61e9db95ccb506606`  
		Last Modified: Fri, 14 Jun 2024 17:55:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e0bc242bd145740c9652f149641c2460d6b6c7a0b8380d244ba92dcb89ec57`  
		Last Modified: Fri, 14 Jun 2024 20:26:38 GMT  
		Size: 5.3 MB (5346632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff4da2794aa5574eba52a6dc0c23fc23fe09962ab452d7fde731126592ac8d1`  
		Last Modified: Fri, 14 Jun 2024 20:26:38 GMT  
		Size: 1.4 MB (1420771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfd2e184c73144c7910a2e818cf037f620433750c8e4e19a9ce823f8ee0b317`  
		Last Modified: Fri, 14 Jun 2024 20:26:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:18b1fc5583ec48da84f9df181962de8663d920d252686189873d1201bea107fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 KB (299288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c710bc337f225d0157c4d57bc6fcc9e3296670a71260262fd33a74f136d550`

```dockerfile
```

-	Layers:
	-	`sha256:7654384cfb7a78d5874477e317b5a7b23ece56a7491a2d5c6b806903d5aab99a`  
		Last Modified: Fri, 14 Jun 2024 20:26:38 GMT  
		Size: 279.1 KB (279069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eecb54162d7dd70032566ec1da00e4cc5cd42962025105bf6f3aad803a45a2c`  
		Last Modified: Fri, 14 Jun 2024 20:26:37 GMT  
		Size: 20.2 KB (20219 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:40ca549a30cbb2cca429ecdbc8971bf6dc952e95b11117426f51d871031a36e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78078319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3e91ec086a0fb2febde72be6af362ac33ac387cb2ede1292198f0a3100cee4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1415b17371e9e60943269f29a4d23a5e3704ddbc1ab4546289828f84c8f85ba`  
		Last Modified: Tue, 04 Jun 2024 20:21:10 GMT  
		Size: 295.4 KB (295442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c0d35bf3e901b1024e7abc65a8b1332e085c592b5bdd1d9422364771935e1e`  
		Last Modified: Tue, 04 Jun 2024 20:19:51 GMT  
		Size: 66.3 MB (66270410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1454c04e2e13bf638acbf6645eced9cf823aec91cf7395ce136c1d5348dfbdd9`  
		Last Modified: Tue, 04 Jun 2024 20:21:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43be9a418c8984086ef40945de09003a9bdc78d1c4265cbea409f27660637069`  
		Last Modified: Tue, 04 Jun 2024 23:48:58 GMT  
		Size: 6.0 MB (6027923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba185ef49ce587557c88f72919c1213651d0323ba3025980a0d5927c5ffaad88`  
		Last Modified: Wed, 05 Jun 2024 13:11:04 GMT  
		Size: 1.4 MB (1397171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b712c17af96c9440b016f012aa17be505aaf9c6d6d0a782f9eca710f6dd5afb`  
		Last Modified: Wed, 05 Jun 2024 13:11:04 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:54e3714cc0fb949c67ed8932e45aee5f2d3075ce1f491c81fad903c1bdf776e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 KB (297044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e54bb9142e66f07680cbfa173a95f5653a9331c08ed3730b7b48eb38ee712`

```dockerfile
```

-	Layers:
	-	`sha256:3bd7ce0ba6b8d4d553f96ff4d446f6dcb7e7b8b6d5662d330fe9ef7a8e9cb240`  
		Last Modified: Wed, 05 Jun 2024 13:11:04 GMT  
		Size: 276.6 KB (276561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781d74cd600da586fabf5d6a330934b208a92c12f112fa0e5cfffc5eeca54a5b`  
		Last Modified: Wed, 05 Jun 2024 13:11:04 GMT  
		Size: 20.5 KB (20483 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:290b2ab82007b3cc09676c7ac914786a3bcde8c566c3f507656ef43e8d995c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77931822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5997afaf0c2c2745a643026072681cb2a2a38e4029aaf4cf809cc943767397e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d80f5a26e017a5de387ee9062b6045acd39de2769d99f89412d8bf3a06a818e`  
		Last Modified: Tue, 04 Jun 2024 20:22:25 GMT  
		Size: 295.9 KB (295901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210b2be98c546d98d20cd631f014745f73d191238d22c5e439478550b6727b8`  
		Last Modified: Fri, 14 Jun 2024 17:54:36 GMT  
		Size: 66.4 MB (66440814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee1536d69e63886254422ef719cbfc05e944ac23de507c77bde7e1190b6bb79`  
		Last Modified: Fri, 14 Jun 2024 17:56:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b13c52fd7d87b5e88f94e9dde229bcc403cf2e7d32424188dca5a098e02b90`  
		Last Modified: Fri, 14 Jun 2024 20:38:40 GMT  
		Size: 6.2 MB (6234637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308045fcb54d25b1d9ebe0cdb312449267fdc9cf835530556c119984e338ad1f`  
		Last Modified: Fri, 14 Jun 2024 20:38:39 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e32eb1a51f5906a5845137fff97e510ff20eceefe79cc36beefb1c2492a3439`  
		Last Modified: Fri, 14 Jun 2024 20:38:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:24d560cafb896659b0ec7c33b5f99e347adf1b9897953a9c9ccb0e2d12f3907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 KB (294764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59999cf727e500ec0b7fb3fdd286c5dc32d97011445079b3b055155ef34195c`

```dockerfile
```

-	Layers:
	-	`sha256:c29462965fb5fb405329a52e0291af44494add9651735619623b132616480352`  
		Last Modified: Fri, 14 Jun 2024 20:38:39 GMT  
		Size: 274.6 KB (274595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3141ed2d02408fbe44fd56cc91851fe84e6cc745cd5bdbb9d67a7409b0358320`  
		Last Modified: Fri, 14 Jun 2024 20:38:39 GMT  
		Size: 20.2 KB (20169 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - linux; riscv64

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

### `caddy:2-builder` - unknown; unknown

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

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:fc8c9a7408d873d7462f78440356354bf54c9f70deb96847c4ecc2978be04475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79784060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2a3e6ccdf0bfb9fcb23c926f443dfb896a28007695650d6467249d244b2f4b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Tue, 04 Jun 2024 22:12:59 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOLANG_VERSION=1.22.4
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Jun 2024 22:12:59 GMT
ENV GOPATH=/go
# Tue, 04 Jun 2024 22:12:59 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 22:12:59 GMT
COPY /target/ / # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de2e843de006048b62d6b06bfc83cfa81a3d30ed58401daa91927b1294d4a31`  
		Last Modified: Tue, 04 Jun 2024 20:25:29 GMT  
		Size: 293.4 KB (293405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54ac55846ff64482893d22cd74289e959d60007f939ee44a6905370f9611de2`  
		Last Modified: Fri, 14 Jun 2024 19:31:27 GMT  
		Size: 68.4 MB (68405222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f410bf0e354fc721a933146ceb370df116e2090b95760ab8137d4438566078`  
		Last Modified: Fri, 14 Jun 2024 19:37:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541db20020885b7c57471f0f50a9b77d948fa61a0a3f1cee5fe0534e5547b34b`  
		Last Modified: Fri, 14 Jun 2024 20:02:32 GMT  
		Size: 6.2 MB (6172714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d33c113dd367a19d6c890b7f5d3c20d3cb847af6668e90c96f4594fb0fc365`  
		Last Modified: Fri, 14 Jun 2024 20:02:32 GMT  
		Size: 1.5 MB (1451785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68127fc2982f2e634d59d4ff9ed4f77d9b9753d3f7132e94250f0918f478e00`  
		Last Modified: Fri, 14 Jun 2024 20:02:31 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:2-builder` - unknown; unknown

```console
$ docker pull caddy@sha256:b15876b742a711d8cbd3bddbac953d87281186c7db9e7b646db84fb54e6332fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 KB (294601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d442e597a3bd2c6f44b82d819e7d48390a1889e372efc351321915238b70acb4`

```dockerfile
```

-	Layers:
	-	`sha256:3f1d60985c4aeb0eeb12e27d99bdc817dcfd6278f16aa860a8e743b91715236c`  
		Last Modified: Fri, 14 Jun 2024 20:02:31 GMT  
		Size: 274.5 KB (274503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71fbc8509f2837477e93d54b9ded46c05c6babcb42f3d695288bfe00c894412`  
		Last Modified: Fri, 14 Jun 2024 20:02:31 GMT  
		Size: 20.1 KB (20098 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:2-builder` - windows version 10.0.20348.2527; amd64

```console
$ docker pull caddy@sha256:a5c9736e07d2e51fc117c08a132ddd8cf0d4d157cc8ce24dde31e4833e220148
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2217625172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e712c86b78dda184eedc0dd175768d280e951233e45b985a826454212f5ffb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:09:22 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jun 2024 18:09:23 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jun 2024 18:09:24 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jun 2024 18:09:24 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jun 2024 18:09:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:09:44 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 18:09:50 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:09:50 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 18:10:55 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:10:57 GMT
WORKDIR C:\go
# Wed, 12 Jun 2024 19:06:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 19:06:22 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 12 Jun 2024 19:06:23 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 19:06:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Jun 2024 19:06:36 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Jun 2024 19:06:37 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0587398dd0c7678da17819ef86b03d0f03d5608d921ef1bd9dd041001aa46064`  
		Last Modified: Wed, 12 Jun 2024 18:11:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9adab2cbb6127c55064d7c9aa02c40af934b227b342e9ce0ed36ee98f1b4843`  
		Last Modified: Wed, 12 Jun 2024 18:11:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69ff0b716a5ce8110bb53b45bd91710d820149130deed9c38472234a7e9afd9`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96de8f0195629f8fc68326d735d8815462e97b6c76fbbf56e537824e83e8e4be`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc335406a0dfe2ded2091ea3986516dfe4e922b476d834ddb8aec57c37e493c`  
		Last Modified: Wed, 12 Jun 2024 18:11:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5e46457004c449858017460ecd124b76a51b6e5c4d75579bd0fed83a03b66b`  
		Last Modified: Wed, 12 Jun 2024 18:11:04 GMT  
		Size: 25.4 MB (25426639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a91a7cff7f3986c1704d0d0fc42da5934271de00dc73f1bbbb33c58179ae1d2`  
		Last Modified: Wed, 12 Jun 2024 18:10:59 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ffbe09e050d4b99a243d40d14a09182e015c0a0d40c056ecd2f2b196eb9d06`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 325.4 KB (325417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342559014cfb73e966442ed88b5360904cd00c05a834f575b49596888e680792`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea1a9b1009e5fa7a44f4b39043515d74d2b1a71c21fa1252506b20c9d8d935`  
		Last Modified: Wed, 12 Jun 2024 18:11:10 GMT  
		Size: 71.7 MB (71736322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59599ecaa1eb84019e233b455deae710859ed0f0a323ec5689d820efaf55ff3f`  
		Last Modified: Wed, 12 Jun 2024 18:11:00 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65d85360857cfc8e00101a27ce37393334201cf7ad2bfa92f1d25ac2c46a099`  
		Last Modified: Wed, 12 Jun 2024 19:06:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a649add317f0043f54d8847dbb12dec7f65e49c4aa06a80f8c512a69166caa8`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874045c3f76c039258ec0823fa7e4e83cd2dcd56615e0bd7d98e12954e51b3c1`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a82ca2afafcf0ef97e7a1ce7133e6331a3165d1b37c49d49e7e344d5a6e4a98`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2693bfc3905400c24ddcd564bde563b2bcf9db8bba5d8ca5bc5655ecc0fe8029`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.9 MB (1941203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bea81e16e408457ef5a11b956b6c21f1c2995e66814c68bc50b44bba9f18764`  
		Last Modified: Wed, 12 Jun 2024 19:06:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.5936; amd64

```console
$ docker pull caddy@sha256:87643957c20a3a87ccd5a56c00ef0f360eff0b9498e2fc15e0a93d8d5f513f86
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320513498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed61ae64a42b233780136a6dd4245dc4313a9d5a41e0b05ac7caf83ef6f39f02`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:13:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jun 2024 18:13:35 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jun 2024 18:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:14:24 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 18:14:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:14:42 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 18:16:03 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:16:05 GMT
WORKDIR C:\go
# Wed, 12 Jun 2024 19:06:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 19:07:00 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 12 Jun 2024 19:07:01 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 19:07:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Jun 2024 19:07:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Jun 2024 19:07:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3c3ab4cd77fae9059354ee5b73b856f9ac9c22731d9dcf4e365268e08cd843`  
		Last Modified: Wed, 12 Jun 2024 18:16:10 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c37a0d0339c6b8b1c237b2c8250a774461350198b803d76982b65e45d102b`  
		Last Modified: Wed, 12 Jun 2024 18:16:09 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3b2fa9fd4cc3f0df2f037d6653ea1cdb5b7f419bd99e0576a57dcdf4b1ace7`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856fdc06eea972eccedb4e2c6d528d9d6b992c971c4a29f289a88eac23a5d5a9`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2096b09fa3f4c724fcb42fe19a8a5b0dc61277e2e802b4674b64a58de93238`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69169629162eb6e94b664ddd335d3d02ae4c7a356ec11557b77d6780bfb3bb04`  
		Last Modified: Wed, 12 Jun 2024 18:16:11 GMT  
		Size: 25.6 MB (25576657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78abdc0679bbe9abc0864ab9497cfb6767ad50cc06c121d874dd8a022821b892`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6bc3316ec48d85e70aa2d8c21fa5ad4eb37113d651977b29d3b5495e034859`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 336.9 KB (336919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222f75d358e9b8e60fd785f40a7b8245f0cf6d634f64488172b55910395e1a2`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e23068dc7ebfc095432cdb1e6af9726e3b10d959fb3635a24504c0e99a1a297`  
		Last Modified: Wed, 12 Jun 2024 18:16:18 GMT  
		Size: 72.0 MB (71984977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe4726c882b12bd6e005278f53050cd3de58b99ce5170e1d152a081dd3e8d6b`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.5 KB (1501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a82c23888a8a0ba647456b84c7ea43d9006ae2be3d5696242de32eb8405ac31`  
		Last Modified: Wed, 12 Jun 2024 19:07:48 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46372b8f4856e120d8fb747141593fa94d9a23f57791830afde85df63afc9899`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f48c9a230e1a939a96d21e33a526d29db1f16f675d8a5a5d2980d525c55e7`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a77f93979cdc9572da29ca6339d8c5d86cab41b05c15587495a9eb7462e987f`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a650a02a30a4f0a3a25ceba7eb1f2a71ec607cc0ef9eadf34699b617fd5b0171`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.9 MB (1916297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e5d61909213f979bdf56f6332986a4a3e32291b9e092ecd1ee655b82e52b90`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
