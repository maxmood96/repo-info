## `caddy:builder-alpine`

```console
$ docker pull caddy@sha256:0030fe883629b7c7923e2b8b2ff76608346e08ab88192c5e78ab290e8ca7046f
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
$ docker pull caddy@sha256:877814c5abb44c85c2615cc705f8011e8188aa6a211da55986a6d038e23834b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80672576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fce6536f855029143fa4374ced1ec74a5f9d851de7eb2ac6ef0c40b64a2c0e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7728242c92e74edf5cfd2c7e300edc2756a81630e514f71f9330869e86280f0e`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 292.4 KB (292423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060aaf7efd0676cdf56165fe26e63a047d7f3c483ab1043d530db9370e6c28e7`  
		Last Modified: Fri, 14 Jun 2024 17:54:07 GMT  
		Size: 69.3 MB (69345548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f8e900f733a3e177aeba423378acb3315424c72b4d86836a7e71a7a1a4393a`  
		Last Modified: Thu, 20 Jun 2024 20:54:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54d6740a81ffc96171c19312eb197fdaf263a027a55b507e9f71f2896879936`  
		Last Modified: Thu, 20 Jun 2024 21:55:40 GMT  
		Size: 5.9 MB (5909488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e77eacc660a838d65f8fcf5a51e1da2bbf2416e82461d872302d4bf8ce27f1`  
		Last Modified: Thu, 20 Jun 2024 21:55:39 GMT  
		Size: 1.5 MB (1500680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030fdae9f84a086a8da29d14de6701ee550a57a3a60b6b9fa5ca2ce2415c862c`  
		Last Modified: Thu, 20 Jun 2024 21:55:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:0d32d244df1051d7a2add823911963fbbea810229195d72523c5d0657c2b1ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 KB (296527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f078a0c725ab67ebc090568ca92af33423025bc05b9d27afadc86a6cfd48a51`

```dockerfile
```

-	Layers:
	-	`sha256:5fb8d35f8f2cfc19e0d28ae3e075165e8ae7f8b7b60ad7193daeeb2419c039ef`  
		Last Modified: Thu, 20 Jun 2024 21:55:40 GMT  
		Size: 276.5 KB (276458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc6868f02b356d04d4a04c2f74b5f77f24a81474cdc0a656e7da4de1c0bae771`  
		Last Modified: Thu, 20 Jun 2024 21:55:39 GMT  
		Size: 20.1 KB (20069 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:bff47e09ce9f4921942fc8828a26d702b73ae34af6e2413ade52337601d84eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78655876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0509f98d762d33f5fc06ca0bf2b2b6c39ef0daba4cb4cbc85bf7dfef24e6464f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb26f139748033dd9f410aaee2fa9f225bf8b64a17b5e3f1adf1ef26427ce27e`  
		Last Modified: Fri, 21 Jun 2024 03:29:57 GMT  
		Size: 293.6 KB (293605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743e448a2b4bba38b1783fb849b3f5093e7931cf69d898520c4f1462ad93a836`  
		Last Modified: Fri, 14 Jun 2024 20:04:04 GMT  
		Size: 67.7 MB (67713294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17aa4a6c18860c6004fb2b335568db1f1bcfcd78962c48ca4fe9172dda6d304`  
		Last Modified: Fri, 21 Jun 2024 03:29:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e542be869cb8ecb61c09d5cc28f6b3a6d7d17f138e340aa8963d988d6a98fa`  
		Last Modified: Fri, 21 Jun 2024 11:34:57 GMT  
		Size: 5.9 MB (5857413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f2f77b231848e16ee251a8cbd2a80bdcd9dd9794b65daf34716579fded05a0`  
		Last Modified: Fri, 21 Jun 2024 11:34:57 GMT  
		Size: 1.4 MB (1423814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcb6838ec5b505516436f167db00a3560930476c5ebc766878190e7bdb6bedb`  
		Last Modified: Fri, 21 Jun 2024 11:34:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:38e11feea40948a6f377e1840784e1f81777bc4b683612afb57ea48148d309c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 KB (20001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f92d40f9f4153ddafbf96443b4df24c0f449fb9ed96d4927aedb2cde513e2e34`

```dockerfile
```

-	Layers:
	-	`sha256:5c2b8bdda6daad1b5fe9724c24fb2a04474320c4bbd57487430fd67e88ebad6e`  
		Last Modified: Fri, 21 Jun 2024 11:34:56 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:000b2628af8c5256f694f07e16989ff4c02f2e8142bbd4557766e043a64eb693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77868704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b73904bec0e6a2208a4a567f64426f987e3688f742cbc059d755b29b32db80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc4b91d7452250ed1597b3c0ff80be71a34634d82b036162d70ec2cab221a87`  
		Last Modified: Fri, 21 Jun 2024 03:29:32 GMT  
		Size: 292.5 KB (292465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8d8376f429e08832ffbb91ed771b1b953556865415b4e4c37033a89a2f8aca`  
		Last Modified: Fri, 14 Jun 2024 17:54:08 GMT  
		Size: 67.7 MB (67713411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf50fd4501ccc7e2735edcd4a4f5bf90bb444e27ed9ee37ee24250240338ed9`  
		Last Modified: Fri, 21 Jun 2024 03:29:32 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c1e7d3b76825ef38ba476087b143882feccb0d7831100a612d2faefada036a`  
		Last Modified: Fri, 21 Jun 2024 11:53:53 GMT  
		Size: 5.3 MB (5346618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02b6e7d9a46971e4cbe2580919a5a40f00a23f2a7b7a3b3691719d3611e91d6`  
		Last Modified: Fri, 21 Jun 2024 11:53:53 GMT  
		Size: 1.4 MB (1420762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef404bfa48ae21fe61018234fa44018ab03fe6e864210a027c21da3813f30474`  
		Last Modified: Fri, 21 Jun 2024 11:53:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:3c7c2104ad6e09b832b670fb1f3889ae711256cfcef38522efae2cca71346880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.3 KB (299289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153a3559f19a258319bee7e08df4da8d6b86b2d73aab96dc2e441fe12435ec1a`

```dockerfile
```

-	Layers:
	-	`sha256:5d4a5d7b0699a1af6c843cb5a9d633b4d6804e3df3b51d2f6631c6108951f899`  
		Last Modified: Fri, 21 Jun 2024 11:53:53 GMT  
		Size: 279.1 KB (279070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5162a3e89c1aef29000d0d3ebe50c410a682a80a60c26eeecbc21f7612a170`  
		Last Modified: Fri, 21 Jun 2024 11:53:53 GMT  
		Size: 20.2 KB (20219 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:f0694f707e9944e09f3b1defbf75633fd7915b9a3eb6b2077969c2a9783add87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78080287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6729c0f0794c8214346a56845a8e64992f082c3bafab8dd53c5f91143153449`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112965af61e48c79f6f081b66e8fcc392cd621303fe32a47457e35dbd92041e4`  
		Last Modified: Fri, 21 Jun 2024 05:03:46 GMT  
		Size: 295.5 KB (295459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2259e4bd2629c850a0f37f6d3351f44770f5d4afee65aac3cddcb3bf2a735031`  
		Last Modified: Fri, 14 Jun 2024 19:43:41 GMT  
		Size: 66.3 MB (66270325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93676ef1db8c89860011e8eeae8d68fb8e5d5e669a04a2a907553aab62aff75`  
		Last Modified: Fri, 21 Jun 2024 05:03:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f1d55f028222d58657cbc8fe4adf0b9ab580edcc3816fa9b372c23bc1a3086`  
		Last Modified: Fri, 21 Jun 2024 12:11:43 GMT  
		Size: 6.0 MB (6027940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ac0a4d7f4556036b38f1c1b7852eaa1f31d3749ff2ed29e9fc0feebddf1c0c`  
		Last Modified: Fri, 21 Jun 2024 12:11:43 GMT  
		Size: 1.4 MB (1397168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328dc2d5161a837f7174baae3b6382739135552357e41f837c00dc7ce0232dda`  
		Last Modified: Fri, 21 Jun 2024 12:11:42 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:a14edf4148a4038368e9fc8c31cf6c7b12773d47c07776b232c74a9f1fdfed7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 KB (297093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc58a289984f52f61289c20720321cfb9ddc9db235778115245ed3cc671a2cb`

```dockerfile
```

-	Layers:
	-	`sha256:e82a6202714f7adf0600e9ffa9649de4335662f5979347ad7bf846da2703f609`  
		Last Modified: Fri, 21 Jun 2024 12:11:43 GMT  
		Size: 276.6 KB (276562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02264b55cb49f0b98d0bb324adc6681f1377c3018f1843f30c854d5605fde545`  
		Last Modified: Fri, 21 Jun 2024 12:11:43 GMT  
		Size: 20.5 KB (20531 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:f087d0bc24815e3f0fe61c70cdfc4a9bc9e172df0dfc5bd3e57d9e3ad4ccf5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77933688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cb7fada8d4c02fa040a12ba2b3904ada3265a1c64f768b9fd2c66f765a63fc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477fe0e563a78bfc8789f98753a872bab84abaf1026e276ac6665d797175815b`  
		Last Modified: Fri, 21 Jun 2024 01:47:42 GMT  
		Size: 295.9 KB (295884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2210b2be98c546d98d20cd631f014745f73d191238d22c5e439478550b6727b8`  
		Last Modified: Fri, 14 Jun 2024 17:54:36 GMT  
		Size: 66.4 MB (66440814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfed35a1567d183c45c7e8a04b11d626d4dd085224a9a1f3f9e560e2bdf63a8`  
		Last Modified: Fri, 21 Jun 2024 01:47:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e156942991c8fd0dee1d39c6026a6a820b2b2425546996f63dd55cb5d7875e61`  
		Last Modified: Fri, 21 Jun 2024 05:27:39 GMT  
		Size: 6.2 MB (6234666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed43d369c0bb3c893179b9919957b886b4a8dc27c24d6cfc1cf51229b74c20`  
		Last Modified: Fri, 21 Jun 2024 05:27:38 GMT  
		Size: 1.4 MB (1390030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53399413ba874498b22ba190e5d937a92f001a69bb0b7cc4084711c02adef3af`  
		Last Modified: Fri, 21 Jun 2024 05:27:38 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:48a8d2f11bda9e488fc1e98f862077889680ef7975883510e81707157a645fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 KB (294765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db22af4bd5cd97ab02a4d87350dd4bdabe61ee063cb8aa3e62ac562b0e055771`

```dockerfile
```

-	Layers:
	-	`sha256:f5a811906cdda5193a973f7e7dbe50ad5ab80c7a9389065e4998f85b00a9d234`  
		Last Modified: Fri, 21 Jun 2024 05:27:38 GMT  
		Size: 274.6 KB (274596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:165f0456aec3600447a0ffdf866cc03690db60f1c06fefdc749c1081274c7410`  
		Last Modified: Fri, 21 Jun 2024 05:27:38 GMT  
		Size: 20.2 KB (20169 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; riscv64

```console
$ docker pull caddy@sha256:cee8aab5183476170e543e56d4b9e3be2337e087ec8ef0cc4217503cc22dc931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78088484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9008588f0ee0a00abe9379ff271e34fd89b467eddea54f3259855d6af20bfa54`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5b5f435f7e590189af756b0088b13452e972213bf9e8b7231c861784440a71`  
		Last Modified: Fri, 21 Jun 2024 07:54:22 GMT  
		Size: 293.2 KB (293177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720f2671938fbfe8609ea6b3e22d6f25d4497370e3b0109cc065588d36d42db6`  
		Last Modified: Fri, 14 Jun 2024 17:57:25 GMT  
		Size: 66.9 MB (66893351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88f851c95d1e14a521b4e4816ea17dc2c49abd212cf82a146a090014479463e`  
		Last Modified: Fri, 21 Jun 2024 07:54:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47e70471f315279dbc09cfc0862dfaa25759d5c8d67346a723b28c82e7edbe8`  
		Last Modified: Fri, 21 Jun 2024 23:12:01 GMT  
		Size: 6.1 MB (6126027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee02451a515770a067f37b4f3a642cd3d6ace4d48865dfee7ed0602822a2e1e`  
		Last Modified: Fri, 21 Jun 2024 23:12:01 GMT  
		Size: 1.4 MB (1404295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778b4687d01f3fd127faba2bfbf05bac7e130f5c1bcd9b222723b6fa9c9341a1`  
		Last Modified: Fri, 21 Jun 2024 23:12:00 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:03bcb157a5a08dd723a1f25579114a346761184e0ecb19cc16bdc6abcdb28711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 KB (294761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c83b0a1978bfec0547d8bb4bfe5d24180f0d5ee4a34399b495bbcab6b966c0`

```dockerfile
```

-	Layers:
	-	`sha256:99ecc2d661c765438c3def62c34098e0c295f214fdacdd68b8ae0b6695f32518`  
		Last Modified: Fri, 21 Jun 2024 23:12:00 GMT  
		Size: 274.6 KB (274592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18ace0b273d7224f18e17cd74e945461e1c89ee357c6feb658d1d58d2fcdd22`  
		Last Modified: Fri, 21 Jun 2024 23:11:59 GMT  
		Size: 20.2 KB (20169 bytes)  
		MIME: application/vnd.in-toto+json

### `caddy:builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:1d8beb97a843f3a33b1e2c2e1fa12545466141b17a4674c935d3e62453380372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79785571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cb7382dad7e46b0dde0d59c20145f5d960874e77a8a7b3b8253361fe626798`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 04 Jun 2024 22:12:59 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Tue, 04 Jun 2024 22:12:59 GMT
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
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dbaf32ffd27702fcbbf4fe4d764f59a796cd2d4f7ea86c0e7975245b7941ca`  
		Last Modified: Fri, 21 Jun 2024 04:04:52 GMT  
		Size: 293.4 KB (293400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54ac55846ff64482893d22cd74289e959d60007f939ee44a6905370f9611de2`  
		Last Modified: Fri, 14 Jun 2024 19:31:27 GMT  
		Size: 68.4 MB (68405222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45e302ad79ac2c0f523d67257e514c47ae55272223df23f6d57e8e6b5d1141f`  
		Last Modified: Fri, 21 Jun 2024 04:04:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d77884a2e7145e3409abc6522f14404277db57aa1aa6c6203d72be3929ce131`  
		Last Modified: Fri, 21 Jun 2024 13:42:20 GMT  
		Size: 6.2 MB (6172713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93655c89f985b43c09e7afa86e9c0e56e6b0b6290014919dc2c0caf064b897f7`  
		Last Modified: Fri, 21 Jun 2024 13:42:20 GMT  
		Size: 1.5 MB (1451785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1d0d0fc096f9fda4df5758730cd6188e6563acf7056da8414c2ac468b07443`  
		Last Modified: Fri, 21 Jun 2024 13:42:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `caddy:builder-alpine` - unknown; unknown

```console
$ docker pull caddy@sha256:c1d67a85200d273be73bf07c7090578704a11f348f9bade8c0bfcc6eb68070e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 KB (294603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c0ef96901535e5796991793b912f162f5fe28d2e53f5a819d08808352d4109`

```dockerfile
```

-	Layers:
	-	`sha256:97e0275981dbbb4978f9104167031d623d5c1b264916d7373cf1d71e26027140`  
		Last Modified: Fri, 21 Jun 2024 13:42:20 GMT  
		Size: 274.5 KB (274504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98b32d3914cee0c2052b81ade680869668c376ca940c1ba365065c97587a9f3`  
		Last Modified: Fri, 21 Jun 2024 13:42:20 GMT  
		Size: 20.1 KB (20099 bytes)  
		MIME: application/vnd.in-toto+json
